---
title: Avertissement de la table de données ARIA
description: Avertissement de la table de données ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029732"
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



 

 




