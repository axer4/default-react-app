1. Создать репозиторий на гите и клонировать на комп, запустить:
            git clone url-путь-к-репозиторию

2. Запустить: 
             npm init -y

3. Сохранить появившийся в папке package.json, чтоб из него прописать в новый пути и имена папок

4. В клонированную папку скопировать с заменой необходимые файлы и папки (все из папки variant), прописать пути, имена и т.п. (а именно: "name":, "description":, "author":, "homepage":, последнее очень внимательно, чтоб правильно работал деплой!) в скопированном (с заменой) package.json из сохраненного ранее (см. п. 3). Можно прописать по новому README.md, в папке можно ещё поудалять ненужные на на настоящий момент файлы (начинаются с _)...

5. Запустить: 
             npm install 
   (Должны установится все пакеты, зависимости с сохранением связей с репозиторием на гитхаб, Дожен установится линтинг, проп-тайпс, модерн-нормалайз...)

6. Запустить:
            npm start

Откроется страница в браузере. Можно работать, работать, работать.....

7. Каммитить-пушить на гитхаб в три операции (пордок важен! На всякий случай остановить локальный сервер командой ctrl+c или открыть другой терминал):
                    git add .       (точка важна)
					git commit -m 'name of commit'
					git push
					
8. Деплоить только после очередного камита-пуша (ничего не меняя в файлах проекта, перед этим проверить, чтоб правильно был прописан путь к папке деплоя в package.json, ("homepage":) он отличается от пути к репозиторию на гите) командой:
                    npm run deploy
					


Дополнительно:
					
Чтобы проверить, является ли какой-либо модуль в проекте «старым»:
            npm outdated

Чтобы обновить все зависимости, если вы уверены, что это желательно (перед этим лучше забекапить package.json, если что-то пойдет не так, его можно востановить, запустить npm install и все откатится):
            npm update или npx update
			
Или, чтобы обновить одну зависимость, такую ​​как ,например, xml2js:
        npm update xml2js
