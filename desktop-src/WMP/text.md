---
title: texte (Lecteur Windows Media SDK)
description: Texte
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Lecteur Windows Media Skins mobiles, texte
- apparences, texte
- informations de référence sur les apparences, le texte
- texte dans les enveloppes, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55027415222516e72df61afab01a14cceb503528467bf329264014c94bf31ed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118097"
---
# <a name="text-windows-media-player-sdk"></a>texte (Lecteur Windows Media SDK)

Vous souhaiterez peut-être utiliser une ou plusieurs zones d’affichage de texte dans votre apparence. Chaque zone d’affichage de texte que vous utilisez doit être définie dans le fichier de définition d’apparence. Si vous ne définissez pas de zone d’affichage de texte dans cette section, votre apparence ne sera pas en mesure de l’utiliser.

La section de texte du fichier de définition d’apparence commence par cette ligne :


```C++
[ Text ]

```



Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacune des zones d’affichage de texte dans votre apparence.


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



Vous pouvez utiliser le modèle suivant pour la section de texte de votre fichier de définition d’apparence :


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



Vous devez utiliser l’ordre indiqué dans le modèle précédent pour obtenir des informations sur la zone d’affichage de texte pour chaque ligne de la section de texte. Chaque partie de la ligne est requise. Les sections suivantes décrivent chaque élément en détail.

1.  [Type de texte](text-type.md)
2.  [Emplacement du texte](text-location.md)
3.  [Alignement du texte](text-alignment.md)
4.  [Police du texte](text-font.md)
5.  [Couleur du texte](text-color.md)

Pour obtenir un exemple de code de texte, consultez la [section exemple de texte](sample-text-section.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




