---
title: Constantes WINBIO_BIOMETRIC_SENSOR_SUBTYPE ( \_ types WINBIO. h)
description: Spécifiez un masque de réutiliser pour les fonctionnalités de capteur intégrées.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384379"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a><span data-ttu-id="5ebcb-103">\_ \_ Constantes de sous-type de capteur BIOmétrique WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="5ebcb-103">WINBIO\_BIOMETRIC\_SENSOR\_SUBTYPE Constants</span></span>

<span data-ttu-id="5ebcb-104">Les constantes suivantes peuvent être utilisées comme masque de masque pour le paramètre *Capabilities* de la structure de [**\_ \_ schéma d’unité WINBIO**](winbio-unit-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="5ebcb-104">The following constants can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="5ebcb-105">Ils font référence aux fonctionnalités de capteur intégrées.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-105">These refer to the onboard sensor capabilities.</span></span>



| <span data-ttu-id="5ebcb-106">Constante</span><span class="sxs-lookup"><span data-stu-id="5ebcb-106">Constant</span></span>                                                                                                                                                                                                            | <span data-ttu-id="5ebcb-107">Description</span><span class="sxs-lookup"><span data-stu-id="5ebcb-107">Description</span></span>                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <span data-ttu-id="5ebcb-108"><dt>**\_sous-type de capteur WINBIO \_ \_ inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebcb-108"><dt>**WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN**</dt></span></span> </dl>     | <span data-ttu-id="5ebcb-109">Les sous-types de capteur ne sont pas connus.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-109">The sensor sub types is not known.</span></span><br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <span data-ttu-id="5ebcb-110"><dt>**\_balayage de \_ sous-type de capteur WINBIO FP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebcb-110"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE**</dt></span></span> </dl> | <span data-ttu-id="5ebcb-111">Le capteur prend en charge les balayages par empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-111">The sensor supports fingerprint swipes.</span></span><br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <span data-ttu-id="5ebcb-112"><dt>**WINBIO \_ de \_ sous-type de capteur FP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ebcb-112"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH**</dt></span></span> </dl> | <span data-ttu-id="5ebcb-113">Le capteur prend en charge les touches Finger.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-113">The sensor supports finger touches.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="5ebcb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ebcb-114">Requirements</span></span>



| <span data-ttu-id="5ebcb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ebcb-115">Requirement</span></span> | <span data-ttu-id="5ebcb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ebcb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebcb-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ebcb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebcb-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ebcb-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="5ebcb-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ebcb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebcb-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ebcb-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ebcb-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ebcb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ebcb-122"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ebcb-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ebcb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ebcb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebcb-124">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="5ebcb-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="5ebcb-125">**\_schéma d’unité WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="5ebcb-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





