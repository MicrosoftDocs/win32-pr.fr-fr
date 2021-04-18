---
title: Retour uniquement des noms d’attributs avec IDirectorySearch
description: Vous pouvez effectuer une recherche pour déterminer le type de données disponibles pour un objet particulier.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Retour uniquement des noms d’attributs avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, en retournant uniquement les noms d’attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509362"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Retour uniquement des noms d’attributs avec IDirectorySearch

Vous pouvez effectuer une recherche pour déterminer le type de données disponibles pour un objet particulier. Dans ce cas, vous vous intéressez uniquement aux noms d’attributs, et non aux valeurs d’attribut de l’objet. L’option **ad \_ SEARCHPREF \_ ATTRIBTYPES \_ only** indique au serveur de retourner uniquement les noms d’attributs et non les valeurs d’attribut. Toutefois, le jeu de résultats comprend uniquement les attributs qui ont des valeurs affectées. Par exemple, considérez un objet avec les attributs suivants :

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Lorsque l’option **ad \_ SEARCHPREF \_ ATTRIBTYPES \_ only** est définie, le jeu de résultats comprend les éléments suivants :

``` syntax
name
sn
department
phone
```

La valeur par défaut est pour le retour des valeurs et des noms d’attribut.

Pour récupérer uniquement des noms d’attributs, définissez une option de recherche **\_ SEARCHPREF \_ ATTRIBTYPES ADS \_ uniquement** avec une valeur **\_ booléenne ADSTYPE** **true** dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

L’exemple de code suivant montre comment récupérer uniquement des noms d’attributs.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Pour plus d’informations et pour obtenir un exemple de code qui montre comment utiliser l’option de recherche **\_ ATTRIBTYPES SEARCHPREF ADS \_ \_ uniquement** , consultez l' [exemple de code pour rechercher des attributs](example-code-for-searching-for-attributes.md).

 

 




