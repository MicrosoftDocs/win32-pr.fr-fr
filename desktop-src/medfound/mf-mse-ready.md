---
description: Définit les différents États prêts de l’extension de source de média.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: Énumération MF_MSE_READY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865585"
---
# <a name="mf_mse_ready-enumeration"></a><span data-ttu-id="37034-103">\_ \_ Énumération compatible MF MSE</span><span class="sxs-lookup"><span data-stu-id="37034-103">MF\_MSE\_READY enumeration</span></span>

<span data-ttu-id="37034-104">Définit les différents États prêts de l’extension de source de média.</span><span class="sxs-lookup"><span data-stu-id="37034-104">Defines the different ready states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="37034-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37034-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a><span data-ttu-id="37034-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="37034-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="37034-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF \_ MSE \_ prêt \_ fermé**</span><span class="sxs-lookup"><span data-stu-id="37034-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF\_MSE\_READY\_CLOSED**</span></span>
</dt> <dd>

<span data-ttu-id="37034-108">La source du média est fermée.</span><span class="sxs-lookup"><span data-stu-id="37034-108">The media source is closed.</span></span>

</dd> <dt>

<span data-ttu-id="37034-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**\_ouverture de MSE MF \_ \_ ouverte**</span><span class="sxs-lookup"><span data-stu-id="37034-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF\_MSE\_READY\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="37034-110">La source du média est ouverte.</span><span class="sxs-lookup"><span data-stu-id="37034-110">The media source is open.</span></span>

</dd> <dt>

<span data-ttu-id="37034-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**fin de la fermeture de \_ MSE MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="37034-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF\_MSE\_READY\_ENDED**</span></span>
</dt> <dd>

<span data-ttu-id="37034-112">La source du média est terminée.</span><span class="sxs-lookup"><span data-stu-id="37034-112">The media source is ended.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37034-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37034-113">Requirements</span></span>



| <span data-ttu-id="37034-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37034-114">Requirement</span></span> | <span data-ttu-id="37034-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="37034-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37034-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37034-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37034-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37034-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="37034-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37034-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37034-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37034-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="37034-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="37034-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37034-121"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="37034-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37034-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37034-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37034-123">Énumérations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37034-123">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




