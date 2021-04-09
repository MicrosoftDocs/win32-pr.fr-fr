---
description: Compare deux chaînes Unicode.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Fonction RtlCompareUnicodeString (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861057"
---
# <a name="rtlcompareunicodestring-function"></a><span data-ttu-id="ce86c-103">RtlCompareUnicodeString fonction)</span><span class="sxs-lookup"><span data-stu-id="ce86c-103">RtlCompareUnicodeString function</span></span>

<span data-ttu-id="ce86c-104">Compare deux chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce86c-104">Compares two Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce86c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce86c-105">Syntax</span></span>


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="ce86c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce86c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce86c-107">*Chaîne1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce86c-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce86c-108">Pointeur vers la première chaîne.</span><span class="sxs-lookup"><span data-stu-id="ce86c-108">Pointer to the first string.</span></span>

</dd> <dt>

<span data-ttu-id="ce86c-109">*Chaîne2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce86c-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce86c-110">Pointeur vers la deuxième chaîne.</span><span class="sxs-lookup"><span data-stu-id="ce86c-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="ce86c-111">*CaseInSensitive* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce86c-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce86c-112">Si la **valeur est true**, la casse doit être ignorée lors de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="ce86c-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce86c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce86c-113">Return value</span></span>

<span data-ttu-id="ce86c-114">Valeur signée qui donne les résultats de la comparaison :</span><span class="sxs-lookup"><span data-stu-id="ce86c-114">A signed value that gives the results of the comparison:</span></span>



| <span data-ttu-id="ce86c-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ce86c-115">Return code</span></span>                                                                               | <span data-ttu-id="ce86c-116">Description</span><span class="sxs-lookup"><span data-stu-id="ce86c-116">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="ce86c-117"><dt>**Nuls**</dt></span><span class="sxs-lookup"><span data-stu-id="ce86c-117"><dt>**Zero**</dt></span></span> </dl>       | <span data-ttu-id="ce86c-118">*Chaîne1* est égal à *Chaîne2*.</span><span class="sxs-lookup"><span data-stu-id="ce86c-118">*String1* equals *String2*.</span></span><br/>          |
| <dl> <span data-ttu-id="ce86c-119"><dt>**< zéro**</dt></span><span class="sxs-lookup"><span data-stu-id="ce86c-119"><dt>**< Zero**</dt></span></span> </dl>  | <span data-ttu-id="ce86c-120">*Chaîne1* est inférieur à *Chaîne2*.</span><span class="sxs-lookup"><span data-stu-id="ce86c-120">*String1* is less than *String2*.</span></span><br/>    |
| <dl> <span data-ttu-id="ce86c-121"><dt>**> zéro**</dt></span><span class="sxs-lookup"><span data-stu-id="ce86c-121"><dt>**> Zero** </dt></span></span> </dl> | <span data-ttu-id="ce86c-122">*Chaîne1* est supérieur à *Chaîne2*.</span><span class="sxs-lookup"><span data-stu-id="ce86c-122">*String1* is greater than *String2*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ce86c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce86c-123">Requirements</span></span>



| <span data-ttu-id="ce86c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce86c-124">Requirement</span></span> | <span data-ttu-id="ce86c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce86c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce86c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce86c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ce86c-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce86c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="ce86c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce86c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ce86c-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce86c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="ce86c-130">Plateforme cible</span><span class="sxs-lookup"><span data-stu-id="ce86c-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="ce86c-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="ce86c-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="ce86c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce86c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce86c-133"><dt>WDM. h (inclure WDM. h, Ntddk. h ou Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce86c-133"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="ce86c-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce86c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce86c-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce86c-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ce86c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ce86c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce86c-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce86c-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="ce86c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce86c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce86c-139">**RtlCompareString**</span><span class="sxs-lookup"><span data-stu-id="ce86c-139">**RtlCompareString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[<span data-ttu-id="ce86c-140">**RtlEqualString**</span><span class="sxs-lookup"><span data-stu-id="ce86c-140">**RtlEqualString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
