---
title: Méthodes de propriété IADsFaxNumber (IADs. h)
description: La méthode Property de l’interface IADsFaxNumber définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: f4d46b9d-8db2-47b3-b489-9ffc363e6ac6
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsFaxNumber ADSI
topic_type:
- apiref
api_name:
- IADsFaxNumber Property Methods
- IADsFaxNumber.TelephoneNumber
- IADsFaxNumber.get_TelephoneNumber
- IADsFaxNumber.put_TelephoneNumber
- IADsFaxNumber.Parameters
- IADsFaxNumber.get_Parameters
- IADsFaxNumber.put_Parameters
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e2d982aee794272f80e58385be34098a92a28e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511165"
---
# <a name="iadsfaxnumber-property-methods"></a><span data-ttu-id="c6bb4-105">Méthodes de propriété IADsFaxNumber</span><span class="sxs-lookup"><span data-stu-id="c6bb4-105">IADsFaxNumber Property Methods</span></span>

<span data-ttu-id="c6bb4-106">La méthode Property de l’interface [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c6bb4-106">The property method of the [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) interface sets the property described in the following table.</span></span> <span data-ttu-id="c6bb4-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c6bb4-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c6bb4-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c6bb4-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c6bb4-109">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="c6bb4-109">**Parameters**</span></span>
<span data-ttu-id="c6bb4-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c6bb4-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c6bb4-111">Paramètres de l’ordinateur de télécopie.</span><span class="sxs-lookup"><span data-stu-id="c6bb4-111">The parameters for the fax machine.</span></span>

<dt>

<span data-ttu-id="c6bb4-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c6bb4-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c6bb4-113">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="c6bb4-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parameters(
  [out] VARIANT* retval
);
HRESULT put_Parameters(
  [in] VARIANT vParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c6bb4-114">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="c6bb4-114">**TelephoneNumber**</span></span>
<span data-ttu-id="c6bb4-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c6bb4-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="c6bb4-116">Numéro de téléphone de l’ordinateur de télécopie.</span><span class="sxs-lookup"><span data-stu-id="c6bb4-116">The telephone number of the fax machine.</span></span>

<dt>

<span data-ttu-id="c6bb4-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c6bb4-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c6bb4-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c6bb4-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* retVal
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="c6bb4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6bb4-119">Requirements</span></span>



| <span data-ttu-id="c6bb4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6bb4-120">Requirement</span></span> | <span data-ttu-id="c6bb4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6bb4-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6bb4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6bb4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c6bb4-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6bb4-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6bb4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6bb4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c6bb4-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6bb4-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6bb4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6bb4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6bb4-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6bb4-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c6bb4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c6bb4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6bb4-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6bb4-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c6bb4-130">IID</span><span class="sxs-lookup"><span data-stu-id="c6bb4-130">IID</span></span><br/>                      | <span data-ttu-id="c6bb4-131">IID \_ IADsFaxNumber est défini en tant que A910DEA9-4680-11D1-0A3B-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="c6bb4-131">IID\_IADsFaxNumber is defined as A910DEA9-4680-11D1-0A3B-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c6bb4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6bb4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6bb4-133">**IADsFaxNumber**</span><span class="sxs-lookup"><span data-stu-id="c6bb4-133">**IADsFaxNumber**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[<span data-ttu-id="c6bb4-134">**\_FAXNUMBER ads**</span><span class="sxs-lookup"><span data-stu-id="c6bb4-134">**ADS\_FAXNUMBER**</span></span>](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 





