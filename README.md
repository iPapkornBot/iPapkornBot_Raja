
from telegram import Update
from telegram.ext import Updater, CommandHandler, CallbackContext

# Define a command callback function
def start(update: Update, context: CallbackContext) -> None:
 update.message.reply_text('Hello! I am your iPapkornBot.')

def help_command(update: Update, context: CallbackContext) -> None:
 update.message.reply_text('Help! Here are the commands you can use: /start, /help')

def main():
 # Replace 'YOUR_TOKEN' with your bot's API token
 updater = Updater("YOUR_TOKEN")

 # Get the dispatcher to register handlers
 dp = updater.dispatcher

 # Register command handlers
 dp.add_handler(CommandHandler("start", start))
 dp.add_handler(CommandHandler("help", help_command))

 # Start the Bot
 updater.start_polling()

 # Run the bot until you send a signal to stop
 updater.idle()

if __name__ == '__main__':
 ter.idle()

if __name__ == '__main__':
 main()
 
