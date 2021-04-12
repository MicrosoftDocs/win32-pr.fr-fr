---
title: Création et suppression d’objets
description: Avec ADSI, les objets sont créés et supprimés à l’aide de l’interface IADsContainer ou IDirectoryObject.
ms.assetid: 4d1f7ac5-48d3-4ea9-91e4-0cd4bb2ec9f8
ms.tgt_platform: multiple
keywords:
- Création et suppression d’objets ADSI
- ADSI, création et suppression d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4730c4cc6a95ad37bfd3953474d3d488fcf05abb
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463703"
---
# <a name="creating-and-deleting-objects"></a>Création et suppression d’objets

Avec ADSI, les objets sont créés et supprimés à l’aide de l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ou [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .

## <a name="creating-an-object-with-iadscontainer"></a>Création d’un objet avec IADsContainer

**Pour créer un objet avec l’interface IADsContainer**

1.  Créez une liaison avec le conteneur qui contiendra l’objet à créer et obtenez l’interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .
2.  Utilisez la méthode [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) pour créer un nouvel objet dans le conteneur.
3.  Définissez les valeurs de tous les attributs requis pour l’objet à l’aide de la méthode [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) ou [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-putex) placent. Les attributs requis pour créer un objet dépendent du service d’annuaire et du type d’objet créé. Pour plus d’informations sur la création d’objets Active Directory, consultez [création et suppression](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)d’objets Active Directory.
4.  Définissez les valeurs de tous les attributs facultatifs souhaités pour l’objet à l’aide de la méthode [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) ou [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-putex) préférences.
5.  Appelez la méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) pour valider l’objet et ses attributs. Le nouvel objet n’est pas réellement créé dans le service d’annuaire sous-jacent tant que la méthode **IADs. setinfo** n’a pas été appelée pour valider les attributs.

## <a name="creating-an-object-with-idirectoryobject"></a>Création d’un objet avec IDirectoryObject

**Pour créer un objet avec l’interface IDirectoryObject**

1.  Créez une liaison avec le conteneur qui contiendra l’objet à créer et obtenez l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .
2.  Allouez un tableau de structures d' [**\_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) qui contient une structure pour chaque attribut à définir lors de la création de l’objet.
3.  Remplissez une structure [**d' \_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) pour chaque attribut requis de l’objet. Les attributs requis pour créer un objet dépendent du service d’annuaire et du type d’objet créé. Pour plus d’informations sur la création d’objets Active Directory, consultez [création et suppression](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)d’objets Active Directory.
4.  Remplissez une structure [**d' \_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) pour chaque attribut facultatif de l’objet.
5.  Utilisez la méthode [**IDirectoryObject :: CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) pour créer l’objet dans le conteneur. Cette méthode valide également l’objet dans le service d’annuaire sous-jacent. Si le tableau d' [**\_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) ne contient pas tous les attributs requis pour l’objet, **IDirectoryObject :: CreateDSObject** échoue.

## <a name="deleting-an-object"></a>Suppression d’un objet

Pour supprimer un objet, utilisez la méthode [**IADsContainer ::D supprim**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) ou [**IDirectoryObject ::D eletedsobject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-deletedsobject) . Ces méthodes échouent si l’objet supprimé contient des objets enfants. Utilisez la méthode [**IADsDeleteOps ::D eleteobject**](/windows/desktop/api/Iads/nf-iads-iadsdeleteops-deleteobject) pour supprimer un conteneur et tous les objets enfants du conteneur.

Ce qui arrive à un objet supprimé dépend du service d’annuaire sous-jacent. Pour plus d’informations sur la suppression d’objets Active Directory, consultez [création et suppression](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)d’objets Active Directory.

 

 