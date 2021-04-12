---
title: Méthodes de propriété IADsHold (IADs. h)
description: La méthode Property de l’interface IADsHold définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsHold ADSI
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae2499efb461e6c13397fdaef75e515f0a1a21a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105136"
---
# <a name="iadshold-property-methods"></a><span data-ttu-id="11587-105">Méthodes de propriété IADsHold</span><span class="sxs-lookup"><span data-stu-id="11587-105">IADsHold Property Methods</span></span>

<span data-ttu-id="11587-106">La méthode Property de l’interface [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="11587-106">The property method of the [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) interface sets the property described in the following table.</span></span> <span data-ttu-id="11587-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="11587-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="11587-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="11587-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="11587-109">**Montant**</span><span class="sxs-lookup"><span data-stu-id="11587-109">**Amount**</span></span>
<span data-ttu-id="11587-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="11587-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="11587-111">Montant des frais perçus par l’utilisateur pour la période en attente, tandis que le serveur vérifie le solde du compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="11587-111">The amount of charges levied against the user for the period on hold while the server checks the account balance of the user.</span></span>

<dt>

<span data-ttu-id="11587-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="11587-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="11587-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="11587-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="11587-114">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="11587-114">**ObjectName**</span></span>
<span data-ttu-id="11587-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="11587-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="11587-116">Nom de l’objet représentant un utilisateur en attente.</span><span class="sxs-lookup"><span data-stu-id="11587-116">The name of the object representing a user on hold.</span></span>

<dt>

<span data-ttu-id="11587-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="11587-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="11587-118">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="11587-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="11587-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11587-119">Requirements</span></span>



| <span data-ttu-id="11587-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11587-120">Requirement</span></span> | <span data-ttu-id="11587-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="11587-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11587-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11587-122">Minimum supported client</span></span><br/> | <span data-ttu-id="11587-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11587-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11587-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11587-124">Minimum supported server</span></span><br/> | <span data-ttu-id="11587-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11587-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11587-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="11587-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="11587-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="11587-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="11587-128">DLL</span><span class="sxs-lookup"><span data-stu-id="11587-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11587-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11587-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="11587-130">IID</span><span class="sxs-lookup"><span data-stu-id="11587-130">IID</span></span><br/>                      | <span data-ttu-id="11587-131">IID \_ IADsHold est défini en tant que B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="11587-131">IID\_IADsHold is defined as B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="11587-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11587-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11587-133">**IADsHold**</span><span class="sxs-lookup"><span data-stu-id="11587-133">**IADsHold**</span></span>](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





