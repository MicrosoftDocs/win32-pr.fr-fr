---
title: mappage du code d’Visual Basic ADSI au code C++
description: ADSI est constitué de plus de 50 interfaces.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a924f403dcbdbe89b1b0bbf846c95223b401a04d1925ce9362a5300faf828fe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179206"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>mappage du code d’Visual Basic ADSI au code C++

ADSI est constitué de plus de 50 interfaces. La plupart des opérations d’annuaire peuvent être effectuées à l’aide de cinq interfaces uniquement. Il s'agit de :

-   [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**Rubrique IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

le tableau suivant répertorie les mappages d’ADSI VB le code/VBS au code C++. N’oubliez pas qu’il ne s’agit pas d’une liste complète.



| Code VBS                           | Code VC                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject ()              | HR = AdsGetObject ()                                                   |
| obj. Placez obj. Obtient obj. Parent         | IADs ou IDirectoryObject                                              |
| obj. Créez un obj. Supprimez obj. MoveHere | IADsContainer                                                         |
| For each... dans...                      | AdsBuildEnumerator() ADsEnumerateNext()                               |
| Connexion, commande, Recordset     | Rubrique IDirectorySearch                                                      |
| Descripteur de sécurité, ACL, ACE      | IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry |



 

 

 




