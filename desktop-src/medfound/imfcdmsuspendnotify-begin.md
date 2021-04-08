---
description: Indique que le processus de suspension démarre et que les ressources doivent être mises dans un état cohérent.
ms.assetid: 5cf3d249-3d8b-4596-9d8b-e7b95a270eff
title: 'IMFCdmSuspendNotify :: Begin, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.Begin
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 84453a6c846e88a9d6e6c32c5253d97d36e89c7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749661"
---
# <a name="imfcdmsuspendnotifybegin-method"></a><span data-ttu-id="ae396-103">IMFCdmSuspendNotify :: Begin, méthode</span><span class="sxs-lookup"><span data-stu-id="ae396-103">IMFCdmSuspendNotify::Begin method</span></span>

<span data-ttu-id="ae396-104">Indique que le processus de suspension démarre et que les ressources doivent être mises dans un état cohérent.</span><span class="sxs-lookup"><span data-stu-id="ae396-104">Indicates that the suspend process is starting and resources should be brought into a consistent state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae396-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae396-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="ae396-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae396-106">Parameters</span></span>

<span data-ttu-id="ae396-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ae396-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae396-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae396-108">Return value</span></span>

<span data-ttu-id="ae396-109">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ae396-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ae396-110">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae396-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae396-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae396-111">Requirements</span></span>



| <span data-ttu-id="ae396-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae396-112">Requirement</span></span> | <span data-ttu-id="ae396-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae396-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae396-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae396-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ae396-115">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae396-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ae396-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae396-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ae396-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae396-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ae396-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="ae396-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae396-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae396-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae396-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae396-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae396-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="ae396-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




