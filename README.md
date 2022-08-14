# DestroyWorld Documentation
  Данный майнкрафт плагин позволит ваам создать свой вирус заражающий блоки!
  
  [![Video](https://img.youtube.com/vi/pErfLsTStkw/0.jpg)](https://www.youtube.com/watch?v=pErfLsTStkw)

# Config - Распространие
  settings:
  
    # Радиус разброса блоков от каждого ответвления (По умолчанию: 1)
    radius: 1

    # Задержка на появление блоков (По умолчанию: 10)
    delay: 10

    # Сколько будет отвлетений (По умолчанию: 5)
    ways: 5

# Config - Оповещение
  alert:
  
    # Сообщение на экране
    title: "&4ВНИМАНИЕ!"
    subtitle: "&cМир поразил грибок!"

    # Сообщение в чате
    messageChat: "&7<&c!&7> &4ВНИМАНИЕ! &cМир поразил грибок! Пожалуйста соберите для себя самые главные ресурсы и не сооружайте постройки на земле!"

    # Звуковое сопровождение (По умолчанию: "ENTITY_ENDER_DRAGON_DEATH")
    sound: ENTITY_ENDER_DRAGON_DEATH

# Config - Блоки
  blocks:

    # Блок, который будет все захватывать (По умолчанию: SCULK)
    target: SCULK

    # Блоки которые нельзя заражать (По умолчанию: AIR)
    forbidden:
      - # НЕ ТРОГАТЬ!
      - AIR

  surface:
    
    # Комманды на поверхности (При заражении)
    
    # Состояние (По умолчанию: false)
    enable: false

    # Шанс Выполнить комманду 0%-200% (По умолчанию: 5%)
    change: 5

    # Какая комманда будет выполнятся
    command: "summon minecraft:lightning_bolt %cord"

  coming:
  
    # Команды, которые выполняются после наступления игрока на зараженный блок (%cord - координаты игрока %player - ник игрока)
    
    # Состояние (По умолчанию: false)
    enable: false
    
    # Какая комманда будет выполнятся
    commands:
      - "effect give %player minecraft:darkness 15"
      - "effect give %player minecraft:nausea 15 30"
      - "effect give %player minecraft:slowness 15 2"
      - "summon minecraft:lightning_bolt %cord"
      - "playsound minecraft:entity.zombie_villager.cure player %player %cord"

  # Плагин DiscordAlert (Устанавливается отдельно)
  discord:

    # Аватарка webhook. Указывать в url
    avatar: "https://img.icons8.com/fluency/344/virus.png"
    # Сообщение в дискорд
    messageDiscord: "⚠️ ВНИМАНИЕ! На сервере завелся грибок. Пожалуйста не сооружайте на земле свои постройки!"
