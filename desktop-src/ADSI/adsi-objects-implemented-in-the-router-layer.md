---
title: Objets ADSI implémentés dans la couche de routeur
description: Le tableau suivant présente une brève description des objets COM implémentés dans le routeur ADSI.
ms.assetid: bd446e05-a15d-4354-9204-1df4e360497c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cc96eac8a2d680cb83622e01d94f8ef7a1d236726ab6b6fef9b2e6c5c40f50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692816"
---
# <a name="adsi-objects-implemented-in-the-router-layer"></a>Objets ADSI implémentés dans la couche de routeur

Le tableau suivant présente une brève description des objets COM implémentés dans le routeur ADSI.



| Objet ADSI            | Description                                                         | Interfaces prises en charge                                                                                                                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AccessControlEntry** | Objet ADSI qui représente une entrée de contrôle d’accès (ACE).       | [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)                                                                                                                                                                                                                                  |
| **AccessControlList**  | Objet ADSI qui représente une liste de contrôle d’accès (ACL).        | [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                                                                                                                                                                                                                                    |
| **ADsNamespaces**      | Objet ADSI qui représente le conteneur de différents espaces de noms. | <dl> <dt>[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)</dt> <dt>[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)</dt> <dt>[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)</dt> </dl> |
| **LargeInteger**       | Objet ADSI qui représente un grand entier.                     | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                                                                                                                                                                                                                                              |
| **PropertyEntry**      | Objet ADSI qui représente une entrée de propriété.                    | [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                                                                                                                                                                                                                                            |
| **PropertyValue**      | Objet ADSI qui représente une valeur de propriété.                    | [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                                                                                                                                                                                                                                            |
| **PropertyValue2**     | Objet ADSI qui représente une valeur de propriété.                    | [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)                                                                                                                                                                                                                                          |
| **SecurityDescriptor** | Objet ADSI qui représente un descripteur de sécurité.               | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                                                                                                                                                                                                                  |



 

 

 




