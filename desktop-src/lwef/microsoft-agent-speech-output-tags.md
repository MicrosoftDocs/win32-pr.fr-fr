---
title: Balises de sortie vocale Microsoft Agent
description: Balises de sortie vocale Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27add35cc9be72a002cdb1a6fba60ef61d47cca61ef532a6d80fd6ed4a5794d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747885"
---
# <a name="microsoft-agent-speech-output-tags"></a>Balises de sortie vocale Microsoft Agent

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Les services Microsoft Agent prennent en charge la modification de la sortie vocale par le biais de balises spéciales insérées dans la chaîne de texte vocal. Ces balises vous aident à modifier les caractéristiques de l’expression de sortie du caractère.

Les balises de sortie vocale utilisent les règles de syntaxe suivantes :

-   Toutes les balises commencent et se terminent par une barre oblique inverse ( \\ ).
-   La barre oblique inverse unique n’est pas activée dans une balise. Pour inclure une barre oblique inverse dans un paramètre de texte d’une balise, utilisez une double barre oblique inverse ( \\ \\ ).
-   Les balises ne respectent pas la casse. Par exemple, \\ Pit \\ est le même que \\ Pit \\ .
-   Les balises sont dépendantes des espaces blancs. Par exemple, \\ RST \\ n’est pas le même \\ que \\ RST.

Sauf indication contraire ou modification par une autre balise, la sortie vocale conserve la caractéristique définie par la balise dans le texte spécifié dans une méthode [**Speak**](speak-method.md) unique. La sortie vocale est automatiquement réinitialisée via les paramètres définis par l’utilisateur après la fin d’une méthode **Speak** .

Certaines balises incluent des chaînes entre guillemets. pour certains langages de programmation, tels que Visual Basic scripting Edition (VBScript) et Visual Basic, cela signifie que vous devrez peut-être utiliser deux guillemets pour désigner le paramètre de la balise ou concaténer un guillemet double comme faisant partie de la chaîne. ce dernier s’affiche dans cet exemple de Visual Basic :


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Pour la programmation en C, C++ et Java™, faites précéder les barres obliques inverses et les guillemets doubles d’une barre oblique inverse. Par exemple :


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



Pour les langues étrangères qui prennent en charge les caractères DBCS (Double-Byte Character Set), vous pouvez utiliser des caractères codés sur deux octets pour spécifier des paramètres de chaîne. Toutefois, utilisez des caractères codés sur un octet pour tous les autres paramètres et caractères utilisés pour définir la balise, y compris l’étiquette elle-même.

Les balises suivantes sont prises en charge :

-   [**Chr**](chr-tag.md)
-   [**CTX**](ctx-tag.md)
-   [**Renseignements**](emp-tag.md)
-   [**LST**](lst-tag.md)
-   [**Canal**](map-tag.md)
-   [**Mrk**](mrk-tag.md)
-   [**Pau**](pau-tag.md)
-   [**Compose**](pit-tag.md)
-   [**RST**](rst-tag.md)
-   [**SPD**](spd-tag.md)
-   [**Vol**](vol-tag.md)

Les balises sont principalement conçues pour ajuster la sortie générée par la conversion de texte par synthèse vocale (TTS). Seules les balises [**MRK**](mrk-tag.md) et [**Map**](map-tag.md) peuvent être utilisées avec une sortie orale basée sur des fichiers audio.

> [!Note]  
> Microsoft Agent ne prend pas en charge toutes les balises documentées dans le kit de développement logiciel (SDK) Microsoft Speech. Les paramètres peuvent également varier en fonction du moteur TTS sélectionné. Vous pouvez définir un moteur TTS spécifique à l’aide de [**TTSModeID**](ttsmodeid-property.md).

 

 

 




