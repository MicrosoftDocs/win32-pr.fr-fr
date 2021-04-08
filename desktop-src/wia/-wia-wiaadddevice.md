---
description: La fonction WiaAddDevice appelle l’interface utilisateur de l’Assistant Installation du scanneur et de l’appareil photo. Cela équivaut à exécuter &\# 0034 ; rundll32.exe sti \_ci.dll AddDevice&\# 0034 ; à partir de l’invite de commandes.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Fonction WiaAddDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751749"
---
# <a name="wiaadddevice-function"></a><span data-ttu-id="e108a-104">WiaAddDevice fonction)</span><span class="sxs-lookup"><span data-stu-id="e108a-104">WiaAddDevice function</span></span>

<span data-ttu-id="e108a-105">La fonction **WiaAddDevice** appelle l’interface utilisateur de l’Assistant Installation du scanneur et de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="e108a-105">The **WiaAddDevice** function invokes the Scanner and Camera Installation Wizard UI.</span></span> <span data-ttu-id="e108a-106">Cela équivaut à exécuter « rundll32.exe STI \_ci.dll AddDevice » à partir de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="e108a-106">It is equivalent to running "rundll32.exe sti\_ci.dll AddDevice" from the command prompt.</span></span>

## <a name="syntax"></a><span data-ttu-id="e108a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e108a-107">Syntax</span></span>


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a><span data-ttu-id="e108a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e108a-108">Parameters</span></span>

<span data-ttu-id="e108a-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="e108a-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e108a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e108a-110">Return value</span></span>

<span data-ttu-id="e108a-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e108a-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e108a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e108a-112">Remarks</span></span>

<span data-ttu-id="e108a-113">Cette fonction doit être appelée avec les informations d’identification d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="e108a-113">This function should be called with administrator credentials.</span></span> <span data-ttu-id="e108a-114">En cas d’exécution sous le contrôle de compte d’utilisateur (LUA), le processus doit être élevé.</span><span class="sxs-lookup"><span data-stu-id="e108a-114">When running under User Account Control (LUA), the process should be elevated.</span></span>

## <a name="requirements"></a><span data-ttu-id="e108a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e108a-115">Requirements</span></span>



| <span data-ttu-id="e108a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e108a-116">Requirement</span></span> | <span data-ttu-id="e108a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e108a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e108a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e108a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e108a-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e108a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e108a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e108a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e108a-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e108a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e108a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e108a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e108a-123"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e108a-123"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="e108a-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e108a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="e108a-125"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e108a-125"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e108a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e108a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e108a-127">**InstallWiaDevice**</span><span class="sxs-lookup"><span data-stu-id="e108a-127">**InstallWiaDevice**</span></span>](-wia-installwiadevice.md)
</dt> </dl>

 

 




