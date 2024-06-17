<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(f"# {config['name'].title()}")
]]]-->
# Nuclear Energy
<!--//[[[end]]]-->

## Mission

Tilt's mission is to map every theme to a basket of stocks for anyone to invest in. Mappings are AI generated and expert curated.
Expert improvements are accepted if they provide a better representation of a given theme.

## Theme Prompt
<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(config['prompt'])
]]]-->
The increasing integration of AI in various sectors is driving the need for more robust and sustainable energy solutions, such as nuclear power.
<!--[[[end]]]-->

## Theme Stocks

<!--[[[cog
import cog
import csv
import json

with open('context.json') as file:
  contexts = json.load(file)

def _get_context_str_for_ticker(ticker):
  try:
    context = contexts[ticker]
    context_str = context['chat_gpt'] or context['claude'] or ""
  except KeyError:
    context_str = ""

  return context_str

cog.outl("| Ticker  | Context | Source |")
cog.outl("| ------- | ---- | ---- |")

with open('theme.csv') as file:
  reader = csv.reader(file)
  next(reader) # skip the header
  for row in reader:
    context_str = _get_context_str_for_ticker(row[0])
    cog.outl(f"| {row[0]} | {context_str} | {row[1]} |")
]]]-->
| Ticker  | Context | Source |
| ------- | ---- | ---- |
| AES | AES Corporation is diversifying its energy portfolio with investments in nuclear power to meet the rising energy demands. | chat_gpt |
| BWXT | BWX Technologies provides nuclear components and services, benefiting indirectly from the increased demand for nuclear energy. | chat_gpt,claude,twitter,google |
| ETR | Entergy Corporation operates several nuclear power plants and is poised to benefit from the trend towards sustainable energy solutions. | chat_gpt,google |
| EXC | Exelon Corporation is one of the largest nuclear power plant operators in the U.S., benefiting directly from the trend towards sustainable energy. | chat_gpt,claude,google |
| FLR | Fluor Corporation is involved in the construction and maintenance of nuclear power plants, benefiting indirectly from the increased demand. | chat_gpt,claude |
| GE | General Electric supplies nuclear reactors and technology, indirectly benefiting from the growth in nuclear energy. | chat_gpt,google |
| HON | Honeywell International provides control systems and technology for nuclear power plants, benefiting indirectly from the trend. | chat_gpt,claude |
| NEE | NextEra Energy is a leader in renewable energy and is investing heavily in sustainable energy solutions, including nuclear power. | chat_gpt |
| PCG | Pacific Gas and Electric Company operates nuclear power plants and is investing in sustainable energy infrastructure. | chat_gpt |
| SO | Southern Company is investing in nuclear energy projects to meet the growing demand for sustainable energy solutions. | chat_gpt,claude |
| SRE | Sempra Energy is involved in various sustainable energy projects, including nuclear power, to support the increasing energy demands driven by AI integration. | chat_gpt |
| WEC | WEC Energy Group is investing in nuclear energy projects to support the growing need for sustainable energy solutions. | chat_gpt,google |
| XEL | Xcel Energy is committed to increasing its nuclear energy capacity as part of its sustainable energy strategy. | chat_gpt |
| AMZN | Amazon's AWS, a major provider of AI services, could benefit from the use of nuclear power as part of its commitment to 100% renewable energy. | claude,twitter |
| CCJ | Cameco, a major uranium producer, could see increased demand as nuclear power becomes more important for meeting AI energy needs. | claude,twitter,google |
| CEG | Constellation Energy's nuclear power plants could benefit from increased demand driven by the growth of AI. | claude,google |
| CW | Curtiss-Wright's components and services for the nuclear power industry could benefit from increased investment driven by AI adoption. | claude |
| NVDA | Nvidia's AI hardware and software will be crucial for AI development and deployment, driving the need for robust energy solutions like nuclear power. | claude,twitter |
| SMR | NuScale Power's small modular nuclear reactors could provide flexible, scalable energy solutions for AI applications. | claude,twitter,google |
| DNN |  | twitter,google |
| NXE |  | twitter,google |
| UEC |  | twitter,google |
| UUUU |  | twitter,google |
| EU |  | google |
| URG |  | google |
| OKLO |  | experts |
| VST |  | experts |
<!--[[[end]]]-->

## License

<p>
This project is licensed under <a href="./LICENSE">AGPLv3</a>.
</p>


## Contributors

Thank you for your improvements! We appreciate all the contributions from the community.

<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  repo = config['github_repo'].lower()
  cog.outl(f'<a href="https://github.com/gettilt/{repo}/graphs/contributors">')
  cog.outl(f'  <img src="https://contrib.rocks/image?repo=gettilt/{repo}" />')
  cog.outl('</a>')
]]]-->
<a href="https://github.com/gettilt/nuclear/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=gettilt/nuclear" />
</a>
<!--[[[end]]]-->

## Join Our Community

<a href="https://discord.gg/4vYMhRpaMY" target="_blank">
<img src="https://discord.com/api/guilds/1179775688421683220/widget.png?style=banner3" alt="">
</a>
