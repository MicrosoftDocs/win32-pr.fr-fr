---
title: Propriété Value
description: La propriété valeur fournit une représentation textuelle des informations visuelles contenues dans un objet. Tous les objets ne prennent pas en charge la propriété Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412205"
---
# <a name="value-property"></a>Propriété Value

La propriété **valeur** fournit une représentation textuelle des informations visuelles contenues dans un objet. Tous les objets ne prennent pas en charge la propriété **value** .

La propriété **value** est récupérée en appelant [**IAccessible :: \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

La propriété **valeur** indique au client les informations visuelles contenues dans un objet. Par exemple, la valeur d’un contrôle d’édition est le texte qu’il contient, alors qu’un élément de menu n’a pas de valeur.

## <a name="providing-hierarchical-information"></a>Fournir des informations hiérarchiques

La propriété **value** fournit des informations hiérarchiques dans les cas tels qu’un contrôle Tree View. Bien que l’objet parent dans le contrôle TreeView ne fournisse pas d’informations dans la propriété **value** , chaque élément du contrôle a une valeur de base zéro qui représente son niveau dans la hiérarchie. Les éléments de niveau supérieur ont une valeur de zéro, les éléments de second niveau ont la valeur un, et ainsi de suite.

 

 




