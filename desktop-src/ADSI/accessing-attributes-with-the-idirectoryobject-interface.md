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
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a>Accès aux attributs avec l’interface IDirectoryObject

L’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fournit une application cliente écrite en C et C++ avec un accès direct aux objets du service d’annuaire. L’interface active l’accès au moyen d’un protocole réseau direct, plutôt que via le cache des attributs ADSI. À la place des propriétés prises en charge par l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , **IDirectoryObject** fournit des méthodes qui prennent en charge un sous-ensemble critique des méthodes de maintenance d’un objet et fournissent l’accès à ses attributs. Avec **IDirectoryObject**, un client peut obtenir ou définir un nombre quelconque d’attributs d’objet à l’aide d’un appel de méthode. Contrairement aux méthodes Automation correspondantes, qui sont traitées par lot, celles de **IDirectoryObject** sont exécutées lorsqu’elles sont appelées. Étant donné que les méthodes sur cette interface ne nécessitent pas la création d’une instance d’un objet d’annuaire Automation, la surcharge de performances est faible.

Les clients écrits dans des langages tels que C et C++ doivent utiliser les méthodes de l’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pour optimiser les performances et tirer parti des interfaces de service d’annuaire natives. Les clients Automation ne peuvent pas utiliser **IDirectoryObject**. Au lieu de cela, ils doivent utiliser l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .

La méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) récupère les attributs avec des valeurs uniques et multiples. Cette méthode prend une liste d’attributs demandés et retourne une structure d' [**\_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) . ADSI alloue cette structure ; l’appelant doit libérer cette mémoire lorsqu’il n’est plus nécessaire à l’aide de la fonction [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .

L’ordre des valeurs d’attribut retournées n’est pas nécessairement le même que l’ordre dans lequel les attributs ont été demandés. Par conséquent, il est nécessaire de comparer les noms d’attributs retournés par ADSI.

> [!Note]  
> La [**structure \_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) ne retourne pas tous les attributs demandés. Seuls les attributs qui contiennent des valeurs font partie de la structure retournée.

 

Le nombre d’attributs retournés est déterminé par le paramètre *dwNumberAttributes* passé à la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .

L’exemple de code suivant lie à un objet et utilise la méthode [**IDirectoryObject :: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) pour récupérer les attributs de l’objet.


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



 

 




