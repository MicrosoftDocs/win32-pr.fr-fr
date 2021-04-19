---
description: Fonction de rappel utilisée pour informer l’hôte de la progression des moteurs. Cela permet également à l’hôte de déterminer que le moteur est toujours en cours d’exécution.
title: 'IStatusCallback :: Status, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517165"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span data-ttu-id="b3c00-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback :: Status, méthode</span><span class="sxs-lookup"><span data-stu-id="b3c00-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback::Status method</span></span>

<span data-ttu-id="b3c00-105">Fonction de rappel utilisée pour informer l’hôte de la progression du moteur.</span><span class="sxs-lookup"><span data-stu-id="b3c00-105">A callback function used to notify the host of the engine's progress.</span></span> <span data-ttu-id="b3c00-106">Cela permet également à l’hôte de déterminer que le moteur est toujours en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b3c00-106">This also serves as a way for the host to determine that the engine is still running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c00-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3c00-107">Syntax</span></span>


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a><span data-ttu-id="b3c00-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3c00-108">Parameters</span></span>

<span data-ttu-id="b3c00-109">*dwMillisecondsElapsed* </span><span class="sxs-lookup"><span data-stu-id="b3c00-109">*dwMillisecondsElapsed* </span></span>  
<span data-ttu-id="b3c00-110">Temps écoulé depuis le dernier appel de l’État, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="b3c00-110">The time elapsed since the last call to Status, in milliseconds.</span></span>

<span data-ttu-id="b3c00-111">*dwFramesCaptured* </span><span class="sxs-lookup"><span data-stu-id="b3c00-111">*dwFramesCaptured* </span></span>  
<span data-ttu-id="b3c00-112">Nombre de frames capturés depuis le dernier appel de l’État.</span><span class="sxs-lookup"><span data-stu-id="b3c00-112">The number of frames that have been captures since the last call to Status.</span></span>

<span data-ttu-id="b3c00-113">*dwFramesElapsed* </span><span class="sxs-lookup"><span data-stu-id="b3c00-113">*dwFramesElapsed* </span></span>  
<span data-ttu-id="b3c00-114">Nombre de frames écoulés depuis le dernier appel à l’État.</span><span class="sxs-lookup"><span data-stu-id="b3c00-114">The number of frames elapsed since the last call to Status.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3c00-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3c00-115">Return value</span></span>

<span data-ttu-id="b3c00-116">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="b3c00-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="b3c00-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3c00-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c00-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3c00-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b3c00-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3c00-119">Header</span></span></p></td><td><span data-ttu-id="b3c00-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b3c00-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b3c00-121"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3c00-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b3c00-122">**IStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="b3c00-122">**IStatusCallback**</span></span>](/windows/desktop/direct3dtools/istatuscallback)

 

 
