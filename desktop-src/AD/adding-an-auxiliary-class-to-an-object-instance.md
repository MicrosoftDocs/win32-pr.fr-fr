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
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a><span data-ttu-id="a05b2-103">Ajout d’une classe auxiliaire à une instance d’objet</span><span class="sxs-lookup"><span data-stu-id="a05b2-103">Adding an Auxiliary Class to an Object Instance</span></span>

<span data-ttu-id="a05b2-104">Les exemples de code suivants montrent comment utiliser ADSI et LDAP pour ajouter dynamiquement une classe auxiliaire à une instance d’objet existante.</span><span class="sxs-lookup"><span data-stu-id="a05b2-104">The following code examples show how to use ADSI and LDAP to dynamically add an auxiliary class to an existing object instance.</span></span> <span data-ttu-id="a05b2-105">Les exemples supposent qu’une classe auxiliaire nommée **Vehicle** est définie dans le schéma Active Directory, et que la classe **Vehicle** a un attribut **vin** .</span><span class="sxs-lookup"><span data-stu-id="a05b2-105">The examples assume that an auxiliary class named **vehicle** is defined in the Active Directory schema, and that the **vehicle** class has a **vin** attribute.</span></span>

<span data-ttu-id="a05b2-106">Quand vous ajoutez dynamiquement une classe auxiliaire à une instance d’objet, vous devez spécifier simultanément des valeurs pour tous les attributs **musthave** obligatoires dans la classe.</span><span class="sxs-lookup"><span data-stu-id="a05b2-106">When you dynamically add an auxiliary class to an object instance, you must simultaneously specify values for any mandatory **mustHave** attributes in the class.</span></span> <span data-ttu-id="a05b2-107">Les exemples suivants montrent comment effectuer cette opération avec l’attribut « vin », qui est supposé être obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a05b2-107">The following examples show how to do this with the "vin" attribute, which is assumed to be mandatory.</span></span>

<span data-ttu-id="a05b2-108">L’exemple C++ suivant effectue une liaison à un objet et utilise [**IADs.**](/windows/desktop/api/iads/nf-iads-iads-putex) prénom pour ajouter la classe auxiliaire à la liste de classes dans la propriété **objectClass** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a05b2-108">The following C++ example binds to an object, and uses [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) to append the auxiliary class to the list of classes in the object's **objectClass** property.</span></span> <span data-ttu-id="a05b2-109">L’exemple utilise ensuite [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put) pour définir la valeur de l’attribut **vin** .</span><span class="sxs-lookup"><span data-stu-id="a05b2-109">Then the example uses [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put) to set the value of the **vin** attribute.</span></span> <span data-ttu-id="a05b2-110">Enfin, il appelle [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider les modifications apportées au répertoire.</span><span class="sxs-lookup"><span data-stu-id="a05b2-110">Finally, it calls [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>


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



 

 