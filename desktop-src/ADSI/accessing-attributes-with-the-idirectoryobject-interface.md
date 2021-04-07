---
title: Accès aux attributs avec l’interface IDirectoryObject
description: L’interface IDirectoryObject fournit une application cliente écrite en C et C++ avec un accès direct aux objets du service d’annuaire.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Accès aux attributs avec l’interface IDirectoryObject ADSI
- IDirectoryObject ADSI, accès aux attributs avec
- ADSI ADSI, à l’aide de, à l’aide de l’interface IDirectoryObject pour accéder aux attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da62b6a5cf7e1389276475c46faac6455672790
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939617"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="dda03-106">Accès aux attributs avec l’interface IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="dda03-106">Accessing Attributes With the IDirectoryObject Interface</span></span>

<span data-ttu-id="dda03-107">L’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fournit une application cliente écrite en C et C++ avec un accès direct aux objets du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="dda03-107">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface provides a client application written in C and C++ with direct access to directory service objects.</span></span> <span data-ttu-id="dda03-108">L’interface active l’accès au moyen d’un protocole réseau direct, plutôt que via le cache des attributs ADSI.</span><span class="sxs-lookup"><span data-stu-id="dda03-108">The interface enables access by means of a direct network protocol, rather than through the ADSI attribute cache.</span></span> <span data-ttu-id="dda03-109">À la place des propriétés prises en charge par l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , **IDirectoryObject** fournit des méthodes qui prennent en charge un sous-ensemble critique des méthodes de maintenance d’un objet et fournissent l’accès à ses attributs.</span><span class="sxs-lookup"><span data-stu-id="dda03-109">In place of the properties supported by the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface, **IDirectoryObject** provides methods that support a critical subset of an object's maintenance methods and provide access to its attributes.</span></span> <span data-ttu-id="dda03-110">Avec **IDirectoryObject**, un client peut obtenir ou définir un nombre quelconque d’attributs d’objet à l’aide d’un appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="dda03-110">With **IDirectoryObject**, a client can get or set any number of object attributes with one method call.</span></span> <span data-ttu-id="dda03-111">Contrairement aux méthodes Automation correspondantes, qui sont traitées par lot, celles de **IDirectoryObject** sont exécutées lorsqu’elles sont appelées.</span><span class="sxs-lookup"><span data-stu-id="dda03-111">Unlike the corresponding Automation methods, which are batched, those of **IDirectoryObject** are executed when called.</span></span> <span data-ttu-id="dda03-112">Étant donné que les méthodes sur cette interface ne nécessitent pas la création d’une instance d’un objet d’annuaire Automation, la surcharge de performances est faible.</span><span class="sxs-lookup"><span data-stu-id="dda03-112">Because methods on this interface do not require creating an instance of an Automation directory object, the performance overhead is small.</span></span>

<span data-ttu-id="dda03-113">Les clients écrits dans des langages tels que C et C++ doivent utiliser les méthodes de l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pour optimiser les performances et tirer parti des interfaces de service d’annuaire natives.</span><span class="sxs-lookup"><span data-stu-id="dda03-113">Clients written in languages such as C and C++ should use the methods of the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface to optimize performance and take advantage of native directory service interfaces.</span></span> <span data-ttu-id="dda03-114">Les clients Automation ne peuvent pas utiliser **IDirectoryObject**.</span><span class="sxs-lookup"><span data-stu-id="dda03-114">Automation clients cannot use **IDirectoryObject**.</span></span> <span data-ttu-id="dda03-115">Au lieu de cela, ils doivent utiliser l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="dda03-115">Instead, they should use the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>

<span data-ttu-id="dda03-116">La méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) récupère les attributs avec des valeurs uniques et multiples.</span><span class="sxs-lookup"><span data-stu-id="dda03-116">The [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method retrieves attributes with both single and multiple values.</span></span> <span data-ttu-id="dda03-117">Cette méthode prend une liste d’attributs demandés et retourne une structure d' [**\_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) .</span><span class="sxs-lookup"><span data-stu-id="dda03-117">This method takes a list of requested attributes and returns an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure.</span></span> <span data-ttu-id="dda03-118">ADSI alloue cette structure ; l’appelant doit libérer cette mémoire lorsqu’il n’est plus nécessaire à l’aide de la fonction [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="dda03-118">ADSI allocates this structure; the caller must free this memory when it is no longer required using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="dda03-119">L’ordre des valeurs d’attribut retournées n’est pas nécessairement le même que l’ordre dans lequel les attributs ont été demandés.</span><span class="sxs-lookup"><span data-stu-id="dda03-119">The order of returned attribute values is not necessarily the same as the order in which the attributes were requested.</span></span> <span data-ttu-id="dda03-120">Par conséquent, il est nécessaire de comparer les noms d’attributs retournés par ADSI.</span><span class="sxs-lookup"><span data-stu-id="dda03-120">Therefore, it is necessary to compare the attribute names returned from ADSI.</span></span>

> [!Note]  
> <span data-ttu-id="dda03-121">La [**structure \_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) ne retourne pas tous les attributs demandés.</span><span class="sxs-lookup"><span data-stu-id="dda03-121">The [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure does not return all of the attributes requested.</span></span> <span data-ttu-id="dda03-122">Seuls les attributs qui contiennent des valeurs font partie de la structure retournée.</span><span class="sxs-lookup"><span data-stu-id="dda03-122">Only those attributes that contain values are part of the returned structure.</span></span>

 

<span data-ttu-id="dda03-123">Le nombre d’attributs retournés est déterminé par le paramètre *dwNumberAttributes* passé à la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="dda03-123">The number of attributes returned is determined by the *dwNumberAttributes* parameter passed to the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>

<span data-ttu-id="dda03-124">L’exemple de code suivant lie à un objet et utilise la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) pour récupérer les attributs de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dda03-124">The following code example binds to an object and uses the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve attributes of the object.</span></span>


```C++
HRESULT hr;
IDirectoryObject *pDirObject;

CoInitialize(NULL);

hr = ADsGetObject(
       L"LDAP://CN=Jeff Smith,OU=Users,DC=Fabrikam,DC=com",
       IID_IDirectoryObject, 
       (void**)&pDirObject);

if(SUCCEEDED(hr))
{
  ADS_ATTR_INFO *pAttrInfo = NULL;
  LPWSTR pAttrNames[] = {L"cn", L"title", L"otherTelephone"};
  DWORD dwNumAttr = sizeof(pAttrNames)/sizeof(LPWSTR);
  DWORD dwReturn;

  //////////////////////////////////////////////////
  // Get attribute values requested.
  // Be aware that the order is not necessarily the 
  // same as requested using pAttrNames.
  //////////////////////////////////////////////////
  hr = pDirObject->GetObjectAttributes(pAttrNames, 
                                       dwNumAttr, 
                                       &pAttrInfo, 
                                       &dwReturn);
     
  if(SUCCEEDED(hr))
  {
    for(DWORD idx = 0; idx < dwReturn; idx++)
      {
        if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"cn") == 0)
        {
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Common Name: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"title") == 0)
        {
          if(pAttrInfo->dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Title: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, 
                L"otherTelephone") == 0)
        {  
          // Print the multi-valued property, "Other Telephones".
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
        {
          wprintf(L"Other Telephones:");
          for(DWORD val = 0; val < pAttrInfo[idx].dwNumValues; val++) 
          {
            wprintf(L"  %s\n", 
                    pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
          }
        }
      }
    }

    FreeADsMem(pAttrInfo);
  }
     
  pDirObject->Release();
}

CoUninitialize();
```



 

 




