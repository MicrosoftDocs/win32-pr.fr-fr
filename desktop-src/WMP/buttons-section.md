---
title: Section boutons
description: Section boutons
ms.assetid: fa413bb4-e04a-4e3d-9754-cd4c2d82de6e
keywords:
- Apparences mobiles du lecteur Windows Media, section boutons
- apparences, section boutons
- création d’apparences, section de boutons
- écriture de code pour les apparences, section Buttons
- boutons dans la section apparences, boutons
- fichiers de définition d’apparence, section boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f994225154e3f4cc55070351c32c654d5ad616c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029430"
---
# <a name="buttons-section"></a>Section boutons

Ensuite, vous devez définir les boutons que vous allez utiliser :


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   100,20,110,100 Pushed @ 100,20   Disabled @ 100,20    0,255,255  Pushed @ 270,20     Pushed @ 270,130
    Stop       PushHit    20,20,45,45    Pushed @ 20,20    Disabled @ 20,20   255,255,  0
    Next       PushHit    20,80,45,45    Pushed @ 20,80    Disabled @ 20,80   255,  0,  0
    Prev       PushHit    20,140,45,45   Pushed @ 20,140   Disabled @ 20,130    0,  0,255

```



Quatre boutons sont définis dans cette section. La page que vous affichez peut encapsuler ces lignes, mais lorsque vous tapez dans le code, vous ne devez pas encapsuler les lignes ; autrement dit, chaque ligne doit être terminée et se terminer par une marque de paragraphe.

> [!Note]  
> Les types de boutons sont déconseillés dans le lecteur Windows Media 10 mobile ou les apparences ultérieures. Au lieu d’un type de bouton déclaré dans votre fichier d’apparence, entrez « NA » pour chaque type.

 

Pour chaque bouton, vous devez définir la fonction, le type, l’emplacement, la source de l’image Poussée, la source désactivée et la couleur (pour les boutons de type d’accès). En outre, pour le bouton PlayPause, vous devez définir les sources d’image normales et Push pour l’état suspendu.

Pour plus d’informations sur la section Buttons du fichier de définition d’apparence, consultez [boutons](buttons.md) dans la référence de l’apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture du code**](writing-the-code.md)
</dt> </dl>

 

 




