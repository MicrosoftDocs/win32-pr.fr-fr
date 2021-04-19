---
description: La liste suivante décrit les constantes de stratégie de déchargement.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Constantes de stratégie de déchargement (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531941"
---
# <a name="discharge-policy-constants"></a><span data-ttu-id="1470c-103">Constantes de stratégie de déchargement</span><span class="sxs-lookup"><span data-stu-id="1470c-103">Discharge Policy Constants</span></span>

<span data-ttu-id="1470c-104">La liste suivante décrit les constantes de stratégie de déchargement.</span><span class="sxs-lookup"><span data-stu-id="1470c-104">The following list describes the discharge policy constants.</span></span>



| <span data-ttu-id="1470c-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="1470c-105">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="1470c-106">Description</span><span class="sxs-lookup"><span data-stu-id="1470c-106">Description</span></span>                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <span data-ttu-id="1470c-107">En <dt>**charge \_ STRATÉGIE \_ critique**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1470c-107"><dt>**DISCHARGE\_POLICY\_CRITICAL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="1470c-108">Lequel des paramètres de stratégie de déchargement de la batterie (structures de [**\_ \_ niveau d’alimentation du système**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) est utilisé lorsque la batterie se décharge au-dessous du seuil critique.</span><span class="sxs-lookup"><span data-stu-id="1470c-108">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the critical threshold.</span></span><br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <span data-ttu-id="1470c-109">En <dt>**charge \_ STRATÉGIE \_ faible**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1470c-109"><dt>**DISCHARGE\_POLICY\_LOW**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="1470c-110">Lequel des paramètres de stratégie de déchargement de la batterie (structures de [**\_ \_ niveau d’alimentation du système**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) est utilisé lorsque la batterie est déchargée au-dessous du seuil inférieur.</span><span class="sxs-lookup"><span data-stu-id="1470c-110">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the low threshold.</span></span><br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <span data-ttu-id="1470c-111"><dt>**Nombre \_ \_Stratégies de rejet**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1470c-111"><dt>**NUM\_DISCHARGE\_POLICIES**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="1470c-112">Nombre de paramètres de [**stratégie de \_ \_**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) déchargement de batterie spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1470c-112">Number of battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) specified.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="1470c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1470c-113">Requirements</span></span>



| <span data-ttu-id="1470c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1470c-114">Requirement</span></span> | <span data-ttu-id="1470c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1470c-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1470c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1470c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1470c-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1470c-117">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1470c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1470c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1470c-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1470c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1470c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1470c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1470c-121"><dt>Winnt. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1470c-121"><dt>WinNT.h (include Windows.h)</dt></span></span> </dl> |



 

 




