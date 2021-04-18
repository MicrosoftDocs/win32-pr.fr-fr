---
description: Définit l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'IVmApplicationHealthMonitor :: SetApplicationState, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536350"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a><span data-ttu-id="736b8-103">IVmApplicationHealthMonitor :: SetApplicationState, méthode</span><span class="sxs-lookup"><span data-stu-id="736b8-103">IVmApplicationHealthMonitor::SetApplicationState method</span></span>

<span data-ttu-id="736b8-104">Définit l’état d’intégrité d’une application qui s’exécute sur un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="736b8-104">Sets the health state of an application that is running in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="736b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="736b8-105">Syntax</span></span>


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a><span data-ttu-id="736b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="736b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="736b8-107">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="736b8-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="736b8-108">Représentation **BSTR** du **GUID** qui identifie l’application.</span><span class="sxs-lookup"><span data-stu-id="736b8-108">A **BSTR** representation of the **GUID** that identifies the application.</span></span> <span data-ttu-id="736b8-109">L’application appelante est chargée de créer et de gérer les identificateurs qu’elle utilise pour les applications surveillées.</span><span class="sxs-lookup"><span data-stu-id="736b8-109">It is the calling application's responsibility to create and maintain the identifiers it uses for the applications being monitored.</span></span>

</dd> <dt>

<span data-ttu-id="736b8-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="736b8-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="736b8-111">Nom d’affichage de l’application.</span><span class="sxs-lookup"><span data-stu-id="736b8-111">The display name of the application.</span></span> <span data-ttu-id="736b8-112">Ce nom est utilisé dans une entrée de journal des événements d’information pour le changement d’État.</span><span class="sxs-lookup"><span data-stu-id="736b8-112">This name is used in an informational event log entry for the state change.</span></span>

</dd> <dt>

<span data-ttu-id="736b8-113">*État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="736b8-113">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="736b8-114">Valeur de l’énumération de l' [**\_ État**](application-state.md) de l’application qui spécifie le nouvel état d’intégrité de l’application.</span><span class="sxs-lookup"><span data-stu-id="736b8-114">A value of the [**APPLICATION\_STATE**](application-state.md) enumeration that specifies the new health state of the application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="736b8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="736b8-115">Return value</span></span>

<span data-ttu-id="736b8-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="736b8-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="736b8-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="736b8-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="736b8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="736b8-118">Remarks</span></span>

<span data-ttu-id="736b8-119">L’état des applications en cours d’exécution sur l’ordinateur virtuel est reflété dans la valeur de la propriété **OperationalStatus** \[ 1 \] de la classe [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="736b8-119">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span>

<span data-ttu-id="736b8-120">Pour utiliser cet élément de programmation, les composants d’intégration Windows 8 doivent être installés sur l’ordinateur virtuel dans lequel l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="736b8-120">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="736b8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="736b8-121">Requirements</span></span>



| <span data-ttu-id="736b8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="736b8-122">Requirement</span></span> | <span data-ttu-id="736b8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="736b8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="736b8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="736b8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="736b8-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="736b8-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="736b8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="736b8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="736b8-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="736b8-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="736b8-128">Version</span><span class="sxs-lookup"><span data-stu-id="736b8-128">Version</span></span><br/>                  | <span data-ttu-id="736b8-129">Composants d’intégration pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="736b8-129">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="736b8-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="736b8-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="736b8-131"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="736b8-131"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="736b8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="736b8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="736b8-133">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="736b8-133">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




