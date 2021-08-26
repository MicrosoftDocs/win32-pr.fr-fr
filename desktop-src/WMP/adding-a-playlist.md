---
title: Ajout d’une sélection
description: Ajout d’une sélection
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- création d’apparences, de sélections
- apparences de Lecteur Windows Media, sélections
- apparences, sélections
- sélections, habillages
- sélections de métafichiers, apparences
- Windows Sélections de métafichiers multimédias, habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23d9198f1f913b83cef40cea9f6ec47976f9f1e08a5e54257ab16df63e538b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031589"
---
# <a name="adding-a-playlist"></a>Ajout d’une sélection

Vous pouvez utiliser les sélections pour choisir parmi les collections de vos données audio et vidéo.

À l’aide de l’illustration de votre première apparence, vous pouvez apporter quelques modifications au fichier de définition d’apparence.

La première étape consiste à utiliser l’interpréteur de commandes que vous allez utiliser pour la plupart des habillages :


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



Ajoutez maintenant une deuxième **vue**, qui contient une sélection. Placez le code suivant après le </VIEW> du code Shell.


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



Vous devez donner à cette deuxième vue un ID pour pouvoir vous y référer ultérieurement. Ajoutez un PLAYELEMENT et un STOPELEMENT. Ces boutons prédéfinis facilitent la vie.


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



Enfin, ajoutez un événement onClick à PLAYELEMENT pour afficher une sélection dans la deuxième vue :


```C++
            onClick = "JScript: theme.openView('playview');" />

```



Vous pouvez voir une apparence de sélection de travail similaire dans la section exemple du kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de création d’apparence**](skin-creation-guide.md)
</dt> </dl>

 

 




