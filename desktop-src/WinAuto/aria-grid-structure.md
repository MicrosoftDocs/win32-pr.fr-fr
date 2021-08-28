---
title: Erreur de structure de grille ARIA
description: Erreur de structure de grille ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b91010417ed01f211859839ceab124b299b10679b3d460f860c03e5b2473f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122379"
---
# <a name="aria-grid-structure-error"></a>Erreur de structure de grille ARIA

## <a name="text"></a>Texte

L’élément avec le rôle de **grille** n’est pas associé à une structure de grille ou à un balisage accessible.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Cette erreur s’applique aux éléments personnalisés dont l’attribut **role** a la valeur « Grid ». Elle ne s’applique pas aux balises de table HTML qui ont un **rôle** implicite « Grid ».

Un élément dont l’attribut de **rôle** est défini sur « Grid » doit avoir la structure définie par le rôle de grille WAI-ARIA (initiative d’accessibilité Web-accessible riches Internet applications), y compris le nom accessible pour la grille et ses sous-éléments d’en-tête.

Pour corriger cette erreur, examinez votre implémentation pour vous assurer qu’elle est conforme à la spécification WAI-ARIA. En particulier, vérifiez que la structure respecte les règles suivantes.

-   **Grid** contient des éléments **Row** ou **rowgroup** .
-   **rowgroup** contient des éléments de **ligne** .
-   les éléments **Row** contiennent les éléments **ColumnHeader** , **GridCell** ou **RowHeader** .

Un nom accessible doit être défini pour les éléments **Grid**, **ColumnHeader**, **GridCell** et **RowHeader** à l’aide de l’un des attributs suivants.

-   attribut [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) permettant de référencer l’élément contenant du texte.
-   attribut [**Aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) pour définir directement le nom accessible.
-   [**titre**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) pour la création d’une info-bulle qui est utilisée en même temps que le nom.

 

 




