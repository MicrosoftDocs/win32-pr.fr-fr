---
description: Autorise la spécification de la collecte des métriques dans le temps à démarrer et à spécifier l’intervalle d’échantillonnage préféré pour la collecte de données périodique.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Méthode ControlSampleTimes de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527506"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a><span data-ttu-id="5ed23-103">Méthode ControlSampleTimes de la \_ classe CIM MetricService</span><span class="sxs-lookup"><span data-stu-id="5ed23-103">ControlSampleTimes method of the CIM\_MetricService class</span></span>

<span data-ttu-id="5ed23-104">Autorise la spécification de la collecte des métriques dans le temps à démarrer et à spécifier l’intervalle d’échantillonnage préféré pour la collecte de données périodique.</span><span class="sxs-lookup"><span data-stu-id="5ed23-104">Allows specification of the point in time metric gathering is to be started and to specify the preferred sample interval time for periodic data gathering.</span></span>

<span data-ttu-id="5ed23-105">Chaque fois que l’échantillonnage pour des métriques supplémentaires est démarré, les paramètres spécifiés par cette méthode peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="5ed23-105">Whenever sampling for additional metrics is started, the settings specified by this method may be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed23-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ed23-106">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="5ed23-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ed23-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed23-108">*StartSampleTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ed23-108">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed23-109">Point dans le temps pendant lequel l’échantillonnage des mesures doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="5ed23-109">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="5ed23-110">La valeur 99990101000000.000000 + 000 indique que l’échantillonnage doit commencer à la prochaine synchronisation à l’heure complète.</span><span class="sxs-lookup"><span data-stu-id="5ed23-110">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="5ed23-111">L’échantillonnage est synchronisé à l’heure complète si les secondes depuis l’intervalle d’échantillonnage du modulo minuit en secondes sont égales à 0.</span><span class="sxs-lookup"><span data-stu-id="5ed23-111">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="5ed23-112">*PreferredSampleInterval* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ed23-112">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed23-113">Intervalle d’échantillonnage préféré.</span><span class="sxs-lookup"><span data-stu-id="5ed23-113">Preferred sample interval time.</span></span> <span data-ttu-id="5ed23-114">Pour obtenir des métriques corrélées, il est recommandé de choisir l’intervalle d’échantillonnage de manière à ce que l’intervalle d’échantillonnage 3600 modulo en secondes soit égal à 0.</span><span class="sxs-lookup"><span data-stu-id="5ed23-114">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="5ed23-115">Il incombe à l’implémentation du service métrique CIM de déterminer si l’intervalle d’échantillonnage demandé est respecté.</span><span class="sxs-lookup"><span data-stu-id="5ed23-115">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="5ed23-116">Le client CIM peut vérifier si les fournisseurs de mesures respectent l’intervalle d’échantillonnage demandé en extrayant les instances BaseMetricDefinition associées et en vérifiant le contenu du [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).**Propriété SampleInterval** .</span><span class="sxs-lookup"><span data-stu-id="5ed23-116">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**SampleInterval** property.</span></span>

</dd> <dt>

<span data-ttu-id="5ed23-117">*RestartGathering* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ed23-117">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed23-118">**True** pour demander que la collecte de toutes les métriques associées au service de métrique soit redémarrée avec cet appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="5ed23-118">**TRUE** to request that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed23-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ed23-119">Return value</span></span>

<span data-ttu-id="5ed23-120">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="5ed23-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5ed23-121">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="5ed23-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5ed23-122">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="5ed23-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5ed23-123">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="5ed23-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5ed23-124">**Méthode réservée** (..)</span><span class="sxs-lookup"><span data-stu-id="5ed23-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5ed23-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5ed23-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5ed23-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ed23-126">Requirements</span></span>



| <span data-ttu-id="5ed23-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ed23-127">Requirement</span></span> | <span data-ttu-id="5ed23-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ed23-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed23-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ed23-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed23-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5ed23-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5ed23-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ed23-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed23-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5ed23-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5ed23-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5ed23-133">Namespace</span></span><br/>                | <span data-ttu-id="5ed23-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5ed23-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5ed23-135">MOF</span><span class="sxs-lookup"><span data-stu-id="5ed23-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ed23-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ed23-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ed23-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5ed23-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ed23-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ed23-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5ed23-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ed23-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed23-140">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="5ed23-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




