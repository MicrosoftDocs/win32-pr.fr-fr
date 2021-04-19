---
title: Méthodes de propriété IADsLargeInteger (IADs. h)
description: Les méthodes de propriété de l’interface IADsLargeInteger obtiennent et définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsLargeInteger ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 097e9ae7387658f983c691e56e4f90ba40dea407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509338"
---
# <a name="iadslargeinteger-property-methods"></a><span data-ttu-id="4958d-105">Méthodes de propriété IADsLargeInteger</span><span class="sxs-lookup"><span data-stu-id="4958d-105">IADsLargeInteger Property Methods</span></span>

<span data-ttu-id="4958d-106">Les méthodes de propriété de l’interface [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) obtiennent et définissent les propriétés décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4958d-106">The property methods of the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface get and set the properties described in the following table.</span></span> <span data-ttu-id="4958d-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4958d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4958d-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4958d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4958d-109">**HighPart**</span><span class="sxs-lookup"><span data-stu-id="4958d-109">**HighPart**</span></span>
<span data-ttu-id="4958d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4958d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4958d-111">Partie haute de l’entier.</span><span class="sxs-lookup"><span data-stu-id="4958d-111">The high part of the integer.</span></span>

<dt>

<span data-ttu-id="4958d-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4958d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4958d-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="4958d-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4958d-114">**LowPart**</span><span class="sxs-lookup"><span data-stu-id="4958d-114">**LowPart**</span></span>
<span data-ttu-id="4958d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4958d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="4958d-116">Partie basse de l’entier.</span><span class="sxs-lookup"><span data-stu-id="4958d-116">The low part of the integer.</span></span>

<dt>

<span data-ttu-id="4958d-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="4958d-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4958d-118">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="4958d-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="4958d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="4958d-119">Remarks</span></span>

<span data-ttu-id="4958d-120">Si largeInt est de type **LargeInteger** , sa valeur est spécifiée par les valeurs de **HighPart** et **LowPart** selon la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="4958d-120">If largeInt is of the **LargeInteger** type, its value is specified by those of **HighPart** and **LowPart** according to the following formula.</span></span>


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a><span data-ttu-id="4958d-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="4958d-121">Examples</span></span>

<span data-ttu-id="4958d-122">L’exemple de code Visual Basic suivant affecte à un grand entier la valeur 43937327281.</span><span class="sxs-lookup"><span data-stu-id="4958d-122">The following Visual Basic code example sets a large integer to 43937327281.</span></span>


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a><span data-ttu-id="4958d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4958d-123">Requirements</span></span>



| <span data-ttu-id="4958d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4958d-124">Requirement</span></span> | <span data-ttu-id="4958d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4958d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4958d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4958d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4958d-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4958d-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4958d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4958d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4958d-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4958d-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4958d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="4958d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4958d-131"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4958d-131"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4958d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4958d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4958d-133"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4958d-133"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4958d-134">IID</span><span class="sxs-lookup"><span data-stu-id="4958d-134">IID</span></span><br/>                      | <span data-ttu-id="4958d-135">IID \_ IADsLargeInteger est défini en tant que 9068270B-0939-11D1-8BE1-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="4958d-135">IID\_IADsLargeInteger is defined as 9068270B-0939-11D1-8BE1-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="4958d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4958d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4958d-137">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="4958d-137">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





