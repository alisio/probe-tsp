# Introdução

O Problema do Caixeiro Viajante "tenta determinar a menor rota para percorrer uma série de cidades (visitando uma única vez cada uma delas), retornando à cidade de origem. Ele é um problema de otimização NP-difícil inspirado na necessidade dos vendedores em realizar entregas em diversos locais (as cidades) percorrendo o menor caminho possível..." (Wikipedia, 2020)

Este notebook do Google Colab almeja ilustrar conceitos de aprendizado de máquina aplicados na otimização dos serviços de uma empresa de segurança patrimonial fictícia, que utiliza drones aéreos para monitoração, cujo problema a ser resolvido é similar ao problema do caixeiro viajante.

O algoritmo utiliza heurística construtiva, do tipo 2-opt, codificado em Python, para determinar a rota otimizada dos vôos dos drones aéreos de monitoração.

Antonio Alisio de Meneses Cordeiro (alisio.meneses@gmail.com)

# Probe Vigilância Inteligente LTDA
---

## Pitch:

Para organizações com presença municipal, que desejam garantir a segurança do seu patrimônio, a Probe Vigilância Inteligente LTDA (empresa fictícia), sediada no bairro Meireles, em Fortaleza-CE, é uma empresa de vigilância que utiliza drones para monitoraração aérea. Diferente das empresas que operam de maneira estática, com transporte terrestre, a Probe utiliza tecnologia IoT com drones aéreos munidos de múltiplos sensores avançados, algoritmo patenteado PCV™, e inteligência artificial para detectar, localizar e alertar em caso de eventos suspeitos. A Probe utiliza rotas otimizadas e dinâmicas, retornando à base de origem, reduzindo o tempo necessário para o trajeto e os custos com transporte e combustível.

## Problema:

A empresa Probe foi a vencedora de um processo licitatório aberto pela prefeitura de Fortaleza, cujo objeto de contratação é o serviço de monitoração de parte do patrimônio, composto por prédios localizados em bairros específicos do município de Fortaleza.

A Probe precisa monitorar os prédios pertencentes à prefeitura de Fortaleza, espalhados em múltiplos bairros da cidade, percorrendo o menor caminho possível, reduzindo o tempo necessário para completar trajeto, os custos inerentes ao transporte e combustível.


# Resultados

|index|nome|latitude|longitude|lat_radians|lon_radians|x|y|
|---|---|---|---|---|---|---|---|
|0|0|meireles|-3.727682|-38.510029|-0.065060|-0.672127|4974.754992|-324.116614|
|1|5|Mucuripe|-3.726926|-38.485426|-0.065047|-0.671697|4976.458594|-324.161640|
|2|8|Varjota|-3.734490|-38.489766|-0.065179|-0.671773|4976.116043|-324.799085|
|3|7|Cocó|-3.751233|-38.488998|-0.065471|-0.671760|4976.073995|-326.256648|
|4|13|Edson Queiroz|-3.775925|-38.478644|-0.065902|-0.671579|4976.647822|-328.448289|
|5|6|Guararapes|-3.763166|-38.493741|-0.065680|-0.671843|4975.678380|-327.271481|
|6|4|Dionísio Torres|-3.747552|-38.506480|-0.065407|-0.672065|4974.887460|-325.857875|
|7|10|Jardim das Oliveiras|-3.780007|-38.512133|-0.065974|-0.672164|4974.311581|-328.650065|
|8|11|Conjunto Palmeiras|-3.848561|-38.537187|-0.067170|-0.672601|4972.183524|-334.485110|
|9|14|Passaré|-3.812427|-38.539118|-0.066539|-0.672635|4972.259960|-331.340377|
|10|9|Fátima|-3.751393|-38.537248|-0.065474|-0.672602|4972.739369|-326.052012|
|11|12|Pici|-3.748823|-38.583673|-0.065429|-0.673412|4969.543062|-325.618536|
|12|3|Barra do Ceará|-3.704828|-38.589112|-0.064661|-0.673507|4969.415192|-321.778138|
|13|2|centro|-3.728274|-38.535950|-0.065071|-0.672579|4972.960250|-324.051318|
|14|1|aldeota|-3.737513|-38.511218|-0.065232|-0.672148|4974.617143|-324.964862|
|0|0|meireles|-3.727682|-38.510029|-0.065060|-0.672127|4974.754992|-324.116614|

# Conclusão

 A rota mais curta de monitoração dos patrimônios indicados pela prefeitura do município de Fortaleza, calculada a partir de algoritmo 2-opt, é de **65.1 km**

A imagem abaixo ilustra a rota mais curta definida pelo algoritmo PCV™, iniciada pelo bairro Meireles.

![Rota Renderizada](https://github.com/alisio/probe-tsp/blob/master/rota_renderizada.png)


# Referências

GEO MIDPOINT. **Geographic Midpoint Calculation Example**. Disponível em \<http://www.geomidpoint.com/example.html>. Acesso em 17 de agosto de 2020.


IBGE. **IBGE disponibiliza coordenadas e altitudes para 21.304 localidades brasileiras**. Disponível em \<https://agenciadenoticias.ibge.gov.br/agencia-sala-de-imprensa/2013-agencia-de-noticias/releases/14126-asi-ibge-disponibiliza-coordenadas-e-altitudes-para-21304-localidades-brasileiras>. Acesso em 17 de agosto de 2020.

MERIDIANOUTPOST. Latitude/Longitude Distance Calculator. Disponível em <http://www.meridianoutpost.com/resources/etools/calculators/calculator-latitude-longitude-distance.php?>. Acesso em 19 de agosto de 2020.

PRADO, Kelvin. **Github - kelvins/Municipios-Brasileiros**. Disponível em \<https://github.com/kelvins/Municipios-Brasileiros>. Acesso em 17 de agosto de 2020.


TAYLOR, Roy. **Travelling Salesman in scipy**
. Disponível em \<https://stackoverflow.com/questions/25585401/travelling-salesman-in-scipy>. Acesso em 17 de agosto de 2020

VIASAT. **Viasat passa a fornecer internet a bordo para aviões da Aeroméxico** .Disponível em \<https://viasatdobrasil.com.br/viasat-passa-a-fornecer-internet-a-bordo-para-avioes-da-aeromexico/>. Acesso em 18 de agosto de 2020

WIKIPEDIA. **2-opt**. Disponível em \<https://en.wikipedia.org/wiki/2-opt>. Acesso em 18 de agosto de 2020.

WIKIPEDIA. **Problema do Caixeiro Viajante**. Disponível em \<https://pt.wikipedia.org/wiki/Problema_do_caixeiro-viajante>. Acesso em 17 de Agosto de 2020.
