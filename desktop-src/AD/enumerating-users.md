---
title: Énumération des utilisateurs
description: contrairement à Windows domaines NT 4,0, Windows 2000 utilisateurs peuvent être placés dans n’importe quel conteneur ou unité d’organisation (ou) dans un domaine, ainsi que la racine du domaine.
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- Énumération des utilisateurs Active Directory
- utilisateurs Active Directory, énumération d’un utilisateur
- Active Directory, utilisation de, utilisateurs, énumération d’un utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa43034c6c006c9c70531f25e2a838ecfc30520e9b42e0b9599e5714a29f225e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191339"
---
# <a name="enumerating-users"></a>Énumération des utilisateurs

contrairement à Windows domaines NT 4,0, Windows 2000 utilisateurs peuvent être placés dans n’importe quel conteneur ou unité d’organisation (ou) dans un domaine, ainsi que la racine du domaine. Cela signifie que les utilisateurs peuvent se trouver à de nombreux emplacements dans la hiérarchie de répertoires. Par conséquent, vous avez deux possibilités pour l’énumération des utilisateurs :

-   Énumérer les utilisateurs contenus directement dans un conteneur, une unité d’organisation ou à la racine du domaine :

    Effectuez une liaison explicite à l’objet conteneur qui contient les utilisateurs que vous souhaitez énumérer, définissez un filtre contenant « utilisateur » en tant que classe à l’aide de la propriété [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) et utilisez la méthode [**IADsContainer :: obtenir \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) pour énumérer les objets utilisateur.

    Cette technique peut être utilisée pour énumérer les utilisateurs qui sont directement contenus dans un conteneur ou un objet d’unité d’organisation. Si le conteneur contient d’autres conteneurs qui peuvent potentiellement contenir d’autres utilisateurs, vous devez les lier à ces conteneurs et énumérer de manière récursive les utilisateurs sur ces conteneurs. Si vous n’avez pas besoin de manipuler les objets utilisateur et que vous devez uniquement lire des propriétés spécifiques, utilisez la recherche détaillée décrite dans l’option 2.

    Étant donné que l’énumération retourne des pointeurs vers des objets COM ADSI représentant chaque objet utilisateur, vous pouvez appeler [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour récupérer les pointeurs d’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)et [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) sur l’objet utilisateur. Cela signifie que vous pouvez obtenir des pointeurs d’interface vers chaque objet utilisateur énuméré dans un conteneur sans avoir à effectuer une liaison explicite à chaque objet utilisateur. Pour effectuer des opérations sur tous les utilisateurs directement dans un conteneur, l’énumération évite d’avoir à établir une liaison à chaque utilisateur afin d’appeler des méthodes **IADs** ou **IADsUser** . Pour récupérer des propriétés spécifiques des utilisateurs, utilisez [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) comme décrit dans l’option 2.

-   Effectuez une recherche détaillée (& (objectClass = user) (objectCategory = person)) pour rechercher tous les utilisateurs dans une arborescence :

    Tout d’abord, établissez une liaison avec l’objet conteneur où commencer la recherche. Par exemple, pour rechercher tous les utilisateurs dans un domaine, établissez une liaison à la racine du domaine. pour rechercher tous les utilisateurs de la forêt, établissez une liaison au catalogue global et recherchez à partir de la racine du GC.

    Utilisez ensuite [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pour interroger à l’aide d’un filtre de recherche contenant (& (objectClass = user) (objectcategory = person)) et la préférence de recherche de la \_ sous-arborescence étendue ADS \_ .

    Vous pouvez effectuer une recherche à l’aide d’une préférence de recherche de \_ l’étendue ad \_ onelevel pour limiter la recherche au contenu direct de l’objet conteneur auquel vous êtes lié.

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) récupère uniquement les valeurs des propriétés spécifiques des utilisateurs. Pour récupérer des valeurs, utilisez **IDirectorySearch**. Pour manipuler les objets utilisateur retournés par une recherche, autrement dit, vous souhaitez utiliser des méthodes [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) , vous devez les lier explicitement. Pour ce faire, spécifiez **distinguishedName** comme l’une des propriétés à retourner à partir de la recherche et utilisez les noms distinctifs retournés pour établir une liaison à chaque utilisateur retourné dans la recherche.

    Seules les propriétés spécifiques sont récupérées. Vous ne pouvez pas récupérer tous les attributs sans spécifier explicitement chaque attribut possible de la classe utilisateur.

 

 