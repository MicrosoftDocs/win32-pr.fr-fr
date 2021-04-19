---
title: Accès à un moteur de reconnaissance vocale dans votre code
description: Accès à un moteur de reconnaissance vocale dans votre code
ms.assetid: ddfe0552-a29e-4ce4-b608-c131efbe300b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d81841f6f287d36a6ac01fa77294b1754eeb9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512724"
---
# <a name="accessing-a-speech-engine-in-your-code"></a>Accès à un moteur de reconnaissance vocale dans votre code

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Pour utiliser un moteur de reconnaissance vocale particulier dans votre code, utilisez l’API de l’agent pour définir le moteur. Pour les moteurs d’entrée vocales, utilisez [**SRModeID**](https://www.bing.com/search?q=**SRModeID**), en spécifiant l’ID de mode du moteur. Toutefois, Notez que le moteur doit être installé. Pour déterminer si le moteur est présent, vous pouvez interroger **SRModeID**. Le moteur doit correspondre au paramètre [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) du caractère. Par exemple, vous ne pouvez pas définir **SRModeID** sur un ID de mode du moteur de reconnaissance vocale en allemand pour un caractère dont la valeur de **LanguageID** est le français.

**ID du mode du moteur d’entrée vocal**



| Voix                                    | ID de mode                             |
|------------------------------------------|--------------------------------------|
| Moteur de reconnaissance vocale Microsoft v 4.0 | {D8905400-B5C8-11D0-B968020AFDB1B9C} |



 

Vérifiez et définissez les paramètres [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) et [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) du caractère dans votre code avant de tenter de définir la grammaire pour les paramètres vocaux des objets de **commande** de votre application. Pensez également à vérifier la langue du navigateur ou du système pour être certain de correspondre à la configuration de vos utilisateurs. Le moteur peut échouer si vous tentez de définir une grammaire pour une langue qui ne correspond pas au moteur.

Un jeu de caractères pour la sortie TTS (Text-to-Speech) peut être compilé avec une préférence d’ID de mode par défaut du moteur de sortie vocale. Lorsque le caractère est chargé, si le moteur est installé et correspond au [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)du caractère, l’agent tente de charger cet ID de mode pour la sortie vocale. Si le moteur n’est pas présent ou a un **LanguageID** différent, l’agent tente de charger le premier ID de mode qu’il trouve et qui correspond à l’identificateur de **langue** du caractère, mais définit toujours le paramètre de vitesse et de hauteur de la compilation du caractère.

Notez que puisque tous les caractères fournis par Microsoft Agent sont compilés pour utiliser le moteur de synthèse vocale Lernout & Hauspie TruVoice, en tant que moteur de sortie vocale par défaut, les paramètres de vitesse et de tonalité des caractères sont réglés pour cette langue et ce moteur. Par conséquent, lors de l’utilisation d’autres moteurs TTS ou de moteurs d’autres langues, les caractères peuvent ne pas se prononcer à la tonalité ou à la vitesse optimale. Bien que votre application ou page Web ne puisse pas [**écrire les valeurs de propriété de pas**](/previous-versions/ms809428(v=msdn.10)) et de [**Vitesse**](https://www.bing.com/search?q=**Speed**) , vous pouvez inclure des balises [Pit](pit-tag.md) (pas) et [SPD](spd-tag.md) (vitesse) dans votre texte de sortie qui modifient temporairement le pas et la vitesse pour une énoncé particulière. Toutefois, l’utilisation des balises Pit et SPD ne modifiera **pas les propriétés de pas** et de **Vitesse** . Pour plus d’informations, consultez [programmation du contrôle Microsoft Agent](programming-the-microsoft-agent-control.md) et des [balises de sortie vocale Microsoft Agent](microsoft-agent-speech-output-tags.md) .

Vous devez également installer SAPI 4.0 en tant que fichiers binaires d’exécution (SPCHAPI.exe) lors de l’utilisation d’autres moteurs TTS compatibles SAPI que le moteur de L&H TruVoice American English avec les caractères Microsoft Agent fournis pour que les moteurs soient énumérés correctement. À partir de votre page Web, incluez la balise d’objet suivante pour installer automatiquement le composant :

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Pour rechercher ou définir l’ID de mode d’un moteur, utilisez [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**). Avec **TTSModeID** , vous pouvez définir un ID de mode différent de l’identificateur de [**langue**](https://www.bing.com/search?q=**LanguageID**)du caractère. Par exemple, vous pouvez définir un caractère allemand pour parler à l’aide d’un ID en mode français. Les ID de mode du moteur de sortie vocale définissent non seulement le moteur que vous utilisez, mais également les voix spécifiques prises en charge pour un moteur. Vous pouvez également utiliser l’éditeur de caractères Microsoft agent ou les outils inclus dans la [documentation du kit de développement logiciel (SDK) Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx) pour demander les ID de mode des moteurs TTS installés sur votre système.

**ID du mode de sortie vocale**



| Voix                                       | ID de mode                               |
|---------------------------------------------|----------------------------------------|
| Adulte femelle \# 1, anglais des États-Unis, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273008} |
| Adulte femelle \# 2, anglais des États-Unis, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273009} |
| Adulte masculin \# 1, anglais des États-Unis, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273000} |
| Adulte masculin \# 2, anglais des États-Unis, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273001} |
| Adulte mâle \# 3, anglais des États-Unis, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273002} |
| Adulte masculin \# 4, anglais des États-Unis, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273003} |
| Adulte masculin \# 5, anglais des États-Unis, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273004} |
| Adulte masculin \# 6, anglais des États-Unis, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273005} |
| Adulte masculin \# 7, anglais des États-Unis, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273006} |
| Adulte masculin \# 8, anglais des États-Unis, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273007} |
| Carol, anglais britannique, L&H TTS3000         | {227A0E40-A92A-11d1-B17B-0020AFED142E} |
| Peter, anglais britannique, L&H TTS3000         | {227A0E41-A92A-11d1-B17B-0020AFED142E} |
| Linda, néerlandais, L&H TTS3000                   | {A0DDCA40-A92C-11d1-B17B-0020AFED142E} |
| Alexander, néerlandais, L&H TTS3000               | {A0DDCA41-A92C-11d1-B17B-0020AFED142E} |
| Véronique, français, L&H TTS3000              | {0879A4E0-A92C-11d1-B17B-0020AFED142E} |
| Pierre, français, L&H TTS3000                 | {0879A4E1-A92C-11d1-B17B-0020AFED142E} |
| Anna, allemand, L&H TTS3000                   | {3A1FB760-A92B-11d1-B17B-0020AFED142E} |
| Stefan, allemand, L&H TTS3000                 | {3A1FB761-A92B-11d1-B17B-0020AFED142E} |
| Barbara, italien, L&H TTS3000               | {7EF71700-A92D-11d1-B17B-0020AFED142E} |
| Stefano, italien, L&H TTS3000               | {7EF71701-A92D-11d1-B17B-0020AFED142E} |
| Naoko, Japanese, L&H TTS3000                | {A778E060-A936-11d1-B17B-0020AFED142E} |
| Kenji, Japanese, L&H TTS3000                | {A778E061-A936-11d1-B17B-0020AFED142E} |
| Chine-Ah, coréen, L&H TTS3000                | {12E0B720-A936-11d1-B17B-0020AFED142E} |
| Juin-Ho, coréen, L&H TTS3000                 | {12E0B721-A936-11d1-B17B-0020AFED142E} |
| Juliana, portugais (Brésil), L&H TTS3000   | {8AA08CA0-A1AE-11d3-9BC5-00A0C967A2D1} |
| Alexandre, portugais (Brésil), L&H TTS3000 | {8AA08CA1-A1AE-11d3-9BC5-00A0C967A2D1} |
| Svetlana, russe, L&H TTS3000              | {06377F80-D48E-11d1-B17B-0020AFED142E} |
| Boris, russe, L&H TTS3000                 | {06377F81-D48E-11d1-B17B-0020AFED142E} |
| Carmen, espagnol, L&H TTS3000                | {2CE326E0-A935-11d1-B17B-0020AFED142E} |
| Julio, espagnol, L&H TTS3000                 | {2CE326E1-A935-11d1-B17B-0020AFED142E} |



 

> [!Note]  
> Il existe une différence entre le CLSID d’installation d’un moteur de reconnaissance vocale et son ID de mode. De même, un moteur de reconnaissance vocale a également un ID de moteur, mais cet ID n’est pas applicable dans l’API de l’agent.

 

 

 