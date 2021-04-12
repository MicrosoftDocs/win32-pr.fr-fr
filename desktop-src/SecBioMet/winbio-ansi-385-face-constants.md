---
title: Constantes WINBIO_ANSI_385_FACE ( \_ types WINBIO. h)
description: Spécifiez les types d’images de face frontale pour la reconnaissance faciale.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6bc6ba28de799795a049dde3ab98ebdb4c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105412"
---
# <a name="winbio_ansi_385_face-constants"></a><span data-ttu-id="31b88-103">\_ \_ Constantes de visage WINBIO ANSI 385 \_</span><span class="sxs-lookup"><span data-stu-id="31b88-103">WINBIO\_ANSI\_385\_FACE Constants</span></span>

<span data-ttu-id="31b88-104">Les constantes suivantes sont des valeurs de **\_ sous- \_ type biométriques WINBIO** qui peuvent être utilisées pour spécifier les deux types d’images de face frontale, comme défini par ANSI INCITS 385-2004 : « format de reconnaissance faciale pour l’échange de données » : résolution complète et résolution faible.</span><span class="sxs-lookup"><span data-stu-id="31b88-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the two types of frontal face images as defined by ANSI INCITS 385-2004: "Face Recognition Format for Data Interchange": full resolution and low resolution.</span></span> <span data-ttu-id="31b88-105">Dans la pratique, l’infrastructure biométrique utilise uniquement des images de résolution complète pour la reconnaissance faciale.</span><span class="sxs-lookup"><span data-stu-id="31b88-105">In practice, the biometric framework will use only full resolution images for facial recognition.</span></span>



| <span data-ttu-id="31b88-106">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="31b88-106">Constant/value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="31b88-107">Description</span><span class="sxs-lookup"><span data-stu-id="31b88-107">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <span data-ttu-id="31b88-108"><dt>**WINBIO \_ \_Type de \_ visage ANSI 385 \_ \_ inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31b88-108"><dt>**WINBIO\_ANSI\_385\_FACE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="31b88-109">Le type d’image de visage frontal est inconnu.</span><span class="sxs-lookup"><span data-stu-id="31b88-109">The frontal face image type is unknown.</span></span><br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <span data-ttu-id="31b88-110"><dt>**WINBIO \_ ANSI \_ 385 \_ face \_ frontale \_ Full**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="31b88-110"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_FULL**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="31b88-111">Le type d’image de visage frontal est à résolution complète.</span><span class="sxs-lookup"><span data-stu-id="31b88-111">The frontal face image type is full resolution.</span></span><br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <span data-ttu-id="31b88-112"><dt>**WINBIO \_ ANSI \_ 385 \_ face \_ frontale \_**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="31b88-112"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_TOKEN**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="31b88-113">Le type d’image de visage frontal est de faible résolution.</span><span class="sxs-lookup"><span data-stu-id="31b88-113">The frontal face image type is low resolution.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="31b88-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31b88-114">Requirements</span></span>



| <span data-ttu-id="31b88-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31b88-115">Requirement</span></span> | <span data-ttu-id="31b88-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="31b88-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31b88-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31b88-117">Minimum supported client</span></span><br/> | <span data-ttu-id="31b88-118">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31b88-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="31b88-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31b88-119">Minimum supported server</span></span><br/> | <span data-ttu-id="31b88-120">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31b88-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="31b88-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="31b88-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b88-122"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31b88-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





