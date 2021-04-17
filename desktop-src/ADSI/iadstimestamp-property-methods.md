---
title: Méthodes de propriété IADsTimestamp (IADs. h)
description: La méthode Property de l’interface IADsTimestamp définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsTimestamp ADSI
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77db7a6a3b3814cd10beca5da5e3166ab1b61a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465062"
---
# <a name="iadstimestamp-property-methods"></a><span data-ttu-id="3e097-105">Méthodes de propriété IADsTimestamp</span><span class="sxs-lookup"><span data-stu-id="3e097-105">IADsTimestamp Property Methods</span></span>

<span data-ttu-id="3e097-106">La méthode Property de l’interface [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3e097-106">The property method of the [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) interface sets the property described in the following table.</span></span> <span data-ttu-id="3e097-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3e097-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3e097-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3e097-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3e097-109">**EventID**</span><span class="sxs-lookup"><span data-stu-id="3e097-109">**EventID**</span></span>
<span data-ttu-id="3e097-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3e097-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3e097-111">Identificateur d'événement.</span><span class="sxs-lookup"><span data-stu-id="3e097-111">An event identifier.</span></span>

<dt>

<span data-ttu-id="3e097-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3e097-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3e097-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="3e097-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e097-114">**WholeSeconds**</span><span class="sxs-lookup"><span data-stu-id="3e097-114">**WholeSeconds**</span></span>
<span data-ttu-id="3e097-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3e097-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="3e097-116">Nombre de secondes avec une valeur nulle égale à 12:00 AM, 1970 janvier, UTC.</span><span class="sxs-lookup"><span data-stu-id="3e097-116">Number of seconds with zero value being 12:00 AM, January 1970, UTC.</span></span>

<dt>

<span data-ttu-id="3e097-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3e097-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3e097-118">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="3e097-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="3e097-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e097-119">Requirements</span></span>



| <span data-ttu-id="3e097-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e097-120">Requirement</span></span> | <span data-ttu-id="3e097-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e097-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e097-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e097-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3e097-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e097-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e097-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e097-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3e097-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e097-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e097-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e097-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e097-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e097-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3e097-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3e097-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e097-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e097-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e097-130">IID</span><span class="sxs-lookup"><span data-stu-id="3e097-130">IID</span></span><br/>                      | <span data-ttu-id="3e097-131">IID \_ IADsTimestamp est défini en tant que B2F5A901-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="3e097-131">IID\_IADsTimestamp is defined as B2F5A901-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="3e097-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e097-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e097-133">**IADsTimestamp**</span><span class="sxs-lookup"><span data-stu-id="3e097-133">**IADsTimestamp**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[<span data-ttu-id="3e097-134">**\_horodateur ads**</span><span class="sxs-lookup"><span data-stu-id="3e097-134">**ADS\_TIMESTAMP**</span></span>](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





