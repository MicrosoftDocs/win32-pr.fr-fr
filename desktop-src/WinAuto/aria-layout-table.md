---
title: Erreur de table de présentation ARIA
description: Erreur de table de présentation ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896c7ec4061119535ed544cfc41598c1387d98011eb275f6a0345d9334a7dc9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122282"
---
# <a name="aria-presentation-table-error"></a>Erreur de table de présentation ARIA

## <a name="text"></a>Texte

La table utilisée pour la disposition ne doit pas avoir d’en-tête, de nom accessible ou d’informations de résumé définis (**th**, **Summary**, **Aria-DescribedBy**, **aria-labelledby**, **Aria-label**, **titre**, attributs de **légende** ).

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Cette erreur s’applique aux balises de table HTML dont l’attribut [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) a la valeur « Presentation », ou à une table comportant une seule cellule (table 1 × 1).

Cette erreur indique qu’une table est marquée en tant que disposition uniquement (has `role="presentation"` ), mais elle contient également des informations d’accessibilité comme s’il s’agissait d’une table de données, ce qui peut prêter à confusion pour les utilisateurs de lecteur d’écran.

Pour résoudre cette erreur, déterminez si la table est simplement une table de disposition et, le cas échéant, supprimez le balisage accessible :

-   Attribut [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)ou [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .
-   attributs [**Summary**](https://www.bing.com/search?q=**summary**) ou [**Aria-DescribedBy**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .
-   Balises [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .

## <a name="example"></a>Exemple

![html pour un élément table, avec des attributs tels que le résumé qui déclenche l’erreur de table de présentation Aria affichée comme balise HTML barrée ](images/aria-layout-table.png)

## <a name="remarks"></a>Remarques

Si vous déterminez qu’une table a besoin d’informations d’accessibilité, supprimez l’attribut de [**rôle**](https://developer.mozilla.org/docs/Web/HTML/Reference) ou affectez-lui une valeur autre que « Presentation ».

 

 




