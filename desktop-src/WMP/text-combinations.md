---
title: Combinaisons de texte
description: Combinaisons de texte
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Lecteur Windows Media Habillages mobiles, rectangles de sélection
- apparences, rectangles de sélection
- informations de référence sur les habillages, les cadres
- textes défilant dans les apparences, combinaisons de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520617"
---
# <a name="text-combinations"></a>Combinaisons de texte

Cette valeur est une liste de combinaisons de zones d’affichage de texte, séparées par des virgules. Les zones d’affichage de texte peuvent être jointes par un caractère plus pour créer une nouvelle valeur d’affichage de texte défilant et tout type de texte défini dans la section type de texte peut être utilisé dans votre texte défilant.

lorsque vous déterminez ce qui doit être affiché, Lecteur Windows Media Mobile évalue chaque élément de la liste pour voir si toutes les parties sont disponibles. Si ce n’est pas le cas, l’élément suivant est évalué, et ainsi de suite, jusqu’à ce que toutes les parties disponibles aient été trouvées. Par exemple, si vous souhaitez afficher l’auteur et le titre, mais que vous ne savez pas si les deux sont disponibles, utilisez la valeur suivante :


```C++
Title+Author, Title, Author

```



Dans l’exemple précédent, le titre et l’auteur s’affichent si le titre et l’auteur ont été définis pour l’élément multimédia. Si les deux ne sont pas définis, le titre est évalué et affiché s’il est défini. Si le titre n’est pas défini, l’auteur est affiché s’il est défini. Si aucun n’est défini, rien ne s’affiche.

Lorsque vous utilisez le signe plus pour la concaténation, veillez à ne pas avoir d’espaces de part et d’autre du signe plus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Chapiteau**](marquee.md)
</dt> <dt>

[**Type de texte**](text-type.md)
</dt> </dl>

 

 




