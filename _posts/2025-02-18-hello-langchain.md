---
categories: genai
---
<table>
  <tr>
  <th>OpenAI</th>
  <th>LangChain</th>
  </tr>
  
  <tr>
  <td>

<pre>
import os
from openai import OpenAI

llm_model = 'gpt-4o-mini'

def get_completion(prompt, model=llm_model):
    messages = [{"role": "user", "content": prompt}]
    client = OpenAI(api_key=os.environ['OPENAI_API_KEY'])
    completion = client.chat.completions.create(
        model=llm_model,
        messages=messages,
        temperature=0, 
    )
    return completion.choices[0].message.content

get_completion("What is 1+1?")

customer_email = """
Arrr, I be fuming that me blender lid \
flew off and splattered me kitchen walls \
with smoothie! And to make matters worse,\
the warranty don't cover the cost of \
cleaning up me kitchen. I need yer help \
right now, matey!
"""

style = """American English \
in a calm and respectful tone
"""

prompt = f"""Translate the text \
that is delimited by triple backticks 
into a style that is {style}.
text: ```{customer_email}```
"""

print(prompt)

response = get_completion(prompt)

print(response)
</pre>

  </td>
  <td>
<pre>

  from langchain_openai import ChatOpenAI

# To control the randomness and creativity of the generated
# text by an LLM, use temperature = 0.0
llm = ChatOpenAI(temperature=0.0, model=llm_model)

# ### Prompt template

template_string = """Translate the text \
that is delimited by triple backticks \
into a style that is {style}. \
text: ```{text}```
"""

from langchain.prompts import ChatPromptTemplate

prompt_template = ChatPromptTemplate.from_template(template_string)

prompt_template.messages[0].prompt

prompt_template.messages[0].prompt.input_variables

customer_style = """American English \
in a calm and respectful tone
"""

customer_email = """
Arrr, I be fuming that me blender lid \
flew off and splattered me kitchen walls \
with smoothie! And to make matters worse, \
the warranty don't cover the cost of \
cleaning up me kitchen. I need yer help \
right now, matey!
"""

customer_messages = prompt_template.format_messages(
                    style=customer_style,
                    text=customer_email)

print(customer_messages)

# Call the LLM to translate to the style of the customer message
customer_response = llm.invoke(customer_messages)

print(customer_response)
</pre>

  </td>
  </tr>
  </table>
