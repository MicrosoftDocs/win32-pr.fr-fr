---
title: Modèle d’objet ADSI pour les fournisseurs LDAP
description: Illustration qui montre les objets ADSI utilisés pour le fournisseur LDAP et les interfaces utilisées pour accéder à ces objets.
ms.assetid: 109fd42e-201e-4b84-a213-2695d81f005b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c7c520793f6095bc9d4d9c6379f8ff6f09766f39ae6102f7e0a82d3a3de7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023790"
---
# <a name="adsi-object-model-for-ldap-providers"></a>Modèle d’objet ADSI pour les fournisseurs LDAP

L’illustration suivante montre les objets ADSI utilisés pour le fournisseur LDAP et les interfaces utilisées pour accéder à ces objets.

![modèle d’objet pour le fournisseur LDAP](images/adsiobjmodldap-gif-1.png)

| Object                        | Interface                                                                                                                                                                                                                                                                                      |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Classe<br/>              | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                                                                                                                                                                                                                           |
| Propriété<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                                                                                                                                                                                                                                     |
| GenObject<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops), [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) |
| Espace de noms<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                                                                                                                                                                                     |
| RootDSE<br/>            | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                                                                                                                                                                                                                             |
| Chemin<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)                                                                                                                                                                                                                                     |
| schéma<br/>             | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                                                                                                                                                                                                                                   |
| Syntaxe<br/>             | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                                                                                                                                                                                                                                         |
| Organisation<br/>       | [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                                                                                                                                                                                                                                                         |
| OrganizationalUnit<br/> | [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                                                                                                                                                                                                                                                       |
| GroupCollection<br/>    | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Groupe<br/>              | [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                                                                                                                                                                                                                                                 |
| UserCollection<br/>     | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Utilisateur<br/>               | [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                                                                                                                                                                                                                                                   |
| Localité<br/>           | [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                                                                                                                                                                                                                                                           |
| NameTranslate<br/>      | [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)                                                                                                                                                                                                                                                 |
| PrintQueue<br/>         | [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue), [ **IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)                                                                                                                                                                                         |



 

 

 





