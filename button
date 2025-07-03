@bot.inline_handler(lambda query: True)
def inline_game(inline_query):
    try:
        # Создаём inline-результат с кнопкой
        game = telebot.types.InlineQueryResultArticle(
            id="1",
            title="🎮 Мини-игра: Угадай число",
            description="Нажмите, чтобы начать!",
            input_message_content=telebot.types.InputTextMessageContent(
                message_text="Привет! Нажми кнопку, чтобы сыграть 👇"
            ),
            reply_markup=telebot.types.InlineKeyboardMarkup().add(
                telebot.types.InlineKeyboardButton(
                    text="Играть", 
                    web_app=telebot.types.WebAppInfo(url="https://bot-telegram-six-gamma.vercel.app")
                )
            )
        )
        bot.answer_inline_query(inline_query.id, [game])
    except Exception as e:
        print(e)
