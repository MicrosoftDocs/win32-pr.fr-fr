---
title: Avertissement de la table de données ARIA
description: Avertissement de la table de données ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fb9e8e97336199b5b133dc59ef7c5f0900f7bdeb0c7a8d8098a51707b107f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122389"
---
# <a name="aria-data-table-warning"></a>Avertissement de la table de données ARIA

## <a name="text"></a>Texte

La table contient des données, mais n’a pas de résumé ni d’attribut **Aria-DescribedBy** valide.

## <a name="type"></a>Type

Avertissement

## <a name="description"></a>Description

Cet avertissement s’applique aux tableaux HTML contenant plusieurs cellules. Elle ne s’applique pas aux tables avec `role="presentation"` , car celles-ci sont considérées comme des tables de disposition.

Cet avertissement indique que la table est identifiée comme une table de données, mais qu’aucune description accessible n’est définie.

> [!Note]  
> Toutes les tables de données n’ont pas besoin d’une description accessible. Vous devez définir une description accessible si les utilisateurs ont besoin d’informations supplémentaires pour comprendre la structure et le contenu de la table de données.

 

Pour résoudre cet avertissement, définissez une description accessible à partir d’une table à l’aide de l’attribut Summary ou de l’attribut **Aria-DescribedBy** .

## <a name="example"></a>Exemple


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




