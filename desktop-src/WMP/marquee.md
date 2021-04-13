---
title: Chapiteau
description: Chapiteau
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Windows Media Player Mobile Skins, palissades
- apparences, rectangles de sélection
- informations de référence sur les habillages, les cadres
- textes défilant dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380174"
---
# <a name="marquee"></a>Chapiteau

Un texte défilant est une zone de texte déroulante qui affiche des informations à partir d’une ou plusieurs zones d’affichage de texte. Vous n’avez pas besoin d’ajouter un texte défilant, mais cela peut s’avérer très utile lorsque vous avez des informations détaillées que vous souhaitez afficher à l’utilisateur dans un espace limité.

Le texte dans le texte défilant défile uniquement si les deux conditions suivantes sont remplies :

-   Vous avez plus de texte à afficher dans le texte défilant que la largeur de la zone d’affichage du texte défilant.
-   L’élément multimédia est arrêté ou suspendu.

La section de texte défilant du fichier de définition d’apparence doit commencer par cette ligne :


```C++
[ Marquee ]

```



> [!Note]  
> Pour assurer la compatibilité avec les versions de Windows Media Player Mobile antérieures à Windows Media Player 10 mobile, l’utilisation de « marquis » dans un fichier de définition d’apparence est toujours considérée comme valide.

 

Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacune des zones d’affichage de texte défilant dans votre apparence.


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



Vous pouvez utiliser le modèle suivant pour la section marquee de votre fichier de définition d’apparence :


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



Vous devez utiliser l’ordre suivant pour obtenir des informations dans chaque ligne de la section marquee (chaque partie de la ligne est requise) :

1.  [Emplacement du texte défilant](marquee-location.md)
2.  [Police du texte défilant](marquee-font.md)
3.  [Couleur du texte défilant](marquee-color.md)
4.  [Combinaisons de texte](text-combinations.md)

Pour obtenir un exemple de code de texte défilant, consultez la [section exemple de texte défilant](sample-marquee-section.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




