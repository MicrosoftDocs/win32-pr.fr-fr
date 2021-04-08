---
title: Constantes WINBIO_ENG_CAP ( \_ types WINBIO. h)
description: Spécifiez des fonctionnalités de moteur génériques.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d69db9f0e15ca0d50aa5ca134fdc74904dec85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743676"
---
# <a name="winbio_eng_cap-constants"></a><span data-ttu-id="5241f-103">\_ \_ Constantes WINBIO ENG</span><span class="sxs-lookup"><span data-stu-id="5241f-103">WINBIO\_ENG\_CAP Constants</span></span>

<span data-ttu-id="5241f-104">Les constantes suivantes sont des valeurs de **\_ fonctionnalités WINBIO** qui peuvent être utilisées pour spécifier des fonctionnalités génériques du composant moteur qui est connecté à une unité biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="5241f-104">The following constants are **WINBIO\_CAPABILITIES** values that can be used to specify generic capabilities of the engine component that is connected to a specific biometric unit.</span></span> <span data-ttu-id="5241f-105">Vous spécifiez ces fonctionnalités dans le membre **GenericEngineCapabilities** de la structure [**WINBIO \_ Extended \_ Engine \_ info**](winbio-extended-engine-info.md) .</span><span class="sxs-lookup"><span data-stu-id="5241f-105">You specify these capabilities in **GenericEngineCapabilities** member of the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure.</span></span>



| <span data-ttu-id="5241f-106">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="5241f-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="5241f-107">Description</span><span class="sxs-lookup"><span data-stu-id="5241f-107">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <span data-ttu-id="5241f-108"><dt>**WINBIO \_ \_ \_ \_ Amélioration itérative du eng-Cap**</dt> - <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5241f-108"><dt>**WINBIO\_ENG\_CAP\_ITERATIVE\_IMPROVEMENT**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="5241f-109">Le composant de moteur biométrique peut effectuer une amélioration itérative.</span><span class="sxs-lookup"><span data-stu-id="5241f-109">The biometric engine component can perform iterative improvement.</span></span><br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <span data-ttu-id="5241f-110"><dt>**WINBIO \_ \_Détection d' \_ usurpation \_ d’adresse eng Cap**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5241f-110"><dt>**WINBIO\_ENG\_CAP\_SPOOF\_DETECTION**</dt> <dt>0x00000002</dt></span></span> </dl>                   | <span data-ttu-id="5241f-111">Le composant de moteur biométrique peut effectuer une détection d’usurpation d’identité.</span><span class="sxs-lookup"><span data-stu-id="5241f-111">The biometric engine component can perform spoof detection.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="5241f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5241f-112">Requirements</span></span>



| <span data-ttu-id="5241f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5241f-113">Requirement</span></span> | <span data-ttu-id="5241f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5241f-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5241f-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5241f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5241f-116">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5241f-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="5241f-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5241f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5241f-118">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5241f-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5241f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="5241f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5241f-120"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5241f-120"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





