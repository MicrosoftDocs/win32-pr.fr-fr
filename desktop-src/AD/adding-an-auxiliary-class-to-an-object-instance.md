---
title: Ajout d’une classe auxiliaire à une instance d’objet
description: Les exemples de code suivants montrent comment utiliser ADSI et LDAP pour ajouter dynamiquement une classe auxiliaire à une instance d’objet existante.
ms.assetid: 739dd372-3bda-4d94-8daf-f71e3091cfb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6b1f61bffe9081350949cccddc70fee83a568
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031060"
---
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a>Ajout d’une classe auxiliaire à une instance d’objet

Les exemples de code suivants montrent comment utiliser ADSI et LDAP pour ajouter dynamiquement une classe auxiliaire à une instance d’objet existante. Les exemples supposent qu’une classe auxiliaire nommée **Vehicle** est définie dans le schéma Active Directory, et que la classe **Vehicle** a un attribut **vin** .

Quand vous ajoutez dynamiquement une classe auxiliaire à une instance d’objet, vous devez spécifier simultanément des valeurs pour tous les attributs **musthave** obligatoires dans la classe. Les exemples suivants montrent comment effectuer cette opération avec l’attribut « vin », qui est supposé être obligatoire.

L’exemple C++ suivant effectue une liaison à un objet et utilise [**IADs.**](/windows/desktop/api/iads/nf-iads-iads-putex) prénom pour ajouter la classe auxiliaire à la liste de classes dans la propriété **objectClass** de l’objet. L’exemple utilise ensuite [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put) pour définir la valeur de l’attribut **vin** . Enfin, il appelle [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider les modifications apportées au répertoire.


```C++
LPWSTR pszAuxClass[]={L"vehicle"};
LPWSTR pszVIN[]={L"df897dsfsa-0"};
VARIANT var;

VariantInit(&var);

ADsOpenObject(L"cn=johnd,cn=users,dc=fabrikam,dc=com", 
    NULL, 
    NULL, 
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,  
    (VOID**)&pIADs);

ADsBuildVarArrayStr(pszAuxClass, 1, &var);
pIADs->PutEx(ADS_PROPERTY_APPEND, CComBSTR("objectClass"), var);
ADsBuildVarArrayStr( pszVIN, 1, &var);
pIADs->Put(CComBSTR("vin"), var);
pIADs->SetInfo();

if(pIADs)
    pIADs->Release();

VariantClear(&var);
```



 

 