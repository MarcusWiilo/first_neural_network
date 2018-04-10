==========================================
Bike Sharing Dataset
==========================================

Hadi Fanaee-T

Laboratory of Artificial Intelligence and Decision Support (LIAAD), University of Porto
INESC Porto, Campus da FEUP
Rua Dr. Roberto Frias, 378
4200 - 465 Porto, Portugal


=========================================
Background 
=========================================

Os sistemas de compartilhamento de bicicletas são uma nova geração de aluguel de bicicletas tradicionais, onde todo o processo de associação, locação e retorno
volta tornou-se automática. Através destes sistemas, o usuário pode facilmente alugar uma bicicleta a partir de uma determinada posição e retornar
de volta a outra posição. Atualmente, existem cerca de 500 programas de compartilhamento de bicicletas em todo o mundo, compostos de
mais de 500 milhares de bicicletas. Hoje, existe um grande interesse nesses sistemas devido ao seu importante papel no tráfego,
questões ambientais e de saúde.

Além das aplicações interessantes do mundo real dos sistemas de compartilhamento de bicicletas, as características dos dados gerados
esses sistemas os tornam atraentes para a pesquisa. Em oposição a outros serviços de transporte, como ônibus ou metrô, a duração
de viagem, partida e chegada é explicitamente registrado nestes sistemas. Esse recurso transforma o sistema de compartilhamento de bicicletas em
uma rede de sensores virtuais que pode ser usada para detectar a mobilidade na cidade. Assim, espera-se que a maioria dos
eventos na cidade poderiam ser detectados através do monitoramento desses dados.

=========================================
Data Set
=========================================

O processo de aluguel de bicicletas compartilhadas é altamente correlacionado com as configurações ambientais e sazonais. Por exemplo, condições climáticas,
precipitação, dia da semana, estação do ano, hora do dia, etc. podem afetar os comportamentos de aluguel. O conjunto de dados principais está relacionado
o registro histórico de dois anos correspondente aos anos de 2011 e 2012 do sistema Capital Bikeshare, Washington D.C., EUA, que é
publicamente disponível em http://capitalbikeshare.com/system-data. Agregamos os dados em duas horas e diariamente e, em seguida,
extraído e adicionado o tempo correspondente e informações sazonais. As informações meteorológicas são extraídas de http://www.freemeteo.com.

=========================================
Associated tasks
=========================================

	- Regressão: 
		Previsão de contagem de aluguel de bicicleta por hora ou diariamente com base nas configurações ambientais e sazonais.
	
	- Detecção de eventos e anomalias:
		A contagem de bicicletas alugadas também está correlacionada a alguns eventos na cidade, que são facilmente rastreados pelos mecanismos de busca.
		Por exemplo, consulta como "2012-10-30 washington d.c." no Google retorna resultados relacionados ao furacão Sandy. Alguns dos eventos importantes são
		identificado em [1]. Portanto, os dados podem ser usados para validação de algoritmos de detecção de anomalias ou eventos.


=========================================
Files
=========================================

	- Readme.txt
	- hour.csv - Contagem de compartilhamento de bicicletas agregada de hora em hora. Registros: 17379 horas
	- day.csv - As contagens de partilha de bicicletas são agregadas diariamente. Registros: 731 dias

	
=========================================
Dataset characteristics
=========================================	

Tanto o hour.csv quanto o day.csv possuem os seguintes campos, exceto hr, que não está disponível no day.csv
	
	- instant: record index
	- dteday : date
	- season : season (1:springer, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2011, 1:2012)
	- mnth : month ( 1 to 12)
	- hr : hour (0 to 23)
	- holiday : weather day is holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : Normalized temperature in Celsius. The values are divided to 41 (max)
	- atemp: Normalized feeling temperature in Celsius. The values are divided to 50 (max)
	- hum: Normalized humidity. The values are divided to 100 (max)
	- windspeed: Normalized wind speed. The values are divided to 67 (max)
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered
	
=========================================
License
=========================================
Use of this dataset in publications must be cited to the following publication:

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

@article{
	year={2013},
	issn={2192-6352},
	journal={Progress in Artificial Intelligence},
	doi={10.1007/s13748-013-0040-3},
	title={Event labeling combining ensemble detectors and background knowledge},
	url={http://dx.doi.org/10.1007/s13748-013-0040-3},
	publisher={Springer Berlin Heidelberg},
	keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
	author={Fanaee-T, Hadi and Gama, Joao},
	pages={1-15}
}

=========================================
Contact
=========================================
	
Para mais informações sobre este conjunto de dados, por favor contacte Hadi Fanaee-T (hadi.fanaee@fe.up.pt)
