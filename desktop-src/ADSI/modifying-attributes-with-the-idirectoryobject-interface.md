---
title: Modification des attributs avec l’interface IDirectoryObject
description: En plus des IAD put et IADs, vous pouvez utiliser la méthode IDirectoryObject SetObjectAttributes pour modifier les valeurs d’attribut. Pour utiliser cette méthode, vous devez remplir une structure d' \_ informations attr ADS \_ pour chaque attribut à modifier.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Modification des attributs avec l’interface IDirectoryObject ADSI
- IDirectoryObject ADSI, utilisation pour modifier des attributs
- ADSI ADSI, exemple de code C/C++, utilisant IDirectoryObject pour modifier des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fa7d75d3e0dce489f676dafb36992c95a1cba2e9856bbbaf49f14806a6c1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179027"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>Modification des attributs avec l’interface IDirectoryObject

En plus des [**IAD ::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) et [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex), vous pouvez utiliser la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) pour modifier les valeurs d’attribut. Pour utiliser cette méthode, vous devez remplir une structure [**d' \_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) pour chaque attribut à modifier.

La méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) vous permet de modifier à la fois des attributs à valeur unique et à valeurs multiples. Cette fonction fournit des contrôles opérationnels similaires, tels que Clear, Append, DELETE et Update, à ceux qui se trouvent dans la méthode [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Les constantes de contrôle sont les suivantes :

-   [**\_attr- \_ effacer les annonces**](adsi-attribute-modification-types.md)
-   [**\_ \_ mise à jour de l’attr ads**](adsi-attribute-modification-types.md)
-   [**\_Ajout d’attr ADS \_**](adsi-attribute-modification-types.md)
-   [**suppression de l' \_ attr ADS \_**](adsi-attribute-modification-types.md)

La spécification de la [**\_ \_ mise à jour d’attr ADS**](adsi-attribute-modification-types.md) déclenche une opération côté serveur qui peut nécessiter de nombreuses ressources. Par exemple, vous pouvez lancer l’opération pour mettre à jour une longue liste d’appartenance à un groupe. En général, évitez d’utiliser cette opération, sauf si la modification implique un petit nombre d’attributs dans l’annuaire. Pour modifier une longue liste d’appartenances à des groupes, l’approche la plus efficace consisterait à lire la liste à partir du répertoire sous-jacent, à apporter des modifications et à stocker à nouveau la liste mise à jour dans l’annuaire.

> [!Note]  
> À l’instar de [**IADs ::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) et [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) avec [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), les modifications d’attribut sont entièrement validées ou ignorées dans Active Directory. Si une ou plusieurs modifications ne sont pas autorisées et ne peuvent donc pas être effectuées, aucune des modifications collectives apportées aux attributs n’est validée dans l’annuaire.

 

## <a name="example"></a>Exemple

L’exemple de code suivant montre comment modifier à la fois des attributs à valeur unique et à valeurs multiples à l’aide de la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .


```C++
HRESULT hr;
LPCWSTR pwszADsPath = L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com";
IDirectoryObject *pDirObject = NULL;

// Bind to the object.
hr = ADsGetObject(pwszADsPath, IID_IDirectoryObject, (void**)&pDirObject);
if(SUCCEEDED(hr))
{ 
    ADSVALUE adsvFaxNumber;
    ADSVALUE rgadsvOtherTelephones[2];
     
    // Set the new FAX number.
    adsvFaxNumber.dwType = ADSTYPE_CASE_IGNORE_STRING; 
    adsvFaxNumber.CaseIgnoreString = L"425-707-9790";

    // Set the first telephone number.
    rgadsvOtherTelephones[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[0].CaseIgnoreString = L"425-707-9791";

    // Set the second telephone number.
    rgadsvOtherTelephones[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[1].CaseIgnoreString = L"425-707-9792";

    ADS_ATTR_INFO attrInfo[2];

    // Setup the facsimileTelephoneNumber attribute data.
    attrInfo[0].pszAttrName = L"facsimileTelephoneNumber";
    attrInfo[0].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[0].dwADsType = adsvFaxNumber.dwType;
    attrInfo[0].pADsValues = &adsvFaxNumber;
    attrInfo[0].dwNumValues = 1;

    // Setup the otherTelephone attribute data.
    attrInfo[1].pszAttrName = L"otherTelephone";
    attrInfo[1].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[1].dwADsType = rgadsvOtherTelephones[0].dwType;
    attrInfo[1].pADsValues = rgadsvOtherTelephones;
    attrInfo[1].dwNumValues = sizeof(rgadsvOtherTelephones)/sizeof(ADSVALUE);

    DWORD dwReturn;
 
    // Set the new attribute values.
    hr = pDirObject->SetObjectAttributes(attrInfo, 
        sizeof(attrInfo)/sizeof(ADS_ATTR_INFO), 
        &dwReturn);

    pDirObject->Release();
}
```



 

 




