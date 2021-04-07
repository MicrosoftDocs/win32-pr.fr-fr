---
title: Rechercher des attributs uniquement
description: Parfois, vous effectuez une recherche pour déterminer le type de données disponibles pour un objet.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Attributs de recherche uniquement ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939579"
---
# <a name="search-attributes-only"></a>Rechercher des attributs uniquement

Parfois, vous effectuez une recherche pour déterminer le type de données disponibles pour un objet. Dans ce cas, vous vous intéressez uniquement aux attributs, et non aux valeurs, de l’objet. Pour ce faire, vous devez définir l’option « Rechercher les attributs uniquement ». La spécification de cette option retourne les noms des attributs sans leurs valeurs. Toutefois, le jeu de résultats comprend uniquement les attributs qui ont des valeurs affectées. Par exemple, considérez un objet avec les attributs suivants :

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

Lorsque l’option Rechercher uniquement les attributs est définie, le jeu de résultats comprend les éléments suivants :

``` syntax
First Name
Last Name
Phone Number
```

Pour plus d’informations sur l’utilisation de l’option Rechercher des attributs uniquement avec une interface de recherche spécifique, consultez :

-   [Retour uniquement des noms d’attributs avec IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)
-   [Recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 




