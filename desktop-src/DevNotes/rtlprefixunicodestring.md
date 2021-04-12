---
description: Compare deux chaînes Unicode pour déterminer si une chaîne est un préfixe de l’autre.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: RtlPrefixUnicodeString, fonction (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483136"
---
# <a name="rtlprefixunicodestring-function"></a><span data-ttu-id="fb6ec-103">RtlPrefixUnicodeString fonction)</span><span class="sxs-lookup"><span data-stu-id="fb6ec-103">RtlPrefixUnicodeString function</span></span>

<span data-ttu-id="fb6ec-104">Compare deux chaînes Unicode pour déterminer si une chaîne est un préfixe de l’autre.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-104">Compares two Unicode strings to determine whether one string is a prefix of the other.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb6ec-105">Syntax</span></span>


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="fb6ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb6ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb6ec-107">*Chaîne1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb6ec-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ec-108">Pointeur vers la première chaîne, qui peut être un préfixe de la chaîne Unicode mise en mémoire tampon à *Chaîne2*.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-108">Pointer to the first string, which might be a prefix of the buffered Unicode string at *String2*.</span></span>

</dd> <dt>

<span data-ttu-id="fb6ec-109">*Chaîne2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb6ec-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ec-110">Pointeur vers la deuxième chaîne.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="fb6ec-111">*CaseInSensitive* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb6ec-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ec-112">Si la **valeur est true**, la casse doit être ignorée lors de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb6ec-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb6ec-113">Return value</span></span>

<span data-ttu-id="fb6ec-114">**True** si *Chaîne1* est un préfixe de *Chaîne2*.</span><span class="sxs-lookup"><span data-stu-id="fb6ec-114">**TRUE** if *String1* is a prefix of *String2*.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6ec-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb6ec-115">Requirements</span></span>



| <span data-ttu-id="fb6ec-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb6ec-116">Requirement</span></span> | <span data-ttu-id="fb6ec-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb6ec-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6ec-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb6ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fb6ec-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb6ec-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="fb6ec-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb6ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fb6ec-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb6ec-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="fb6ec-122">Plateforme cible</span><span class="sxs-lookup"><span data-stu-id="fb6ec-122">Target platform</span></span><br/>          | <dl> <span data-ttu-id="fb6ec-123"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ec-123"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="fb6ec-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb6ec-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb6ec-125"><dt>Ntddk. h (inclure Ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ec-125"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="fb6ec-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fb6ec-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb6ec-127"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ec-127"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fb6ec-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fb6ec-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb6ec-129"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ec-129"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="fb6ec-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb6ec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6ec-131">**RtlCompareUnicodeString**</span><span class="sxs-lookup"><span data-stu-id="fb6ec-131">**RtlCompareUnicodeString**</span></span>](rtlcompareunicodestring.md)
</dt> </dl>

 

 




