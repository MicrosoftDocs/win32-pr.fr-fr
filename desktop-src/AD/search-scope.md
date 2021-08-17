---
title: Spécification de l’étendue de recherche
description: Vous pouvez spécifier l’étendue d’une recherche sous la forme d’une recherche de base, d’un niveau ou d’une sous-arborescence.
ms.assetid: b02354c2-7b95-4911-8ae3-4a261d3ca2d3
ms.tgt_platform: multiple
keywords:
- Spécification de l’étendue de recherche Active Directory
- Active Directory, recherche, spécification de l’étendue de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ea307e349ffc91da41e72798be9c6232c9a510e2edf5563e5407d3d58ef2fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183857"
---
# <a name="specifying-the-search-scope"></a>Spécification de l’étendue de recherche

Vous pouvez spécifier l’étendue d’une recherche sous la forme d’une recherche de base, d’un niveau ou d’une sous-arborescence. Utilisez l’indicateur de la **\_ \_ \_ portée de recherche SEARCHPREF ADS** avec les valeurs de l’énumération [**\_ SCOPEENUM ADS**](/windows/win32/api/iads/ne-iads-ads_scopeenum) pour spécifier l’étendue de recherche. La liste suivante contient les descriptions des types de recherche :

-   De **base**. Une recherche de base limite la recherche à l’objet de base. Le nombre maximal d’objets retournés est toujours un. Cette recherche est utile pour vérifier l’existence d’un objet pour la récupération de l’appartenance à un groupe. Par exemple, si vous avez un nom unique d’objet et que vous devez vérifier l’existence de l’objet en fonction du chemin d’accès, vous pouvez utiliser une recherche à un niveau. Si la recherche échoue, vous pouvez supposer que l’objet a peut-être été renommé ou déplacé vers un autre emplacement, ou que vous avez reçu des informations incorrectes sur l’objet. N’oubliez pas que vous devez stocker l’identificateur global unique (GUID) de l’objet à la place du nom unique, si vous souhaitez revisiter un objet. Le GUID fait toujours référence au même objet, quel que soit l’emplacement de l’objet dans la hiérarchie de répertoires.
-   **Un niveau**. Une recherche à un niveau est limitée aux enfants immédiats d’un objet de base, mais exclut l’objet de base lui-même. Ce paramètre peut effectuer une recherche ciblée d’objets enfants immédiats d’un objet parent. Par exemple, considérez un objet parent P1 et ses enfants immédiats : C1, C2 et C3. Une recherche à un niveau évalue C1, C2 et C3 par rapport aux critères de recherche, mais n’évalue pas P1. Utilisez une recherche à un niveau pour énumérer tous les enfants d’un objet. Une énumération [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) se traduit par une recherche à un niveau.
-   **Sous-arborescence**. Une recherche de sous-arborescence (ou une recherche profonde) comprend tous les objets enfants, ainsi que l’objet de base. Vous pouvez demander au fournisseur LDAP de débusquer les références à d’autres services d’annuaire LDAP, y compris d’autres domaines ou forêts d’annuaire.

 

 