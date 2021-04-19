---
title: Classe Win32_WinSAT
description: Définit des informations d’évaluation récapitulatives pour l’évaluation formelle la plus récente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Classe Win32_WinSAT WinSAT
- Win32_WinSAT classe WinSAT, décrite
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511601"
---
# <a name="win32_winsat-class"></a><span data-ttu-id="84def-105">\_Classe Win32 WinSAT</span><span class="sxs-lookup"><span data-stu-id="84def-105">Win32\_WinSAT class</span></span>

<span data-ttu-id="84def-106">\[**Win32 \_ WinSAT** peut être modifié ou non disponible pour les mises en production après Windows 8.1.\]</span><span class="sxs-lookup"><span data-stu-id="84def-106">\[**Win32\_WinSAT** may be altered or unavailable for releases after Windows 8.1.\]</span></span>

<span data-ttu-id="84def-107">Définit des informations d’évaluation récapitulatives pour l’évaluation formelle la plus récente.</span><span class="sxs-lookup"><span data-stu-id="84def-107">Defines summary assessment information for the most recent formal assessment.</span></span>

<span data-ttu-id="84def-108">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="84def-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84def-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84def-109">Syntax</span></span>

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a><span data-ttu-id="84def-110">Membres</span><span class="sxs-lookup"><span data-stu-id="84def-110">Members</span></span>

<span data-ttu-id="84def-111">La classe **Win32 \_ WinSAT** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="84def-111">The **Win32\_WinSAT** class has these types of members:</span></span>

-   [<span data-ttu-id="84def-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84def-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84def-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="84def-113">Properties</span></span>

<span data-ttu-id="84def-114">La classe **Win32 \_ WinSAT** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="84def-114">The **Win32\_WinSAT** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84def-115">**CPUScore**</span><span class="sxs-lookup"><span data-stu-id="84def-115">**CPUScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84def-116">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="84def-116">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="84def-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84def-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84def-118">Un score pour les processeurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="84def-118">A score for the processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="84def-119">**D3DScore**</span><span class="sxs-lookup"><span data-stu-id="84def-119">**D3DScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84def-120">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="84def-120">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="84def-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84def-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84def-122">Après Windows 8.1, WinSAT n’évalue plus les fonctionnalités graphiques à trois dimensions (jeux) de l’ordinateur et la capacité du pilote Graphics à afficher des objets et à exécuter des nuanceurs à l’aide de cette évaluation.</span><span class="sxs-lookup"><span data-stu-id="84def-122">After Windows 8.1, WinSAT no longer assess the three-dimensional graphics (gaming) capabilities of the computer and the graphics driver's ability to render objects and execute shaders using this assessment.</span></span> <span data-ttu-id="84def-123">Pour la compatibilité, les valeurs Sentinel des rapports WinSAT pour les métriques et les scores, toutefois, ne sont pas calculées en temps réel.</span><span class="sxs-lookup"><span data-stu-id="84def-123">For compatibility, WinSAT report sentinel values for the metrics and scores, however these are not calculated in real time.</span></span>

</dd> <dt>

<span data-ttu-id="84def-124">**DiskScore**</span><span class="sxs-lookup"><span data-stu-id="84def-124">**DiskScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84def-125">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="84def-125">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="84def-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84def-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84def-127">Un score pour le débit de lecture séquentielle sur le disque dur principal sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="84def-127">A score for the sequential read throughput on the primary hard disk on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="84def-128">**GraphicsScore**</span><span class="sxs-lookup"><span data-stu-id="84def-128">**GraphicsScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84def-129">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="84def-129">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="84def-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84def-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84def-131">Score pour les capacités graphiques de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="84def-131">A score for the graphics capabilities of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="84def-132">**MemoryScore**</span><span class="sxs-lookup"><span data-stu-id="84def-132">**MemoryScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84def-133">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="84def-133">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="84def-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84def-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84def-135">Un score pour le débit et la capacité de la mémoire de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="84def-135">A score for the memory throughput and capacity of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="84def-136">**TimeTaken**</span><span class="sxs-lookup"><span data-stu-id="84def-136">**TimeTaken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84def-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="84def-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84def-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84def-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84def-139">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="84def-139">Qualifiers: **key**</span></span>
</dt> </dl>

<span data-ttu-id="84def-140">Cette propriété doit être définie sur « MostRecentAssessment » dans la clause WHERE de votre requête WQL.</span><span class="sxs-lookup"><span data-stu-id="84def-140">This property must be set to "MostRecentAssessment" in the WHERE clause of your WQL query.</span></span>

</dd> <dt>

<span data-ttu-id="84def-141">**WinSATAssessmentState**</span><span class="sxs-lookup"><span data-stu-id="84def-141">**WinSATAssessmentState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84def-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84def-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84def-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84def-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84def-144">État de l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="84def-144">State of the assessment.</span></span> <span data-ttu-id="84def-145">Pour obtenir une description des valeurs possibles, consultez l’énumération de l' [**\_ \_ État d’évaluation WinSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .</span><span class="sxs-lookup"><span data-stu-id="84def-145">For a description of the possible values, see the [**WINSAT\_ASSESSMENT\_STATE**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="84def-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span><span class="sxs-lookup"><span data-stu-id="84def-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84def-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valide** (1)</span><span class="sxs-lookup"><span data-stu-id="84def-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valid** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84def-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span><span class="sxs-lookup"><span data-stu-id="84def-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84def-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span><span class="sxs-lookup"><span data-stu-id="84def-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84def-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="84def-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84def-151">**WinSPRLevel**</span><span class="sxs-lookup"><span data-stu-id="84def-151">**WinSPRLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84def-152">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="84def-152">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="84def-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="84def-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84def-154">Score de base pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="84def-154">Base score for the computer.</span></span> <span data-ttu-id="84def-155">Pour plus d’informations sur la valeur du score, consultez la propriété [**IProvideWinSATResultsInfo :: SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .</span><span class="sxs-lookup"><span data-stu-id="84def-155">For details on the score value, see the [**IProvideWinSATResultsInfo::SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84def-156">Notes</span><span class="sxs-lookup"><span data-stu-id="84def-156">Remarks</span></span>

<span data-ttu-id="84def-157">Pour plus d’informations sur les scores des sous-composants, tels que **MemoryScore**, consultez la propriété [**IProvideWinSATAssessmentInfo :: score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .</span><span class="sxs-lookup"><span data-stu-id="84def-157">For information on the subcomponent scores, such as **MemoryScore**, see the [**IProvideWinSATAssessmentInfo::Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) property.</span></span>

## <a name="examples"></a><span data-ttu-id="84def-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="84def-158">Examples</span></span>

<span data-ttu-id="84def-159">Pour obtenir un exemple qui montre comment utiliser WMI pour récupérer des données de cette classe, consultez la méthode [**IProvideWinSATVisuals :: obtenir une \_ bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .</span><span class="sxs-lookup"><span data-stu-id="84def-159">For an example that shows how to use WMI to retrieve data from this class, see the [**IProvideWinSATVisuals::get\_Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="84def-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84def-160">Requirements</span></span>



| <span data-ttu-id="84def-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84def-161">Requirement</span></span> | <span data-ttu-id="84def-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="84def-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84def-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84def-163">Minimum supported client</span></span><br/> | <span data-ttu-id="84def-164">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84def-164">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="84def-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84def-165">Minimum supported server</span></span><br/> | <span data-ttu-id="84def-166">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="84def-166">None supported</span></span><br/>                                                                |
| <span data-ttu-id="84def-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="84def-167">Namespace</span></span><br/>                | <span data-ttu-id="84def-168">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="84def-168">Root\\CIMv2</span></span><br/>                                                                   |
| <span data-ttu-id="84def-169">MOF</span><span class="sxs-lookup"><span data-stu-id="84def-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84def-170"><dt>WinSAT. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84def-170"><dt>WinSAT.mof</dt></span></span> </dl>    |
| <span data-ttu-id="84def-171">DLL</span><span class="sxs-lookup"><span data-stu-id="84def-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84def-172"><dt>WinSATAPI.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84def-172"><dt>WinSATAPI.dll</dt></span></span> </dl> |



 

 





