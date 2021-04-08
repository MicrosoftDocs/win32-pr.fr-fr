---
title: Méthodes de propriété IADsNetAddress (IADs. h)
description: La méthode Property de l’interface IADsNetAddress définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsNetAddress ADSI
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073033c703db8eaa55b05058d6d2bbc3d3167f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742692"
---
# <a name="iadsnetaddress-property-methods"></a><span data-ttu-id="074c9-105">Méthodes de propriété IADsNetAddress</span><span class="sxs-lookup"><span data-stu-id="074c9-105">IADsNetAddress Property Methods</span></span>

<span data-ttu-id="074c9-106">La méthode Property de l’interface [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="074c9-106">The property method of the [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) interface sets the property described in the following table.</span></span> <span data-ttu-id="074c9-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="074c9-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="074c9-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="074c9-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="074c9-109">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="074c9-109">**Address**</span></span>
<span data-ttu-id="074c9-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="074c9-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="074c9-111">Adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="074c9-111">A network address.</span></span>

<dt>

<span data-ttu-id="074c9-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="074c9-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="074c9-113">Type de données de script : **variante**</span><span class="sxs-lookup"><span data-stu-id="074c9-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="074c9-114">**Typedadresse**</span><span class="sxs-lookup"><span data-stu-id="074c9-114">**AddressType**</span></span>
<span data-ttu-id="074c9-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="074c9-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="074c9-116">Type de protocole de communication.</span><span class="sxs-lookup"><span data-stu-id="074c9-116">A type of communication protocols.</span></span>

<dt>

<span data-ttu-id="074c9-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="074c9-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="074c9-118">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="074c9-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="074c9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="074c9-119">Requirements</span></span>



| <span data-ttu-id="074c9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="074c9-120">Requirement</span></span> | <span data-ttu-id="074c9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="074c9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="074c9-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="074c9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="074c9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="074c9-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="074c9-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="074c9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="074c9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="074c9-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="074c9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="074c9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="074c9-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="074c9-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="074c9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="074c9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="074c9-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="074c9-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="074c9-130">IID</span><span class="sxs-lookup"><span data-stu-id="074c9-130">IID</span></span><br/>                      | <span data-ttu-id="074c9-131">IID \_ IADsNetAddress est défini en tant que B21A50A9-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="074c9-131">IID\_IADsNetAddress is defined as B21A50A9-4080-11D1-A3AC-00C04FB950DC</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="074c9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="074c9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074c9-133">**IADsNetAddress**</span><span class="sxs-lookup"><span data-stu-id="074c9-133">**IADsNetAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[<span data-ttu-id="074c9-134">**ADRESSE de publicité ADS \_**</span><span class="sxs-lookup"><span data-stu-id="074c9-134">**ADS\_NETADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 





