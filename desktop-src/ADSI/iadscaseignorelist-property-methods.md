---
title: Méthodes de propriété IADsCaseIgnoreList (IADs. h)
description: La méthode Property de l’interface IADsCaseIgnoreList définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsCaseIgnoreList ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aabf26508c3e38e117ad25721af8bece5d69b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510159"
---
# <a name="iadscaseignorelist-property-methods"></a><span data-ttu-id="6c5a9-105">Méthodes de propriété IADsCaseIgnoreList</span><span class="sxs-lookup"><span data-stu-id="6c5a9-105">IADsCaseIgnoreList Property Methods</span></span>

<span data-ttu-id="6c5a9-106">La méthode Property de l’interface [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6c5a9-106">The property method of the [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) interface sets the property described in the following table.</span></span> <span data-ttu-id="6c5a9-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6c5a9-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6c5a9-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6c5a9-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6c5a9-109">**CaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="6c5a9-109">**CaseIgnoreList**</span></span>
<span data-ttu-id="6c5a9-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6c5a9-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6c5a9-111">Séquence ordonnée de chaînes qui ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="6c5a9-111">An ordered sequence of case insensitive strings.</span></span>

<dt>

<span data-ttu-id="6c5a9-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6c5a9-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6c5a9-113">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="6c5a9-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="6c5a9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c5a9-114">Requirements</span></span>



| <span data-ttu-id="6c5a9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c5a9-115">Requirement</span></span> | <span data-ttu-id="6c5a9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c5a9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5a9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c5a9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5a9-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c5a9-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c5a9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c5a9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5a9-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c5a9-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c5a9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c5a9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c5a9-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a9-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="6c5a9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6c5a9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c5a9-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a9-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c5a9-125">IID</span><span class="sxs-lookup"><span data-stu-id="6c5a9-125">IID</span></span><br/>                      | <span data-ttu-id="6c5a9-126">IID \_ IADsCaseIgnoreList est défini en tant que 7B66B533-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="6c5a9-126">IID\_IADsCaseIgnoreList is defined as 7B66B533-4680-11D1-A3B4-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="6c5a9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c5a9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5a9-128">**IADsCaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="6c5a9-128">**IADsCaseIgnoreList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[<span data-ttu-id="6c5a9-129">**\_liste des CASEIGNORE ADS \_**</span><span class="sxs-lookup"><span data-stu-id="6c5a9-129">**ADS\_CASEIGNORE\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





