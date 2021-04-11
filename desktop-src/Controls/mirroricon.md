---
title: MirrorIcon fonction)
description: Inverse (met en miroir) les icônes afin qu’elles s’affichent correctement sur un contexte de périphérique en miroir.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Contrôles Windows de la fonction MirrorIcon
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032489"
---
# <a name="mirroricon-function"></a><span data-ttu-id="55ac3-104">MirrorIcon fonction)</span><span class="sxs-lookup"><span data-stu-id="55ac3-104">MirrorIcon function</span></span>

<span data-ttu-id="55ac3-105">\[**MirrorIcon** est disponible via Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="55ac3-105">\[**MirrorIcon** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="55ac3-106">Il peut être modifié ou non disponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="55ac3-106">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="55ac3-107">Inverse (met en miroir) les icônes afin qu’elles s’affichent correctement sur un contexte de périphérique en miroir.</span><span class="sxs-lookup"><span data-stu-id="55ac3-107">Reverses (mirrors) icons so that they are displayed correctly on a mirrored device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ac3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55ac3-108">Syntax</span></span>


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a><span data-ttu-id="55ac3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55ac3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ac3-110">*phIconSmall* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="55ac3-110">*phIconSmall* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55ac3-111">Type : \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="55ac3-111">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="55ac3-112">Pointeur vers le handle d’icône qui fait référence à une petite version d’une icône.</span><span class="sxs-lookup"><span data-stu-id="55ac3-112">A pointer to the icon handle that references a small version of an icon.</span></span>

</dd> <dt>

<span data-ttu-id="55ac3-113">_phIconLarge \* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="55ac3-113">_phIconLarge\* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55ac3-114">Type : \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="55ac3-114">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="55ac3-115">Pointeur vers le handle d’icône qui fait référence à une grande version d’une icône.</span><span class="sxs-lookup"><span data-stu-id="55ac3-115">A pointer to the icon handle that references a large version of an icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ac3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55ac3-116">Return value</span></span>

<span data-ttu-id="55ac3-117">Type : _ *[**bool**](/windows/desktop/WinProg/windows-data-types)*\*</span><span class="sxs-lookup"><span data-stu-id="55ac3-117">Type: _ *[**BOOL**](/windows/desktop/WinProg/windows-data-types)*\*</span></span>

<span data-ttu-id="55ac3-118">**True** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="55ac3-118">**TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="55ac3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="55ac3-119">Remarks</span></span>

<span data-ttu-id="55ac3-120">**MirrorIcon** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="55ac3-120">**MirrorIcon** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="55ac3-121">Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 414 de ComCtl32.dll pour obtenir un pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="55ac3-121">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 414 from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="55ac3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55ac3-122">Requirements</span></span>



| <span data-ttu-id="55ac3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55ac3-123">Requirement</span></span> | <span data-ttu-id="55ac3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="55ac3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ac3-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55ac3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="55ac3-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55ac3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="55ac3-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55ac3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="55ac3-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55ac3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="55ac3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="55ac3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55ac3-130"><dt>Comctl32.dll (version 5,81 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="55ac3-130"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

