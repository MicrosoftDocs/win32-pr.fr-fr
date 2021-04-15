---
title: Constantes WINBIO_IRIS ( \_ types WINBIO. h)
description: Spécifiez les types de reconnaissance d’IRIS.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465823"
---
# <a name="winbio_iris-constants"></a><span data-ttu-id="247be-103">\_Constantes Iris WINBIO</span><span class="sxs-lookup"><span data-stu-id="247be-103">WINBIO\_IRIS Constants</span></span>

<span data-ttu-id="247be-104">Les constantes suivantes sont des valeurs de **\_ sous- \_ type biométriques WINBIO** qui peuvent être utilisées pour spécifier les types de reconnaissance d’IRIS au-delà de l’INCITS ANSI 379-2004 : « Iris image Interchange Format », qui ne définit aucune valeur d’œil gauche/droite :</span><span class="sxs-lookup"><span data-stu-id="247be-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the types for iris recognition beyond ANSI INCITS 379-2004: "Iris Image Interchange Format", which does not define any left/right eye values:</span></span>



| <span data-ttu-id="247be-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="247be-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="247be-106">Description</span><span class="sxs-lookup"><span data-stu-id="247be-106">Description</span></span>                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <span data-ttu-id="247be-107"><dt> **\_ Type d’IRIS WINBIO \_ \_ inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="247be-107"><dt>**WINBIO\_IRIS\_TYPE\_UNKNOWN** </dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="247be-108">Le type d’iris est inconnu.</span><span class="sxs-lookup"><span data-stu-id="247be-108">The iris type is unknown.</span></span> <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <span data-ttu-id="247be-109"><dt> **WINBIO \_ Iris \_ gauche \_**</dt> <dt>0xF5</dt></span><span class="sxs-lookup"><span data-stu-id="247be-109"><dt>**WINBIO\_IRIS\_LEFT\_EYE** </dt> <dt>0xF5 </dt></span></span> </dl>                               | <span data-ttu-id="247be-110">Le type d’iris est l’œil gauche.</span><span class="sxs-lookup"><span data-stu-id="247be-110">The iris type is the left eye.</span></span> <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <span data-ttu-id="247be-111"><dt> **WINBIO \_ Iris \_ droit \_**</dt> <dt>0XF6</dt></span><span class="sxs-lookup"><span data-stu-id="247be-111"><dt>**WINBIO\_IRIS\_RIGHT\_EYE** </dt> <dt>0xF6 </dt></span></span> </dl>                            | <span data-ttu-id="247be-112">Le type d’iris est l’œil droit.</span><span class="sxs-lookup"><span data-stu-id="247be-112">The iris type is the right eye.</span></span> <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <span data-ttu-id="247be-113"><dt>**WINBIO \_ IRIS \_ non spécifié du \_ PDV \_ 01**</dt> <dt>0xF7</dt></span><span class="sxs-lookup"><span data-stu-id="247be-113"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_01**</dt> <dt>0xF7</dt></span></span> </dl>    | <span data-ttu-id="247be-114">Sous-type associé à un utilisateur s premier modèle lorsqu’un seul œil est le cadre de l’appareil photo et qu’il ne peut pas être déterminé s’il s’agit de l’utilisateur ou de l’œil droit.</span><span class="sxs-lookup"><span data-stu-id="247be-114">Subtype associated with a user s first template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <span data-ttu-id="247be-115"><dt> **WINBIO \_ Iris \_ non spécifié \_ pos \_**</dt> <dt>0xf8</dt></span><span class="sxs-lookup"><span data-stu-id="247be-115"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_02** </dt> <dt>0xF8</dt></span></span> </dl> | <span data-ttu-id="247be-116">Sous-type associé à un second modèle utilisateur lorsqu’un seul œil est le cadre de l’appareil photo et qu’il ne peut pas être déterminé s’il s’agit de l’utilisateur ou de l’œil droit.</span><span class="sxs-lookup"><span data-stu-id="247be-116">Subtype associated with a user s second template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <span data-ttu-id="247be-117"><dt> **WINBIO \_ Iris \_ des \_ yeux**</dt> <dt>0xf9</dt></span><span class="sxs-lookup"><span data-stu-id="247be-117"><dt>**WINBIO\_IRIS\_BOTH\_EYES** </dt> <dt>0xF9</dt></span></span> </dl>                             | <span data-ttu-id="247be-118">Le type d’iris est à la fois un œil.</span><span class="sxs-lookup"><span data-stu-id="247be-118">The iris type is both eyes.</span></span> <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <span data-ttu-id="247be-119"><dt> **WINBIO \_ Iris des \_ deux \_ yeux**</dt> <dt>0xFA</dt></span><span class="sxs-lookup"><span data-stu-id="247be-119"><dt>**WINBIO\_IRIS\_EITHER\_EYE** </dt> <dt>0xFA</dt></span></span> </dl>                          | <span data-ttu-id="247be-120">Le type d’iris est l’œil.</span><span class="sxs-lookup"><span data-stu-id="247be-120">The iris type is either eye.</span></span> <br/>                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="247be-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="247be-121">Requirements</span></span>



| <span data-ttu-id="247be-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="247be-122">Requirement</span></span> | <span data-ttu-id="247be-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="247be-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="247be-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="247be-124">Minimum supported client</span></span><br/> | <span data-ttu-id="247be-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="247be-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="247be-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="247be-126">Minimum supported server</span></span><br/> | <span data-ttu-id="247be-127">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="247be-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="247be-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="247be-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="247be-129"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="247be-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





