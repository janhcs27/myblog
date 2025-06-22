---
titel: How To
date: 2025-06-21
draft: false
tags:
  - HalloWelt
  - Test
---
# Test
## Git x Github
Zum Speichern unserer Websitedaten verwenden wir Github. Diese Plattform bietet uns eine zuverlässige und effiziente Möglichkeit, alle relevanten Dateien und Informationen zentral zu verwalten. Durch die Nutzung von GitHub können wir nicht nur den aktuellen Stand unserer Website sichern, sondern auch frühere Versionen nachvollziehen und bei Bedarf wiederherstellen. Darüber hinaus ermöglicht uns die Versionskontrolle, Änderungen nachzuvollziehen und im Team gemeinsam an der Weiterentwicklung der Website zu arbeiten.

## Hugo
Hugo nutzen wir, um ein schönes Theme für die Website zu haben. Das bedeutet, dass wir mit Hugo ein modernes und ansprechendes Design für unseren Internetauftritt realisieren können. Hugo ist ein sogenannter Static Site Generator, der es uns ermöglicht, Webseiten schnell und effizient zu erstellen, ohne dass wir uns um komplizierte Backend-Programmierung kümmern müssen. 

Ein großer Vorteil von Hugo ist die große Auswahl an vorgefertigten Themes, die sich leicht anpassen lassen. So können wir das Aussehen und die Struktur der Website ganz nach unseren Vorstellungen gestalten. Die Themes sind meist responsiv, das heißt, sie sehen auf verschiedenen Geräten wie Smartphones, Tablets und Computern immer gut aus. Außerdem sorgt Hugo dafür, dass die Seiten sehr schnell laden, was sowohl für die Nutzererfahrung als auch für Suchmaschinen vorteilhaft ist.

Durch die Nutzung von Hugo sparen wir Zeit und Aufwand bei der Entwicklung und Pflege der Website. Gleichzeitig profitieren wir von einer modernen Optik und einer klaren, übersichtlichen Präsentation unserer Inhalte.

### Hugo installieren
```bash
brew install hugo
```
### Hugo installation überprüfen
```bash
hugo version
```
### Hugo Website erstellt
Gehe in ein Verzeichnis, in dem du arbeiten möchtest. Das bedeutet, dass du zunächst den Ordner auswählst, in dem du deine Dateien speichern oder bearbeiten willst. Dies kannst du beispielsweise im Terminal oder in der Eingabeaufforderung tun, indem du den Befehl `cd` (change directory) verwendest, gefolgt vom Pfad zu dem gewünschten Verzeichnis. Wenn du zum Beispiel im Terminal arbeitest und in den Ordner "Projekte" auf deinem Desktop wechseln möchtest, gibst du folgenden Befehl ein:

```bash
cd ~/Desktop/Projekte
```

Stelle sicher, dass das Verzeichnis existiert, bevor du hinein wechselst. Du kannst dir mit dem Befehl `ls` (unter Linux oder macOS) oder `dir` (unter Windows) die vorhandenen Ordner anzeigen lassen. Falls das gewünschte Verzeichnis noch nicht existiert, kannst du es mit dem Befehl `mkdir` erstellen, zum Beispiel:

```bash
mkdir ~/Desktop/Projekte
cd ~/Desktop/Projekte
```

Das Arbeiten im richtigen Verzeichnis hilft dir, deine Dateien und Projekte übersichtlich zu organisieren und vermeidet Verwechslungen oder das versehentliche Überschreiben wichtiger Daten.

Jetzt erstellen wir die neue Hugo Seite
```bash
hugo new site JaSBlog
```

Bevor wir weitermachen können, müssen wir ein Git-Repository erstellen. Ein Git-Repository dient als zentrale Anlaufstelle, um den Quellcode und alle zugehörigen Dateien unseres Projekts zu verwalten. Es ermöglicht uns, Änderungen nachzuverfolgen, verschiedene Versionen unseres Codes zu speichern und bei Bedarf auf frühere Stände zurückzugreifen. Zudem erleichtert es die Zusammenarbeit im Team, da mehrere Entwickler gleichzeitig am selben Projekt arbeiten und ihre Änderungen zusammenführen können.

Um ein neues Git-Repository zu erstellen, öffnen wir zunächst ein Terminal oder die Eingabeaufforderung und navigieren in das Verzeichnis unseres Projekts. Dort führen wir den Befehl `git init` aus. Dadurch wird ein neues, leeres Repository im aktuellen Ordner angelegt. Anschließend können wir mit `git add .` alle bestehenden Dateien zum Repository hinzufügen und mit `git commit -m "Initial commit"` den ersten Commit erstellen. Optional kann das lokale Repository mit einem entfernten Repository, zum Beispiel auf GitHub oder GitLab, verknüpft werden, um die Dateien online zu speichern und mit anderen zu teilen.

Erst nachdem diese Schritte abgeschlossen sind, können wir mit der weiteren Entwicklung unseres Projekts fortfahren und von den Vorteilen der Versionskontrolle profitieren.
```bash
git init
git add .
git commit - "Initinal commit"
```
Zusätzlich zum lokalen Git-Repository benötigen wir ein GitHub-Repository, um unsere Website zu speichern und online bereitzustellen. Dafür registrieren wir uns bei GitHub und legen ein neues öffentliches Repository an.

Jetzt haben wir alles vorbereitet und können uns auf [[https://themes.gohugo.io/]] ein Theme für unsere Website aussuchen. Hier gibt es viele verschiedne Seiten mit ihren eigenen  möglichkeiten der Konfiguration und Individualisierung.

In diesem Beispiel verwende ich das Theme PaperMod. Die Installation habe ich entsprechend der offiziellen Anleitung des Themes durchgeführt. Jedes Theme verfügt über eine eigene Installationsanleitung, um sicherzustellen, dass alle erforderlichen Komponenten korrekt eingerichtet werden.

## Obsidian
Zum Erstellen meiner Posts verwende ich Obsidian. Dieses leistungsstarke Notiz- und Wissensmanagement-Tool bietet mir eine flexible und übersichtliche Umgebung, um meine Ideen zu sammeln, zu strukturieren und auszuarbeiten. Besonders schätze ich die Möglichkeit, meine Notizen mithilfe von Markdown einfach zu formatieren und miteinander zu verknüpfen. So kann ich meine Gedanken effizient organisieren und jederzeit auf bereits erstellte Inhalte zurückgreifen.

Obsidian unterstützt mich dabei, den gesamten Schreibprozess – von der ersten Skizze bis zum fertigen Post – an einem zentralen Ort zu verwalten. Durch die lokale Speicherung meiner Daten behalte ich die volle Kontrolle über meine Inhalte und kann auch offline problemlos arbeiten. Die Vielzahl an verfügbaren Plugins ermöglicht es mir zudem, Obsidian individuell an meine Bedürfnisse anzupassen und meinen Workflow stetig zu optimieren. Auf diese Weise gelingt es mir, meine Posts strukturiert und effizient zu erstellen.

Damit meine Posts auf der Website landen muss ich Obsidian mit Hugo und Github Synchronisieren. Dazu verwende ich folgende Befehle:
```bash
rsync -av --delete "sourcepath" "destinationpath"
```


> [!Info] Info
> Der Quell Ordner der Posts aus Obsidian kann Herausgefunden werden wenn man einen Rechtsklick auf den Überordner in Obsidian macht. ![[Pasted image 20250621205259.png]]


Um meine Posts besser zu sortieren, füge ich noch einige zusätzliche Informationen hinzu.
```bash
---
title: blogtitle
date: 2024-11-06
draft: false
tags:
  - tag1
  - tag2
---
```

Um Bilder in den Beiträgen zu verwenden, gibt es ein kleines Skript, das die Bilder aus Obsidian mit Hugo synchronisiert. Das Skript wird später vom übergeordneten Skript genutzt, um die Synchronisation aller Bilder durchzuführen.

```bash
import os
import re
import shutil

# Paths
posts_dir = "/Users/networkchuck/Documents/chuckblog/content/posts/"
attachments_dir = "/Users/networkchuck/Documents/neotokos/Attachments/"
static_images_dir = "/Users/networkchuck/Documents/chuckblog/static/images/"

# Step 1: Process each markdown file in the posts directory
for filename in os.listdir(posts_dir):
    if filename.endswith(".md"):
        filepath = os.path.join(posts_dir, filename)
        
        with open(filepath, "r") as file:
            content = file.read()
        
        # Step 2: Find all image links in the format ![Image Description](/images/Pasted%20image%20...%20.png)
        images = re.findall(r'\[\[([^]]*\.png)\]\]', content)
        
        # Step 3: Replace image links and ensure URLs are correctly formatted
        for image in images:
            # Prepare the Markdown-compatible link with %20 replacing spaces
            markdown_image = f"![Image Description](/images/{image.replace(' ', '%20')})"
            content = content.replace(f"[[{image}]]", markdown_image)
            
            # Step 4: Copy the image to the Hugo static/images directory if it exists
            image_source = os.path.join(attachments_dir, image)
            if os.path.exists(image_source):
                shutil.copy(image_source, static_images_dir)

        # Step 5: Write the updated content back to the markdown file
        with open(filepath, "w") as file:
            file.write(content)

print("Markdown files processed and images copied successfully.")
```


