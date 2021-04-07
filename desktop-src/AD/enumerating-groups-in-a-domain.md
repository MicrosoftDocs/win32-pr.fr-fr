---
title: Énumération des groupes dans un domaine
description: Les groupes peuvent être placés dans n’importe quel conteneur ou unité d’organisation (ou) dans un domaine, ainsi que la racine du domaine.
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- Énumération des groupes dans un domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3586b8c6d261c769cabe56def2aa9396a58fa3a5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724564"
---
# <a name="enumerating-groups-in-a-domain"></a>Énumération des groupes dans un domaine

Les groupes peuvent être placés dans n’importe quel conteneur ou unité d’organisation (ou) dans un domaine, ainsi que la racine du domaine. Cela signifie que les groupes peuvent se trouver à de nombreux emplacements dans la hiérarchie de répertoires. Par conséquent, vous avez deux possibilités pour énumérer des groupes :

1.  Énumérez les groupes contenus directement dans un conteneur, une unité d’organisation ou à la racine du domaine.

    Établissez une liaison explicite à l’objet conteneur qui contient les groupes à énumérer, définissez un filtre qui contient « Groups » en tant que classe à l’aide de la propriété [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) et utilisez la méthode [**IADsContainer :: obtenir \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) pour énumérer les objets de groupe.

    Cette technique énumère les groupes contenus directement dans un conteneur ou un objet d’unité d’organisation. Si le conteneur contient d’autres conteneurs qui peuvent potentiellement contenir d’autres groupes, vous devez les lier à ces conteneurs et énumérer de manière récursive les groupes sur ces conteneurs. Pour manipuler les objets de groupe et lire uniquement des propriétés spécifiques, utilisez la recherche détaillée décrite dans l’option 2.

    Étant donné que l’énumération retourne des pointeurs vers des objets COM ADSI représentant chaque objet de groupe, vous pouvez appeler [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour récupérer les pointeurs d’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)et [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) sur l’objet de groupe. autrement dit, vous pouvez obtenir des pointeurs d’interface vers chaque objet de groupe énuméré dans un conteneur sans avoir à effectuer une liaison explicite à chaque objet de groupe. Pour effectuer des opérations sur tous les groupes directement dans un conteneur, l’énumération ne requiert pas de liaison à chaque groupe afin d’appeler des méthodes **IADs** ou **IADsGroup** . Pour récupérer des propriétés spécifiques à partir de groupes, utilisez [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) comme décrit dans la deuxième option.

    Une exception à cette situation se produit lorsque vous tentez d’énumérer un groupe qui contient des membres qui sont des principaux de sécurité wellKnown, tels que tout le monde, utilisateurs authentifiés, traitement par lots, etc. Étant donné que vous ne pouvez pas lier ces types d’objets, ils ne sont pas répertoriés quand vous énumérez des groupes dans l’étendue WinNT, même s’il peut sembler être lié, car certaines méthodes IADs telles que Class, ADsPath et Name retournent des résultats corrects lorsqu’ils sont appelés sur des membres énumérés.

2.  Effectuez une recherche complète sur « objectCategory = Group » pour rechercher tous les groupes dans une arborescence.

    Tout d’abord, établissez une liaison avec l’objet conteneur où commencer la recherche. Par exemple, pour rechercher tous les groupes d’un domaine, établissez une liaison à la racine du domaine ; pour rechercher tous les groupes de la forêt, établissez une liaison avec le catalogue global et recherchez à partir de la racine du GC.

    Utilisez ensuite [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pour interroger à l’aide d’un filtre de recherche contenant (objectCategory = Group) et des préférences de recherche de la **\_ sous- \_ arborescence étendue ADS**.

    > [!Note]  
    > Vous pouvez effectuer une recherche à l’aide d’une préférence de recherche de l' **\_ étendue ad \_ onelevel** pour limiter la recherche au contenu direct de l’objet conteneur auquel vous êtes lié.

     

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) récupère uniquement les valeurs des propriétés spécifiques des groupes. Pour récupérer des valeurs, utilisez **IDirectorySearch**. Pour manipuler les objets de groupe retournés à partir d’une recherche, autrement dit, pour utiliser des méthodes [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) , établissez une liaison explicite avec eux. Pour ce faire, spécifiez **distinguishedName** comme l’une des propriétés à retourner à partir de la recherche et utilisez les noms distinctifs retournés pour établir une liaison à chaque groupe retourné dans la recherche.

    Seules les propriétés spécifiques sont récupérées. Vous ne pouvez pas récupérer tous les attributs sans spécifier explicitement chaque attribut possible de la classe de groupe.

 

 