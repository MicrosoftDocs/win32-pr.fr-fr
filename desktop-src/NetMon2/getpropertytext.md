---
description: La fonction GetPropertyText retourne un pointeur vers le texte de la propriété.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: GetPropertyText, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318077"
---
# <a name="getpropertytext-function"></a><span data-ttu-id="553ab-103">GetPropertyText fonction)</span><span class="sxs-lookup"><span data-stu-id="553ab-103">GetPropertyText function</span></span>

<span data-ttu-id="553ab-104">La fonction **GetPropertyText** retourne un pointeur vers le texte de la propriété.</span><span class="sxs-lookup"><span data-stu-id="553ab-104">The **GetPropertyText** function returns a pointer to the property text.</span></span>

## <a name="syntax"></a><span data-ttu-id="553ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="553ab-105">Syntax</span></span>


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="553ab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="553ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="553ab-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="553ab-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553ab-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="553ab-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="553ab-109">*lpPI* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="553ab-109">*lpPI* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553ab-110">Pointeur vers une instance de propriété.</span><span class="sxs-lookup"><span data-stu-id="553ab-110">Pointer to a property instance.</span></span>

</dd> <dt>

<span data-ttu-id="553ab-111">*szBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="553ab-111">*szBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553ab-112">Pointeur désignant la chaîne de texte de la propriété.</span><span class="sxs-lookup"><span data-stu-id="553ab-112">Pointer to the property text string.</span></span>

</dd> <dt>

<span data-ttu-id="553ab-113">*BufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="553ab-113">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553ab-114">Taille de la mémoire tampon de la chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="553ab-114">Size of the text string buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="553ab-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="553ab-115">Return value</span></span>

<span data-ttu-id="553ab-116">Si la fonction réussit, la valeur de retour est un pointeur vers le texte de la propriété.</span><span class="sxs-lookup"><span data-stu-id="553ab-116">If the function is successful, the return value is a pointer to the property text.</span></span>

<span data-ttu-id="553ab-117">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="553ab-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="553ab-118">Notes</span><span class="sxs-lookup"><span data-stu-id="553ab-118">Remarks</span></span>

<span data-ttu-id="553ab-119">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetPropertyText** .</span><span class="sxs-lookup"><span data-stu-id="553ab-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyText** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="553ab-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="553ab-120">Requirements</span></span>



| <span data-ttu-id="553ab-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="553ab-121">Requirement</span></span> | <span data-ttu-id="553ab-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="553ab-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="553ab-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="553ab-123">Minimum supported client</span></span><br/> | <span data-ttu-id="553ab-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="553ab-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="553ab-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="553ab-125">Minimum supported server</span></span><br/> | <span data-ttu-id="553ab-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="553ab-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="553ab-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="553ab-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="553ab-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="553ab-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="553ab-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="553ab-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="553ab-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="553ab-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="553ab-131">DLL</span><span class="sxs-lookup"><span data-stu-id="553ab-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="553ab-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="553ab-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




