---
title: Énumération DODownloadState
description: Spécifie l’ID de l’état de téléchargement actuel, qui fait partie de la structure **DO_DOWNLOAD_STATUS** .
keywords:
- Énumération DODownloadState, DODownloadState
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509086"
---
# <a name="dodownloadstate-enumeration"></a><span data-ttu-id="15f41-104">Énumération DODownloadState</span><span class="sxs-lookup"><span data-stu-id="15f41-104">DODownloadState enumeration</span></span>

<span data-ttu-id="15f41-105">L’énumération **DODownloadState** spécifie l’ID de l’état de téléchargement actuel, qui fait partie de la structure **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="15f41-105">The **DODownloadState** enumeration specifies the ID of the current download state, which is part of the **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f41-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15f41-106">Syntax</span></span>

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a><span data-ttu-id="15f41-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="15f41-107">Constants</span></span>

| <span data-ttu-id="15f41-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15f41-108">Requirement</span></span> | <span data-ttu-id="15f41-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f41-109">Value</span></span> |
|-|-|
| <span data-ttu-id="15f41-110">DODownloadState_Created</span><span class="sxs-lookup"><span data-stu-id="15f41-110">DODownloadState_Created</span></span> | <span data-ttu-id="15f41-111">Le téléchargement de l’objet est créé mais n’a pas encore démarré.</span><span class="sxs-lookup"><span data-stu-id="15f41-111">Download object is created but hasn't been started yet.</span></span> |
| <span data-ttu-id="15f41-112">DODownloadState_Transferring</span><span class="sxs-lookup"><span data-stu-id="15f41-112">DODownloadState_Transferring</span></span> | <span data-ttu-id="15f41-113">Le téléchargement est en cours.</span><span class="sxs-lookup"><span data-stu-id="15f41-113">Download is in progress.</span></span> |
| <span data-ttu-id="15f41-114">DODownloadState_Transferred</span><span class="sxs-lookup"><span data-stu-id="15f41-114">DODownloadState_Transferred</span></span> | <span data-ttu-id="15f41-115">Le téléchargement est transféré et peut redémarrer en téléchargeant une autre partie du fichier.</span><span class="sxs-lookup"><span data-stu-id="15f41-115">Download is transferred and can start again by downloading another portion of the file.</span></span> |
| <span data-ttu-id="15f41-116">DODownloadState_Finalized</span><span class="sxs-lookup"><span data-stu-id="15f41-116">DODownloadState_Finalized</span></span> | <span data-ttu-id="15f41-117">Le téléchargement est finalisé et ne peut pas être redémarré.</span><span class="sxs-lookup"><span data-stu-id="15f41-117">Download is finalized and cannot be started again.</span></span> |
| <span data-ttu-id="15f41-118">DODownloadState_Aborted</span><span class="sxs-lookup"><span data-stu-id="15f41-118">DODownloadState_Aborted</span></span> | <span data-ttu-id="15f41-119">Le téléchargement a été abandonné.</span><span class="sxs-lookup"><span data-stu-id="15f41-119">Download was aborted.</span></span> |
| <span data-ttu-id="15f41-120">DODownloadState_Paused</span><span class="sxs-lookup"><span data-stu-id="15f41-120">DODownloadState_Paused</span></span> | <span data-ttu-id="15f41-121">Le téléchargement a été suspendu à la demande ou en raison d’une erreur temporaire.</span><span class="sxs-lookup"><span data-stu-id="15f41-121">Download has been paused on demand or due to transient error.</span></span> |

## <a name="requirements"></a><span data-ttu-id="15f41-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15f41-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="15f41-123">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="15f41-123">**Minimum supported client**</span></span> | <span data-ttu-id="15f41-124">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15f41-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="15f41-125">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="15f41-125">**Minimum supported server**</span></span> | <span data-ttu-id="15f41-126">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15f41-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="15f41-127">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="15f41-127">**Header**</span></span> | <span data-ttu-id="15f41-128">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="15f41-128">DeliveryOptimizationDownloadTypes.h</span></span> |
