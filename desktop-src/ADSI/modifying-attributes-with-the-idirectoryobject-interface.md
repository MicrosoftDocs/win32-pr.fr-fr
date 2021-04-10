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
ms.openlocfilehash: 8715826d0fc835f3d9ecae914fcc51603883af5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100564"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="20fc3-107">Modification des attributs avec l’interface IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="20fc3-107">Modifying Attributes with the IDirectoryObject Interface</span></span>

<span data-ttu-id="20fc3-108">En plus des [**IAD ::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) et [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex), vous pouvez utiliser la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) pour modifier les valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="20fc3-108">In addition to [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex), you can use the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method to modify attribute values.</span></span> <span data-ttu-id="20fc3-109">Pour utiliser cette méthode, vous devez remplir une structure [**d' \_ \_ informations attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) pour chaque attribut à modifier.</span><span class="sxs-lookup"><span data-stu-id="20fc3-109">To use this method, you must fill in an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure for each attribute to modify.</span></span>

<span data-ttu-id="20fc3-110">La méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) vous permet de modifier à la fois des attributs à valeur unique et à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="20fc3-110">The [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method enables you to modify both single-valued and multi-valued attributes.</span></span> <span data-ttu-id="20fc3-111">Cette fonction fournit des contrôles opérationnels similaires, tels que Clear, Append, DELETE et Update, à ceux qui se trouvent dans la méthode [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="20fc3-111">This function provides similar operational controls, such as clear, append, delete, and update, to those found in the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span> <span data-ttu-id="20fc3-112">Les constantes de contrôle sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="20fc3-112">The control constants include:</span></span>

-   [<span data-ttu-id="20fc3-113">**\_attr- \_ effacer les annonces**</span><span class="sxs-lookup"><span data-stu-id="20fc3-113">**ADS\_ATTR\_CLEAR**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="20fc3-114">**\_ \_ mise à jour de l’attr ads**</span><span class="sxs-lookup"><span data-stu-id="20fc3-114">**ADS\_ATTR\_UPDATE**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="20fc3-115">**\_Ajout d’attr ADS \_**</span><span class="sxs-lookup"><span data-stu-id="20fc3-115">**ADS\_ATTR\_APPEND**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="20fc3-116">**suppression de l' \_ attr ADS \_**</span><span class="sxs-lookup"><span data-stu-id="20fc3-116">**ADS\_ATTR\_DELETE**</span></span>](adsi-attribute-modification-types.md)

<span data-ttu-id="20fc3-117">La spécification de la [**\_ \_ mise à jour d’attr ADS**](adsi-attribute-modification-types.md) déclenche une opération côté serveur qui peut nécessiter de nombreuses ressources.</span><span class="sxs-lookup"><span data-stu-id="20fc3-117">Specifying [**ADS\_ATTR\_UPDATE**](adsi-attribute-modification-types.md) will trigger a server side operation that can be resource-intensive.</span></span> <span data-ttu-id="20fc3-118">Par exemple, vous pouvez lancer l’opération pour mettre à jour une longue liste d’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="20fc3-118">An example would be to initiate the operation to update a long list of group membership.</span></span> <span data-ttu-id="20fc3-119">En général, évitez d’utiliser cette opération, sauf si la modification implique un petit nombre d’attributs dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="20fc3-119">In general, refrain from using this operation unless the modification involves a small number of attributes in the directory.</span></span> <span data-ttu-id="20fc3-120">Pour modifier une longue liste d’appartenances à des groupes, l’approche la plus efficace consisterait à lire la liste à partir du répertoire sous-jacent, à apporter des modifications et à stocker à nouveau la liste mise à jour dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="20fc3-120">To modify a long list of group memberships, the more efficient approach would be to read the list from the underlying directory, make modifications, and store the updated list back to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="20fc3-121">À l’instar de [**IADs ::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) et [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) avec [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), les modifications d’attribut sont entièrement validées ou ignorées dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="20fc3-121">Like [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) with [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), the attribute changes are either completely committed or discarded in Active Directory.</span></span> <span data-ttu-id="20fc3-122">Si une ou plusieurs modifications ne sont pas autorisées et ne peuvent donc pas être effectuées, aucune des modifications collectives apportées aux attributs n’est validée dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="20fc3-122">If one or more of the modifications are not allowed and therefore not able to be performed, then none of the collective modifications made to the attributes are committed to the directory.</span></span>

 

## <a name="example"></a><span data-ttu-id="20fc3-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="20fc3-123">Example</span></span>

<span data-ttu-id="20fc3-124">L’exemple de code suivant montre comment modifier à la fois des attributs à valeur unique et à valeurs multiples à l’aide de la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="20fc3-124">The following code example shows how to modify both single and multi-valued attributes with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span>


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



 

 




