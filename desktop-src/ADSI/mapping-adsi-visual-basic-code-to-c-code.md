---
title: Mappage du code d’Visual Basic ADSI au code C++
description: ADSI est constitué de plus de 50 interfaces.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510385"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>Mappage du code d’Visual Basic ADSI au code C++

ADSI est constitué de plus de 50 interfaces. La plupart des opérations d’annuaire peuvent être effectuées à l’aide de cinq interfaces uniquement. Les voici :

-   [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**Rubrique IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Le tableau suivant répertorie les mappages du code ADSI VB/VBS au code C++. N’oubliez pas qu’il ne s’agit pas d’une liste complète.



| Code VBS                           | Code VC                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject ()              | HR = AdsGetObject ()                                                   |
| obj. Placez obj. Obtient obj. Parent         | IADs ou IDirectoryObject                                              |
| obj. Créez un obj. Supprimez obj. MoveHere | IADsContainer                                                         |
| For each... dans...                      | AdsBuildEnumerator() ADsEnumerateNext()                               |
| Connexion, commande, Recordset     | Rubrique IDirectorySearch                                                      |
| Descripteur de sécurité, ACL, ACE      | IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry |



 

 

 




