---
title: Méthodes de propriété IADsPostalAddress (IADs. h)
description: La méthode Property de l’interface IADsPostalAddress définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPostalAddress ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d8eeaac8fa258a2df1452b8aa261ee59b3cc85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515072"
---
# <a name="iadspostaladdress-property-methods"></a><span data-ttu-id="39172-105">Méthodes de propriété IADsPostalAddress</span><span class="sxs-lookup"><span data-stu-id="39172-105">IADsPostalAddress Property Methods</span></span>

<span data-ttu-id="39172-106">La méthode Property de l’interface [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="39172-106">The property method of the [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) interface sets the property described in the following table.</span></span> <span data-ttu-id="39172-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="39172-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="39172-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="39172-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="39172-109">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="39172-109">**PostalAddress**</span></span>
<span data-ttu-id="39172-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="39172-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="39172-111">Tableau de six chaînes contenant l’adresse postale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39172-111">An array of six strings holding the postal address of the user.</span></span>

<dt>

<span data-ttu-id="39172-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="39172-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="39172-113">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="39172-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="39172-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39172-114">Requirements</span></span>



| <span data-ttu-id="39172-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39172-115">Requirement</span></span> | <span data-ttu-id="39172-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="39172-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39172-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39172-117">Minimum supported client</span></span><br/> | <span data-ttu-id="39172-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39172-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39172-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39172-119">Minimum supported server</span></span><br/> | <span data-ttu-id="39172-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39172-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39172-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="39172-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="39172-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="39172-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="39172-123">DLL</span><span class="sxs-lookup"><span data-stu-id="39172-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39172-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39172-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="39172-125">IID</span><span class="sxs-lookup"><span data-stu-id="39172-125">IID</span></span><br/>                      | <span data-ttu-id="39172-126">IID \_ IADsPostalAddress est défini en tant que 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="39172-126">IID\_IADsPostalAddress is defined as 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="39172-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39172-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39172-128">**IADsPostalAddress**</span><span class="sxs-lookup"><span data-stu-id="39172-128">**IADsPostalAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[<span data-ttu-id="39172-129">**\_POSTALADDRESS ads**</span><span class="sxs-lookup"><span data-stu-id="39172-129">**ADS\_POSTALADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 





