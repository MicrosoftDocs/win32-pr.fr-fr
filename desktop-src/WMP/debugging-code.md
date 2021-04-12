---
title: Débogage du code
description: Débogage du code
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Apparences du lecteur Windows Media, code de débogage
- apparences, débogage de code
- débogage de code pour les apparences
- Apparences du lecteur Windows Media, journalisation
- apparences, journalisation
- fonctionnalité de journalisation dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311057"
---
# <a name="debugging-code"></a>Débogage du code

Vous voudrez souvent voir ce qui se passe dans votre apparence. Pour ce faire, vous pouvez utiliser un contrôle de texte ou un fichier journal.

Vous pouvez créer un élément de **texte** et le placer temporairement sur une partie de votre apparence. Par exemple, vous pouvez utiliser le code suivant pour créer votre élément de **texte** :


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



Par exemple, si vous souhaitez voir la position actuelle du contenu multimédia numérique dans le lecteur Windows Media, vous pouvez utiliser du code semblable au suivant pour afficher la position actuelle dans la zone de texte.


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a>Pour écrire des informations de débogage dans un fichier journal

Pour activer ou désactiver le débogage, modifiez la valeur de la clé de Registre suivante :

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ MediaPlayer \\ Preferences \\ ScriptDebugging**

Lorsque vous définissez la valeur sur 1, la journalisation est activée. Lorsque vous affectez la valeur 0 (valeur par défaut), la journalisation est désactivée.

Si la journalisation est activée, un fichier est placé sur l’ordinateur de l’utilisateur dans le même dossier que l’apparence. Le fichier est nommé «*filename* \_ 0 \_log.txt », où *filename* est le nom du fichier d’apparence. Le code de votre apparence peut écrire du texte dans ce fichier à l’aide du *thème*. méthode **logString** . Cela peut être utile si vous souhaitez déterminer ce qui se passe dans votre code pendant qu’il est en cours d’exécution. Notez que le fichier texte est encodé à l’aide de caractères Unicode.

Lorsque la journalisation est activée et que vous avez installé un système de développement qui fournit des fonctionnalités de débogage (par exemple, Microsoft Visual Studio), les exceptions qui ne sont pas gérées par votre code de script entraînent l’ouverture d’une boîte de dialogue d’avertissement du débogueur pour chaque exception. Il s’agit d’une fonctionnalité utile pour vous aider à déboguer votre code de script. En outre, vous pouvez attacher manuellement le processus du lecteur Windows Media à votre débogueur lorsque la journalisation est activée.

Ce kit de développement logiciel (SDK) comprend un exemple d’apparence, appelé « journalisation », qui illustre la fonctionnalité de journalisation dans les apparences. Pour en savoir plus sur l’utilisation des exemples, consultez [exemples](samples.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des apparences**](about-skins.md)
</dt> </dl>

 

 




