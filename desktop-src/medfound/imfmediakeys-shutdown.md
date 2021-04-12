---
description: 'En savoir plus sur : IMFMediaKeys :: Shutdown, méthode'
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: 'IMFMediaKeys :: Shutdown, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9fcee861b53aaf0c9fda2c6265f50fcee60f674c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321602"
---
# <a name="imfmediakeysshutdown-method"></a><span data-ttu-id="91622-103">IMFMediaKeys :: Shutdown, méthode</span><span class="sxs-lookup"><span data-stu-id="91622-103">IMFMediaKeys::Shutdown method</span></span>

## <a name="syntax"></a><span data-ttu-id="91622-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91622-104">Syntax</span></span>


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="91622-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91622-105">Parameters</span></span>

<span data-ttu-id="91622-106">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="91622-106">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91622-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91622-107">Return value</span></span>

<span data-ttu-id="91622-108">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="91622-108">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="91622-109">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="91622-109">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="91622-110">Notes</span><span class="sxs-lookup"><span data-stu-id="91622-110">Remarks</span></span>

<span data-ttu-id="91622-111">L' **arrêt** doit être appelé par l’application avant la version finale.</span><span class="sxs-lookup"><span data-stu-id="91622-111">**Shutdown** should be called by the application before final release.</span></span> <span data-ttu-id="91622-112">La référence CDM (Content decryption module) et toutes les autres ressources sont publiées à ce stade.</span><span class="sxs-lookup"><span data-stu-id="91622-112">The Content Decryption Module (CDM) reference and any other resources is released at this point.</span></span> <span data-ttu-id="91622-113">Toutefois, les sessions associées ne sont pas libérées ou fermées.</span><span class="sxs-lookup"><span data-stu-id="91622-113">However, related sessions are not freed or closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="91622-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91622-114">Requirements</span></span>



| <span data-ttu-id="91622-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91622-115">Requirement</span></span> | <span data-ttu-id="91622-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="91622-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91622-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91622-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91622-118">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91622-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="91622-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91622-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91622-120">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91622-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="91622-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="91622-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91622-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91622-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91622-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91622-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91622-124">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="91622-124">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




