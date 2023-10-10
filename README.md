![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)

> # Основы Git:
> >Понимание основных концепций Git, таких как коммиты, ветки, слияния, клонирование репозиториев и отправка изменений, поможет вам лучше понимать содержание инструкции.



# Использование Git в колледже

В этом `README` файле описаны различные способы использования Git в учебной среде колледжа, включая локальные и удаленные методы.

# 1. Локальный Git-репозиторий

Вы можете инициировать локальный Git-репозиторий на своем компьютере и вести контроль версий для ваших проектов локально. Этот метод подходит для индивидуальной разработки.

# 2. Git через SSH

Если ваш колледж позволяет подключаться к удаленным серверам по SSH, вы можете развернуть удаленный Git-репозиторий на хостинг-платформе, такой как GitHub, GitLab или Bitbucket. Затем вы можете работать с репозиторием через SSH.

# 3. Git через HTTPS

Если использование SSH недоступно, многие хостинг-платформы также поддерживают доступ к Git-репозиториям через HTTPS. Вам придется авторизоваться на своем аккаунте на хостинг-платформе и использовать HTTPS-URL для клонирования и отправки изменений в репозиторий.

# 4. Git посредством Git-подсервера в вашем колледже

Если ваш колледж предоставляет возможность использовать Git-сервер внутри сети учебного заведения, вы можете создать свой собственный Git-сервер и использовать его для совместной работы с учебными проектами.

# 5. Использование Git-клиента с поддержкой прокси

Если прокси-сервер является препятствием для доступа к внешним Git-репозиториям, вы можете настроить Git-клиент для работы через прокси. В большинстве случаев, ваши системные администраторы или техническая поддержка могут предоставить вам настройки прокси для использования.

# 6. Git через локальную сеть (LAN)

Если у вас есть возможность создать локальную сеть (например, в рамках комнаты в общежитии), вы можете развернуть Git-сервер на одном из компьютеров в локальной сети и использовать его для совместной работы.

<hr>

## 1. Локальный Git-репозиторий

Вы можете инициировать локальный Git-репозиторий на своем компьютере и вести контроль версий для ваших проектов локально. Этот метод подходит для индивидуальной разработки.

#### Инструкция:

1. Установите Git на свой компьютер, если он не установлен. [Скачайте Git](https://git-scm.com/downloads) и установите его.

2. Откройте терминал или командную строку на своем компьютере.

3. Перейдите в каталог, где находится ваш проект, используя команду `cd ПУТЬ_К_ПРОЕКТУ`.

4. Инициируйте Git-репозиторий с помощью команды:

```
git init
```

5. Добавьте файлы в репозиторий с помощью команды:
   
```
git add .
```

6. Зафиксируйте изменения с комментарием:

```
git commit -m "Ваш комментарий к изменениям"
```


7. При необходимости создайте удаленный репозиторий на хостинг-платформе Git (например, GitHub) и добавьте его в качестве удаленного источника:

```
git remote add origin ССЫЛКА_НА_РЕПОЗИТОРИЙ
```


8. Отправьте изменения в удаленный репозиторий:

```
git push -u origin master
```

### 2. Git через SSH

Если ваш колледж позволяет подключаться к удаленным серверам по SSH, вы можете развернуть удаленный Git-репозиторий на хостинг-платформе Git и работать с ним через SSH.

#### Инструкция:

1. Установите Git, если он не установлен, и сгенерируйте SSH-ключи на своем компьютере.

2. Добавьте свой открытый SSH-ключ к вашему аккаунту на хостинг-платформе Git.

3. Создайте новый репозиторий на хостинг-платформе Git, если его еще нет.

4. Клонируйте репозиторий на свой компьютер:

```
git clone git@хостинг-платформа.com:пользователь/репозиторий.git
```

5. Внесите изменения в проект и зафиксируйте их, используя `git add`, `git commit`, и отправьте изменения на сервер с помощью `git push`.

## 3. Git через HTTPS

Если использование SSH недоступно, многие хостинг-платформы также поддерживают доступ к Git-репозиториям через HTTPS.

### Инструкция:

1. Установите Git, если он не установлен, и создайте аккаунт на хостинг-платформе Git.

2. Создайте новый репозиторий на хостинг-платформе Git, если его еще нет.

3. Клонируйте репозиторий на свой компьютер, используя HTTPS-ссылку:

```
git clone https://хостинг-платформа.com/пользователь/репозиторий.git
```


4. Внесите изменения в проект и зафиксируйте их, используя `git add`, `git commit`, и отправьте изменения на сервер с помощью `git push`.

## 4. Git посредством Git-подсервера в вашем колледже

Если ваш колледж предоставляет возможность использовать Git-сервер внутри сети учебного заведения, вы можете создать свой собственный Git-сервер и использовать его для совместной работы с учебными проектами.

(Инструкции будут зависеть от настроек и доступности вашего локального Git-сервера. Обратитесь к администраторам для инструкций.)

## 5. Использование Git-клиента с поддержкой прокси

Если прокси-сервер является препятствием для доступа к внешним Git-репозиториям, вы можете настроить Git-клиент для работы через прокси.

### Инструкция:

1. Установите Git, если он не установлен, и настройте его на своем компьютере.

2. Установите настройки прокси для Git, указав адрес и порт вашего прокси-сервера:

```
git config --global http.proxy http://адрес_прокси:порт
```

3. После настройки прокси вы сможете использовать Git через него для клонирования, отправки и получения изменений из удаленных репозиториев.

**## 6. Git через локальную сеть (LAN)

Если у вас есть возможность создать локальную сеть (например, в рамках комнаты в общежитии), вы можете развернуть Git-сер

## 6. Git через локальную сеть (LAN)

Если у вас есть возможность создать локальную сеть (например, в рамках комнаты в общежитии), вы можете развернуть Git-сервер на одном из компьютеров в локальной сети и использовать его для совместной работы.

### Инструкция:

1. Выберите один из компьютеров в вашей локальной сети в качестве Git-сервера.

2. Инициируйте Git-репозиторий на этом компьютере с помощью команды `git init`.

3. Настройте доступ к этому репозиторию для других компьютеров в сети. Убедитесь, что другие компьютеры имеют доступ к репозиторию через сеть.

4. Компьютеры в локальной сети могут клонировать этот репозиторий, вносить изменения и отправлять их на сервер через локальную сеть.

Выберите наиболее подходящий метод в зависимости от доступных ресурсов и политики вашего колледжа. Обратитесь к системным администраторам или преподавателям, чтобы получить дополнительные рекомендации и инструкции.
