---
title: Méthodes de propriété IADsDNWithString (IADs. h)
description: La méthode Property de l’interface IADsDNWithString définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsDNWithString ADSI
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa63a933a6a41eec9e6e55906a940cee650c87b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512824"
---
# <a name="iadsdnwithstring-property-methods"></a><span data-ttu-id="e5e7b-105">Méthodes de propriété IADsDNWithString</span><span class="sxs-lookup"><span data-stu-id="e5e7b-105">IADsDNWithString Property Methods</span></span>

<span data-ttu-id="e5e7b-106">La méthode Property de l’interface [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e5e7b-106">The property method of the [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) interface sets the property described in the following table.</span></span> <span data-ttu-id="e5e7b-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="e5e7b-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e5e7b-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e5e7b-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="e5e7b-109">**DNString**</span><span class="sxs-lookup"><span data-stu-id="e5e7b-109">**DNString**</span></span>
<span data-ttu-id="e5e7b-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e5e7b-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="e5e7b-111">Chaîne DN associée à une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="e5e7b-111">The DN string associated with a string value.</span></span>

<dt>

<span data-ttu-id="e5e7b-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e5e7b-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e5e7b-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e5e7b-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e5e7b-114">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="e5e7b-114">**StringValue**</span></span>
<span data-ttu-id="e5e7b-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e5e7b-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="e5e7b-116">Valeur de chaîne associée à un DN d’un objet.</span><span class="sxs-lookup"><span data-stu-id="e5e7b-116">The string value associated with a DN of an object.</span></span>

<dt>

<span data-ttu-id="e5e7b-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e5e7b-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e5e7b-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e5e7b-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="e5e7b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5e7b-119">Requirements</span></span>



| <span data-ttu-id="e5e7b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5e7b-120">Requirement</span></span> | <span data-ttu-id="e5e7b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5e7b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e7b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5e7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e5e7b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5e7b-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5e7b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5e7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e5e7b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5e7b-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5e7b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5e7b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5e7b-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5e7b-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="e5e7b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e5e7b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5e7b-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5e7b-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5e7b-130">IID</span><span class="sxs-lookup"><span data-stu-id="e5e7b-130">IID</span></span><br/>                      | <span data-ttu-id="e5e7b-131">IID \_ IADsDNWithString est défini en tant que 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="e5e7b-131">IID\_IADsDNWithString is defined as 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="e5e7b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5e7b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e7b-133">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="e5e7b-133">**IADsDNWithString**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[<span data-ttu-id="e5e7b-134">**\_DN ADS \_ avec \_ chaîne**</span><span class="sxs-lookup"><span data-stu-id="e5e7b-134">**ADS\_DN\_WITH\_STRING**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 





