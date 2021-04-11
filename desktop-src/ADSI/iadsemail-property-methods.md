---
title: Méthodes de propriété IADsEmail (IADs. h)
description: La méthode Property de l’interface IADsEmail définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsEmail ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385068"
---
# <a name="iadsemail-property-methods"></a><span data-ttu-id="24eb5-105">Méthodes de propriété IADsEmail</span><span class="sxs-lookup"><span data-stu-id="24eb5-105">IADsEmail Property Methods</span></span>

<span data-ttu-id="24eb5-106">La méthode Property de l’interface [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) définit la propriété décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="24eb5-106">The property method of the [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) interface sets the property described in the following table.</span></span> <span data-ttu-id="24eb5-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="24eb5-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="24eb5-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="24eb5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="24eb5-109">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="24eb5-109">**Address**</span></span>
<span data-ttu-id="24eb5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="24eb5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="24eb5-111">Adresse e-mail de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="24eb5-111">The email address of the user.</span></span>

<dt>

<span data-ttu-id="24eb5-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="24eb5-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="24eb5-113">Type de données de script : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="24eb5-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="24eb5-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="24eb5-114">**Type**</span></span>
<span data-ttu-id="24eb5-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="24eb5-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="24eb5-116">Type du message électronique.</span><span class="sxs-lookup"><span data-stu-id="24eb5-116">The type of the email message.</span></span>

<dt>

<span data-ttu-id="24eb5-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="24eb5-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="24eb5-118">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="24eb5-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="24eb5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24eb5-119">Requirements</span></span>



| <span data-ttu-id="24eb5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24eb5-120">Requirement</span></span> | <span data-ttu-id="24eb5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="24eb5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24eb5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24eb5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="24eb5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24eb5-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24eb5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24eb5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="24eb5-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24eb5-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24eb5-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="24eb5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="24eb5-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="24eb5-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="24eb5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="24eb5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24eb5-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24eb5-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="24eb5-130">IID</span><span class="sxs-lookup"><span data-stu-id="24eb5-130">IID</span></span><br/>                      | <span data-ttu-id="24eb5-131">IID \_ IADsEmail est défini en tant que 97AF011A-478E-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="24eb5-131">IID\_IADsEmail is defined as 97AF011A-478E-11D1-A3B4-00C04FB950DC</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="24eb5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24eb5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24eb5-133">**IADsEmail**</span><span class="sxs-lookup"><span data-stu-id="24eb5-133">**IADsEmail**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[<span data-ttu-id="24eb5-134">**\_E-mail ads**</span><span class="sxs-lookup"><span data-stu-id="24eb5-134">**ADS\_EMAIL**</span></span>](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 





