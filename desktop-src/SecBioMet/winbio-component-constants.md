---
title: Constantes WINBIO_COMPONENT ( \_ types WINBIO. h)
description: Spécifiez le type d’adaptateur utilisé.
ms.assetid: f920788b-2175-4c01-81b5-e7b49111a7ac
topic_type:
- apiref
api_name:
- WINBIO_COMPONENT_SENSOR
- WINBIO_COMPONENT_ENGINE
- WINBIO_COMPONENT_STORAGE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07afe4fac08632133d4fa755717d83475b78c675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384247"
---
# <a name="winbio_component-constants"></a><span data-ttu-id="b64c9-103">\_Constantes de composant WINBIO</span><span class="sxs-lookup"><span data-stu-id="b64c9-103">WINBIO\_COMPONENT Constants</span></span>

<span data-ttu-id="b64c9-104">Les constantes suivantes peuvent être utilisées lors de l’appel de [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit) ou [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged) pour spécifier le type d’adaptateur utilisé.</span><span class="sxs-lookup"><span data-stu-id="b64c9-104">The following constants can be used when calling [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit) or [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged) to specify the type of adapter being used.</span></span>



| <span data-ttu-id="b64c9-105">Constante</span><span class="sxs-lookup"><span data-stu-id="b64c9-105">Constant</span></span>                                                                                                                                                                                        | <span data-ttu-id="b64c9-106">Description</span><span class="sxs-lookup"><span data-stu-id="b64c9-106">Description</span></span>                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="WINBIO_COMPONENT_SENSOR"></span><span id="winbio_component_sensor"></span><dl> <span data-ttu-id="b64c9-107"><dt>**\_capteur de composant WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b64c9-107"><dt>**WINBIO\_COMPONENT\_SENSOR**</dt></span></span> </dl>    | <span data-ttu-id="b64c9-108">Spécifie un adaptateur de capteur.</span><span class="sxs-lookup"><span data-stu-id="b64c9-108">Specifies a sensor adapter.</span></span><br/>  |
| <span id="WINBIO_COMPONENT_ENGINE"></span><span id="winbio_component_engine"></span><dl> <span data-ttu-id="b64c9-109"><dt>**\_moteur de composant WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b64c9-109"><dt>**WINBIO\_COMPONENT\_ENGINE**</dt></span></span> </dl>    | <span data-ttu-id="b64c9-110">Spécifie un adaptateur de moteur.</span><span class="sxs-lookup"><span data-stu-id="b64c9-110">Specifies an engine adapter.</span></span><br/> |
| <span id="WINBIO_COMPONENT_STORAGE"></span><span id="winbio_component_storage"></span><dl> <span data-ttu-id="b64c9-111"><dt>**\_stockage du composant WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b64c9-111"><dt>**WINBIO\_COMPONENT\_STORAGE**</dt></span></span> </dl> | <span data-ttu-id="b64c9-112">Spécifie un adaptateur de stockage.</span><span class="sxs-lookup"><span data-stu-id="b64c9-112">Specifies a storage adapter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b64c9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b64c9-113">Requirements</span></span>



| <span data-ttu-id="b64c9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b64c9-114">Requirement</span></span> | <span data-ttu-id="b64c9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b64c9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b64c9-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b64c9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b64c9-117">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b64c9-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="b64c9-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b64c9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b64c9-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b64c9-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b64c9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b64c9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b64c9-121"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b64c9-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b64c9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b64c9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64c9-123">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="b64c9-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





