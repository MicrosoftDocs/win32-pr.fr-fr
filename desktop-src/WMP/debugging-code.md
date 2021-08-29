---
title: Débogage du code
description: Débogage du code
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- apparences de Lecteur Windows Media, code de débogage
- apparences, débogage de code
- débogage de code pour les apparences
- apparences de Lecteur Windows Media, journalisation
- apparences, journalisation
- fonctionnalité de journalisation dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d0d8be81c22d06c5d25fa5a3fd33dc17080f0f7851fdfbcb656a3fd99e0854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863589"
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



par exemple, si vous souhaitez voir la position actuelle du contenu multimédia numérique dans Lecteur Windows Media, vous pouvez utiliser du code semblable au suivant pour afficher la position actuelle dans la zone de texte.


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

lorsque la journalisation est activée et que vous avez installé un système de développement qui fournit des fonctionnalités de débogage (par exemple, Microsoft Visual Studio), les exceptions qui ne sont pas gérées par votre code de script entraînent l’ouverture d’une boîte de dialogue d’avertissement du débogueur pour chaque exception. Il s’agit d’une fonctionnalité utile pour vous aider à déboguer votre code de script. en outre, vous pouvez attacher manuellement le processus Lecteur Windows Media à votre débogueur lorsque la journalisation est activée.

Ce kit de développement logiciel (SDK) comprend un exemple d’apparence, appelé « journalisation », qui illustre la fonctionnalité de journalisation dans les apparences. Pour en savoir plus sur l’utilisation des exemples, consultez [exemples](samples.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des apparences**](about-skins.md)
</dt> </dl>

 

 




