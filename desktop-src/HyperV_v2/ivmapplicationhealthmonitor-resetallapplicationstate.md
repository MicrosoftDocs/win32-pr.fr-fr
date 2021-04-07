---
description: Réinitialise l’état d’intégrité de toutes les applications d’une machine virtuelle.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'IVmApplicationHealthMonitor :: ResetAllApplicationState, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863566"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a><span data-ttu-id="4c58e-103">IVmApplicationHealthMonitor :: ResetAllApplicationState, méthode</span><span class="sxs-lookup"><span data-stu-id="4c58e-103">IVmApplicationHealthMonitor::ResetAllApplicationState method</span></span>

<span data-ttu-id="4c58e-104">Réinitialise l’état d’intégrité de toutes les applications d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4c58e-104">Resets the health state for all applications in a virtual machine.</span></span> <span data-ttu-id="4c58e-105">En cas de réussite, l’état d’intégrité de toutes les applications analysées est défini sur **ApplicationStateHealthy**.</span><span class="sxs-lookup"><span data-stu-id="4c58e-105">If successful, the health state for all monitored applications will be set to **ApplicationStateHealthy**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c58e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c58e-106">Syntax</span></span>


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a><span data-ttu-id="4c58e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c58e-107">Parameters</span></span>

<span data-ttu-id="4c58e-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4c58e-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c58e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c58e-109">Return value</span></span>

<span data-ttu-id="4c58e-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4c58e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c58e-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c58e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c58e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4c58e-112">Remarks</span></span>

<span data-ttu-id="4c58e-113">Pour utiliser cet élément de programmation, les composants d’intégration Windows 8 doivent être installés sur l’ordinateur virtuel dans lequel l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="4c58e-113">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c58e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c58e-114">Requirements</span></span>



| <span data-ttu-id="4c58e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c58e-115">Requirement</span></span> | <span data-ttu-id="4c58e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c58e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c58e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c58e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4c58e-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c58e-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="4c58e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c58e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4c58e-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c58e-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4c58e-121">Version</span><span class="sxs-lookup"><span data-stu-id="4c58e-121">Version</span></span><br/>                  | <span data-ttu-id="4c58e-122">Composants d’intégration pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="4c58e-122">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="4c58e-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="4c58e-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c58e-124"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c58e-124"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c58e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c58e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c58e-126">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="4c58e-126">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




