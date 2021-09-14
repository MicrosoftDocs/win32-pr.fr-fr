---
title: Code complet pour la peau simple
description: Code complet pour la peau simple
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- créer des apparences, des exemples de code
- apparences de Lecteur Windows Media, exemples de code
- apparences, exemples de code
- fichiers de définition d’apparence, exemples de code
- création d’apparences, exemples
- skins Lecteur Windows Media, exemples
- Skins, exemples
- fichiers de définition d’apparence, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919400"
---
# <a name="complete-code-for-simple-skin"></a>Code complet pour la peau simple

Voici le code complet pour le premier exemple d’apparence :


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



Vous avez maintenant tous les éléments réunis.

Créez un fichier compressé avec une extension de nom de fichier .zip. Ce fichier compressé contient votre fichier de définition d’apparence, vos bitmaps et tous les fichiers multimédias numériques que vous souhaitez inclure. Renommez le fichier afin qu’il ait une extension de nom de fichier. WMZ. Ensuite, double-cliquez sur l’apparence compressée pour la lancer.

Vous pouvez voir une apparence simple de travail similaire dans la section exemples du kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du fichier de définition d’apparence**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




