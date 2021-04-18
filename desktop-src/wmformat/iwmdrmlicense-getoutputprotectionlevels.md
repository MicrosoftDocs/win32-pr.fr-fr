---
title: Méthode IWMDRMLicense GetOutputProtectionLevels
description: La méthode GetOutputProtectionLevels récupère des informations sur tous les niveaux de protection de sortie (OPLs) affectés à la licence.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Méthode GetOutputProtectionLevels format Windows Media
- Méthode GetOutputProtectionLevels format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetOutputProtectionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106512479"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a><span data-ttu-id="be500-106">IWMDRMLicense :: GetOutputProtectionLevels, méthode</span><span class="sxs-lookup"><span data-stu-id="be500-106">IWMDRMLicense::GetOutputProtectionLevels method</span></span>

<span data-ttu-id="be500-107">La méthode **GetOutputProtectionLevels** récupère des informations sur tous les niveaux de protection de sortie (OPLs) affectés à la licence.</span><span class="sxs-lookup"><span data-stu-id="be500-107">The **GetOutputProtectionLevels** method retrieves information about all output protection levels (OPLs) assigned to the license.</span></span>

## <a name="syntax"></a><span data-ttu-id="be500-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be500-108">Syntax</span></span>


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a><span data-ttu-id="be500-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be500-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be500-110">*pOPLs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="be500-110">*pOPLs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be500-111">Pointeur vers une structure de [**\_ niveaux de \_ protection \_ de sortie WMDRM**](wmdrm-output-protection-levels.md) qui reçoit les informations OPL.</span><span class="sxs-lookup"><span data-stu-id="be500-111">Pointer to a [**WMDRM\_OUTPUT\_PROTECTION\_LEVELS**](wmdrm-output-protection-levels.md) structure that receives the OPL information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be500-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be500-112">Return value</span></span>

<span data-ttu-id="be500-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="be500-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="be500-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="be500-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="be500-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="be500-115">Return code</span></span>                                                                          | <span data-ttu-id="be500-116">Description</span><span class="sxs-lookup"><span data-stu-id="be500-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="be500-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be500-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="be500-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="be500-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="be500-119">Notes</span><span class="sxs-lookup"><span data-stu-id="be500-119">Remarks</span></span>

<span data-ttu-id="be500-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="be500-120">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="be500-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be500-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be500-122">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="be500-122">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





