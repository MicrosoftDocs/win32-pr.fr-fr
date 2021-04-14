---
title: Erreur de table de données ARIA
description: Erreur de table de données ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383103"
---
# <a name="aria-data-table-error"></a>Erreur de table de données ARIA

## <a name="text"></a>Texte

La table contient des données, mais n’a pas de balise accessible définie via **les éléments Aria-label**, **aria-labelledby**, **title**, **Caption** ou **th** .

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Cette erreur s’applique aux tableaux HTML comportant plusieurs cellules. Cette erreur ne s’applique pas aux tables avec `role="presentation"` , car celles-ci sont considérées comme des tables de disposition.

Cette erreur indique qu’une table de données n’a pas de nom accessible ou d’informations d’en-tête.

Pour corriger cette erreur, définissez un nom accessible à l’aide de la balise [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , ou des attributs [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)ou [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) . S’il manque des informations d’en-tête dans la table, utilisez des balises [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) pour marquer les cellules d’en-tête.

## <a name="example"></a>Exemple


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




