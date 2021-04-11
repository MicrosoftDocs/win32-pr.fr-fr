---
description: Définit les heures de l’exemple de contrôle.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Méthode ControlSampleTimes de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202764"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="f6a3b-103">Méthode ControlSampleTimes de la \_ classe MetricService MSVM</span><span class="sxs-lookup"><span data-stu-id="f6a3b-103">ControlSampleTimes method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="f6a3b-104">Définit les heures de l’exemple de contrôle.</span><span class="sxs-lookup"><span data-stu-id="f6a3b-104">Sets the control sample times.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6a3b-105">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="f6a3b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6a3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a3b-107">*StartSampleTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6a3b-107">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a3b-108">Point dans le temps pendant lequel l’échantillonnage des mesures doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="f6a3b-108">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="f6a3b-109">La valeur 99990101000000.000000 + 000 indique que l’échantillonnage doit commencer à la prochaine synchronisation à l’heure complète.</span><span class="sxs-lookup"><span data-stu-id="f6a3b-109">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="f6a3b-110">L’échantillonnage est synchronisé à l’heure complète si les secondes depuis l’intervalle d’échantillonnage du modulo minuit en secondes sont égales à 0.</span><span class="sxs-lookup"><span data-stu-id="f6a3b-110">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f6a3b-111">*PreferredSampleInterval* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6a3b-111">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a3b-112">Intervalle d’échantillonnage préféré.</span><span class="sxs-lookup"><span data-stu-id="f6a3b-112">Preferred sample interval time.</span></span> <span data-ttu-id="f6a3b-113">Pour obtenir des métriques corrélées, il est recommandé de choisir l’intervalle d’échantillonnage de manière à ce que l’intervalle d’échantillonnage 3600 modulo en secondes soit égal à 0.</span><span class="sxs-lookup"><span data-stu-id="f6a3b-113">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="f6a3b-114">Il incombe à l’implémentation du service métrique CIM de déterminer si l’intervalle d’échantillonnage demandé est respecté.</span><span class="sxs-lookup"><span data-stu-id="f6a3b-114">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="f6a3b-115">Le client CIM peut vérifier si les fournisseurs de mesures respectent l’intervalle d’échantillonnage demandé en extrayant les instances BaseMetricDefinition associées et en vérifiant le contenu de la propriété « CIM \_ BaseMetricDefinition. SampleInterval ».</span><span class="sxs-lookup"><span data-stu-id="f6a3b-115">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the "CIM\_BaseMetricDefinition.SampleInterval" property.</span></span>

</dd> <dt>

<span data-ttu-id="f6a3b-116">*RestartGathering* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6a3b-116">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a3b-117">Valeur booléenne qui, lorsqu’elle est définie sur TRUE, demande que la collecte de toutes les métriques associées au service de métrique soit redémarrée avec cet appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="f6a3b-117">Boolean that when set to TRUE requests that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a3b-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6a3b-118">Return value</span></span>

<span data-ttu-id="f6a3b-119">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f6a3b-119">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f6a3b-120">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="f6a3b-120">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6a3b-121">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="f6a3b-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f6a3b-122">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="f6a3b-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6a3b-123">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="f6a3b-123">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f6a3b-124">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f6a3b-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f6a3b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6a3b-125">Requirements</span></span>



| <span data-ttu-id="f6a3b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6a3b-126">Requirement</span></span> | <span data-ttu-id="f6a3b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6a3b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a3b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6a3b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f6a3b-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f6a3b-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f6a3b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6a3b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f6a3b-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f6a3b-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f6a3b-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f6a3b-132">Namespace</span></span><br/>                | <span data-ttu-id="f6a3b-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f6a3b-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f6a3b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f6a3b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6a3b-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6a3b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6a3b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f6a3b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6a3b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6a3b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6a3b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6a3b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6a3b-139">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="f6a3b-139">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




