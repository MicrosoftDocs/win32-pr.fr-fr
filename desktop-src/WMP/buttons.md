---
title: boutons (kit de développement logiciel Lecteur Windows Media)
description: Boutons
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Lecteur Windows Media Skins mobiles, vue d’ensemble du bouton
- apparences, vue d’ensemble du bouton
- informations de référence sur les apparences, les boutons
- boutons dans des apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128c723c5b8bbac31c82a32060704bc892dfb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855622"
---
# <a name="buttons-windows-media-player-sdk"></a>boutons (kit de développement logiciel Lecteur Windows Media)

Vous pouvez utiliser un ou plusieurs boutons dans votre apparence, et chaque bouton doit être défini dans le fichier de définition d’apparence. Si vous ne définissez pas de bouton dans cette section, votre apparence ne sera pas en mesure de l’utiliser.

La section Buttons du fichier de définition d’apparence commence par cette ligne :


```C++
[ Buttons ]

```



Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacun des boutons de votre apparence. Une ligne classique peut être :


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



Notez que ce code doit être tapé sous la forme d’une ligne commençant par « PlayPause » et se terminant par « push @ 160, 98 ».

Vous pouvez utiliser le modèle suivant pour la section de bouton de votre fichier de définition d’apparence :


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



Là encore, Notez qu’elles doivent être de type ligne unique, la première commençant par la fonction « // &lt; Function &gt; » et se terminant par « &lt; Push 2 image SRC &gt; ». La deuxième ligne commence par « //---------- » et se termine par « ------------------. ».

Les informations de bouton pour chaque ligne dans la section du bouton doivent apparaître dans l’ordre suivant. Seules les six premières parties de la ligne sont requises. Les images secondaires ne sont pas incluses, sauf si elles sont nécessaires.

1.  [Button, fonction](button-function.md)
2.  [Type de bouton](button-type.md)
3.  [Emplacement du bouton](button-location.md)
4.  [Source de l’image Push](pushed-image-source.md)
5.  [Source de l’image pour le bouton désactivé](image-source-for-disabled-button.md)
6.  [Toucher la couleur RVB](hit-rgb-color.md)
7.  [Source d’image secondaire normale](normal-secondary-image-source.md)
8.  [Source d’image tertiaire normale](normal-tertiary-image-source.md)
9.  [Source d’image secondaire faisant l’objet d’un push](pushed-secondary-image-source.md)
10. [Source d’image tertiaire envoyée](pushed-tertiary-image-source.md)

Pour obtenir un exemple de code de bouton, consultez la [section exemple de bouton](sample-button-section.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




