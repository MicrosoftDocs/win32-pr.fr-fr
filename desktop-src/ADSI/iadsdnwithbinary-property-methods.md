---
title: Méthodes de propriété IADsDNWithBinary (IADs. h)
description: La méthode Property de l’interface IADsDNWithBinary définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsDNWithBinary ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf0398a141596de677d7d1739e84ff7525da9a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105148"
---
# <a name="iadsdnwithbinary-property-methods"></a><span data-ttu-id="63008-105">Méthodes de propriété IADsDNWithBinary</span><span class="sxs-lookup"><span data-stu-id="63008-105">IADsDNWithBinary Property Methods</span></span>

<span data-ttu-id="63008-106">La méthode Property de l’interface [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="63008-106">The property method of the [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) interface sets the property described in the following table.</span></span> <span data-ttu-id="63008-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="63008-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="63008-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63008-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="63008-109">**BinaryValue**</span><span class="sxs-lookup"><span data-stu-id="63008-109">**BinaryValue**</span></span>
<span data-ttu-id="63008-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="63008-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="63008-111">GUID d’un objet associé à un DN.</span><span class="sxs-lookup"><span data-stu-id="63008-111">The GUID of an object associated with a DN.</span></span>

<dt>

<span data-ttu-id="63008-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63008-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="63008-113">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="63008-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="63008-114">**DNString**</span><span class="sxs-lookup"><span data-stu-id="63008-114">**DNString**</span></span>
<span data-ttu-id="63008-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="63008-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="63008-116">Chaîne DN associée au GUID d’un objet.</span><span class="sxs-lookup"><span data-stu-id="63008-116">The DN string associated with the GUID of an object.</span></span>

<dt>

<span data-ttu-id="63008-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63008-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="63008-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="63008-118">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="63008-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63008-119">Requirements</span></span>



| <span data-ttu-id="63008-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63008-120">Requirement</span></span> | <span data-ttu-id="63008-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="63008-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63008-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63008-122">Minimum supported client</span></span><br/> | <span data-ttu-id="63008-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63008-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63008-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63008-124">Minimum supported server</span></span><br/> | <span data-ttu-id="63008-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63008-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63008-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="63008-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="63008-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="63008-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="63008-128">DLL</span><span class="sxs-lookup"><span data-stu-id="63008-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63008-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63008-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="63008-130">IID</span><span class="sxs-lookup"><span data-stu-id="63008-130">IID</span></span><br/>                      | <span data-ttu-id="63008-131">IID \_ IADsDNWithBinary est défini en tant que 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="63008-131">IID\_IADsDNWithBinary is defined as 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="63008-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63008-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63008-133">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="63008-133">**IADsDNWithBinary**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[<span data-ttu-id="63008-134">**\_DN ADS \_ avec \_ binaire**</span><span class="sxs-lookup"><span data-stu-id="63008-134">**ADS\_DN\_WITH\_BINARY**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 





