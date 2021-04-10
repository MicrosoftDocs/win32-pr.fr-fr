---
description: Termine le traitement pour créer une image décodée.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'IDirect3DDXVADevice9 :: EndFrame, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114227"
---
# <a name="idirect3ddxvadevice9endframe-method"></a><span data-ttu-id="e6a74-103">IDirect3DDXVADevice9 :: EndFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="e6a74-103">IDirect3DDXVADevice9::EndFrame method</span></span>

<span data-ttu-id="e6a74-104">Termine le traitement pour créer une image décodée.</span><span class="sxs-lookup"><span data-stu-id="e6a74-104">Ends the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a74-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6a74-105">Syntax</span></span>


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a><span data-ttu-id="e6a74-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6a74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a74-107">*SizeMiscData*</span><span class="sxs-lookup"><span data-stu-id="e6a74-107">*SizeMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a74-108">Taille de la mémoire tampon spécifiée par *pMiscData*, en octets.</span><span class="sxs-lookup"><span data-stu-id="e6a74-108">The size of the buffer specified by *pMiscData*, in bytes.</span></span> <span data-ttu-id="e6a74-109">La valeur doit être 2.</span><span class="sxs-lookup"><span data-stu-id="e6a74-109">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="e6a74-110">*pMiscData*</span><span class="sxs-lookup"><span data-stu-id="e6a74-110">*pMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a74-111">Pointeur vers une mémoire tampon qui contient des données pour l’accélérateur vidéo.</span><span class="sxs-lookup"><span data-stu-id="e6a74-111">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="e6a74-112">Cette mémoire tampon doit contenir le même index de frames que celui qui a été passé à la méthode [**IDirect3DDXVADevice9 :: BeginFrame**](idirect3ddxvadevice9-beginframe.md) dans le paramètre *pInputData* .</span><span class="sxs-lookup"><span data-stu-id="e6a74-112">This buffer must contain the same frame index that was passed to the [**IDirect3DDXVADevice9::BeginFrame**](idirect3ddxvadevice9-beginframe.md) method in the *pInputData* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a74-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6a74-113">Return value</span></span>

<span data-ttu-id="e6a74-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e6a74-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6a74-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6a74-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a74-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6a74-116">Requirements</span></span>



| <span data-ttu-id="e6a74-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6a74-117">Requirement</span></span> | <span data-ttu-id="e6a74-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6a74-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e6a74-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a74-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a74-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6a74-120">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6a74-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a74-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a74-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6a74-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e6a74-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6a74-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6a74-124"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a74-124"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a74-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6a74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a74-126">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="e6a74-126">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




