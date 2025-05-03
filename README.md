import telebot

chave_api = "7576227850:AAGCE4LH5Y66YWZS0SvxfzdXA6g0vUXVLOY"

bot = telebot.TeleBot(chave_api)

@bot.message_handler(commands = ["start"])
def boas_vindas(message):
    chat_id = message.chat.id
    texto_bot = (
    "Salve, fã da Furia eu sou o bot para os fãs da FURIA! Para que possamos interagir use os seguintes comandos:\n\n" \
        "/curiosidades - Ver as curiosidades e informações sobre a organização!\n" 
        "/desempenho - Ver o desempenho atual da Furia no CS!\n" 
        "/lineup - Para ver a atual lineup do time!\n" 
        "/ProximoJogo - Para ver os próximos jogos da FUria!\n" 
        "/RedesSociais - Para ver as redes socias da organização!\n" 
        "/titulos - Para ver todos os títulos da Fúria no CS!\n"
        "/sair - Para finalizar a conversa.\n")
    bot.send_message(chat_id, texto_bot)

@bot.message_handler(commands = ["curiosidades"])
def curiosidades(message):
    chat_id = message.chat.id
    texto_bot = (
    "Aqui estão algumas curiosidades sobre a Fúria:\n\n" 
    "1. FURIA nasceu no CS:GO:\n" 
        "A organização foi fundada em 2017 por André Akkari, Jaime Pádua, Cris Guedes e Guerri(Nicholas Nogueira). Criada por ex-jogadores e empresários eles tinham como missão de ser uma das organizações mais agressivas e profissionais do mundo!\n\n" \
    "2. Estilo de jogo agressivo:\n" 
        "A FURIA ficou famosa pelo seu estilo de jogo super agressivo, muitas vezes apostando em rushes rápidos e jogadas inesperadads.\n\n" 
    "3. Primeira org BR com gaming house nos EUA:\n" 
        "A FURIA foi a primeira organização brasileira de CS a se mudar e montar sede nos Estados Unidos. Isso facilitou a participação constante nos campeonatos norte-americanos e internacionais.\n\n" \
    "4. Equipe formada por grandes talentos e talentos revelados:\n" 
        "Jogadores como KSCERATO e yuurih foram duas grandes revelações da própria organização e se tornaram destaques globais no CS. Vale lembrar que a FURIA ja contratou grandes jogadores também como o próprio FALLEN lenda do cs brasileiro e também chelo ex-MIBR que chegou com muito hype pela torcida.\n\n" \
    "5. Presença em vários jogos:\n" 
        "Além do CS, a FURIA tem times em League of Legends, VALORANT, Apex Legends, Free Fire, Chess, Poker e na Kings League.\n\n" 
    "6. Primeira organização brasileira a jogar uma semifinal de Major:\n" 
        "No PGL Major Antwerp 2022, a FURIA foi a primeira equipe brasileira a alcançar uma semifinal de Major no CS:GO.\n\n" 
    "7. Investimento em educação:\n" 
        "A FURIA lançou iniciativas educacionais como a FURIA Academy, buscando formar novos talentos e oferecer educação sobre o cenário competitivo.\n\n" 
    "8. Patrocínios de peso: \n" 
        "A organização conta com parcerias de grandes marcas, como Red Bull, PokerStars, AOC, Pume e outras.\n\n" 
    "9. Nome e identidade visual:\n" 
        "O nome FURIA e sua logotipo de pantera foram criados para transmitir agressividade, velocidade e impacto.\n\n" 
    "10 Sua torcida:\n" 
        "Sua torcida é uma das mais fanáticas dos eSports, conhecida por levar bandeiras, gritos de torcida e até sinalizadores, são conhecidos como os Ultras da FURIA.")
    bot.send_message(chat_id, texto_bot)

@bot.message_handler(commands = ["desempenho"])
def desempenho(message):
    chat_id = message.chat.id
    texto_bot = (
    "Desempenho da FURIA em 2025:\n\n"
        "Partidas jogadas (últimos 3 meses): 21\n"
        "Vitórias: 9 ✅\n"
        "Derrotas: 12 ❌\n"
        "Aproveitamento de: 43%\n"
        "Ranking Mundial (HLTV): 17º lugar\n\n"
    "Mudanças recentes:\n"
        "Saída de chelo e skullz\n"
        "Entradas de molodoy e YEKINDAR")
    bot.send_message(chat_id, texto_bot)

@bot.message_handler(commands = ["lineup"])
def lineup(message):
    chat_id = message.chat.id
    texto_bot = (
    "A atual lineup do time da FURIA no CS é essa:\n\n"
        "🐐FalleN - Capitão e líder dentro do jogo (IGL)\n"
        "yuurih - Rifler\n"
        "KSCERATO - Rifler\n"
        "molodoy - Sniper, ingressou na equipe em abril de 2025, substituindo chelo.\n"
        "YEKINDAR - Rifler, juntou-se à equipe em abril de 2025, substituindo skullz.\n\n"
    "O treinador atual da equipe é sidde.")
    bot.send_message(chat_id, texto_bot)

@bot.message_handler(commands = ["ProximoJogo"])
def próximo_jogo(message):
    chat_id = message.chat.id
    texto_bot = (
    "Próximos jogos da FURIA: \n\n"
        "Até o momento, a FURIA tem os seguintes torneios programados para maio e junho: \n\n"
        "PGL Astana 2025:\n"
        "📅 De 9 a 17 de maio de 2025\n"
        "📍 Astana, Cazaquistão\n\n"
        "IEM Dallas 2025:\n"
        "📅 De 18 a 24 de maio de 2025\n"
        "📍 Dallas, Estados Unidos\n\n"
        "BLAST.tv Austin Major 2025:\n"
        "📅 De 2 a 22 de junho de 2025\n"
        "📍 Austin, Estados Unidos")
    bot.send_message(chat_id, texto_bot)
@bot.message_handler(commands = ["RedesSociais"])
def contato(message):
    chat_id = message.chat.id
    texto_bot = (
    "As redes sociais da FURIA são:\n\n"
        "📱 Instagram: @furiagg\n"
        "🔵 Twitter: @furiagg\n"
        "🔴 YouTube: FURIA\n"
        "🐾 Site oficial: https://www.furia.gg")
    bot.send_message(chat_id, texto_bot)

@bot.message_handler(commands = ["titulos"])
def titulos(message):
    chat_id = message.chat.id
    texto_bot = (
    "A FURIA possui os seguintes titulos no CS:\n\n"
    "Principais conquistas internacionais:\n"
        "DreamHack Open Anaheim 2020 🏆\n"
        "Elisa Masters Espoo 2022 🏆\n"
        "Arctic invitational 2019 - Helsinque 🏆\n"
        "ESEA Season 31: Global Challenge 🏆\n\n"
    "Titulos regionais: 🏆\n"
        "BLAST Premier: Spring 2020 Showdown - America do Norte 🏆\n"
        "CS_Summit 8 - America do Norte 2021 🏆\n"
        "IEM New York 2020 NA 🏆\n"
        "ESL Pro League Season 12: North America 🏆")
    bot.send_message(chat_id, texto_bot)

@bot.message_handler (commands = ["sair"])
def sair(message):
    chat_id = message.chat.id
    texto_bot = (
    "Obrigado por interagir com o bot da FURIA!🐱‍👤🐾\n"
    "Fique ligado nas redes sociais e acompanhe a FURIA nos proximos campeonatos.\n"
    "Volte quando quiser! Até mais!👋")
    bot.send_message(chat_id, texto_bot)

@bot.message_handler(func=lambda message: True)
def resposta_padrao(message):
    chat_id = message.chat.id
    texto_bot = (
        "❌Não consegui entender oque você mandou!❌\n\n"
        "🤖Estou programado para responder apenas aos seguintes comandos:\n\n"
        "/curiosidades - Ver as curiosidades e informações sobre a organização!\n"
        "/desempenho - Ver o desempenho atual da FURIA no CS!\n"
        "/lineup - Para ver a atual lineup do time!\n"
        "/proximo jogo - Para ver os próximos jogos da FURIA!\n"
        "/redes sociais - Para ver as redes sociais da organização!\n"
        "/titulos - Para ver todos os títulos da FURIA no CS!\n"
        "/sair - Para finalizar a conversa."
    )
    bot.send_message(chat_id, texto_bot, parse_mode="Markdown")
bot.polling()
