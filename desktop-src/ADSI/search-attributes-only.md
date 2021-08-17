---
title: Rechercher des attributs uniquement
description: Parfois, vous effectuez une recherche pour déterminer le type de données disponibles pour un objet.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Attributs de recherche uniquement ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b1775c759975a508f5382ef2a30f290ac4a96b3b92120d4face6b1d0556426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443929"
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
-   [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 




