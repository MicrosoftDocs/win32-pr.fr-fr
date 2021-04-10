---
title: Constantes WINBIO_PRESENCE_CHANGE ( \_ types WINBIO. h)
description: Décrit les types de modifications qui peuvent se produire lorsque le Windows Biometric Framework surveille la présence de personnes.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032460"
---
# <a name="winbio_presence_change-constants"></a><span data-ttu-id="756fe-103">\_Constantes de modification de présence WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="756fe-103">WINBIO\_PRESENCE\_CHANGE Constants</span></span>

<span data-ttu-id="756fe-104">Décrit les types de modifications qui peuvent se produire lorsque le Windows Biometric Framework surveille la présence de personnes.</span><span class="sxs-lookup"><span data-stu-id="756fe-104">Describes the types of changes that can occur when the Windows Biometric Framework monitors the presence of individuals.</span></span>



| <span data-ttu-id="756fe-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="756fe-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="756fe-106">Description</span><span class="sxs-lookup"><span data-stu-id="756fe-106">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <span data-ttu-id="756fe-107"><dt>**WINBIO \_ TYPE de modification de présence \_ \_ \_ inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="756fe-107"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="756fe-108">Le type d’événement est inconnu.</span><span class="sxs-lookup"><span data-stu-id="756fe-108">The type of event is unknown.</span></span> <span data-ttu-id="756fe-109">Cette valeur est utilisée pour la structure non initialisée.</span><span class="sxs-lookup"><span data-stu-id="756fe-109">This value is used for the uninitialized structure.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <span data-ttu-id="756fe-110"><dt>**WINBIO \_ TYPE de modification de présence \_ \_ \_ mettre à jour \_ tous les**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="756fe-110"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UPDATE\_ALL**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="756fe-111">Fournit des informations sur toutes les faces actuelles dans le cadre de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="756fe-111">Provides information about all of the faces current in the camera frame.</span></span><br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <span data-ttu-id="756fe-112"><dt>**WINBIO \_ \_Type de \_ modification \_ de présence**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="756fe-112"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_ARRIVE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="756fe-113">Une nouvelle face est entrée dans le cadre de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="756fe-113">A new face entered the camera frame.</span></span><br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <span data-ttu-id="756fe-114"><dt>**WINBIO \_ \_Reconnaissance du \_ type \_ de modification de présence**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="756fe-114"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_RECOGNIZE**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="756fe-115">Un visage a été mis en correspondance avec un utilisateur inscrit.</span><span class="sxs-lookup"><span data-stu-id="756fe-115">A face was matched to an enrolled user.</span></span><br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <span data-ttu-id="756fe-116"><dt>**WINBIO \_ TYPE de modification de présence- \_ \_ \_ DEPART**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="756fe-116"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_DEPART**</dt> <dt>4</dt></span></span> </dl>              | <span data-ttu-id="756fe-117">Un visage précédemment détecté est sorti du cadre de l’appareil photo pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="756fe-117">A previously detected face has been out of the camera frame for a period of time.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <span data-ttu-id="756fe-118"><dt>**WINBIO \_ TYPE de modification de présence- \_ \_ \_ piste**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="756fe-118"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_TRACK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="756fe-119">Fournit des informations de mise à jour sur le cadre englobant et rejettent les valeurs de détails pour un sous-ensemble des visages qui se trouvent actuellement dans le cadre de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="756fe-119">Provides updates information about the bounding box and reject detail values for a subset of the faces that are currently in the camera frame.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="756fe-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="756fe-120">Requirements</span></span>



| <span data-ttu-id="756fe-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="756fe-121">Requirement</span></span> | <span data-ttu-id="756fe-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="756fe-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756fe-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="756fe-123">Minimum supported client</span></span><br/> | <span data-ttu-id="756fe-124">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="756fe-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="756fe-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="756fe-125">Minimum supported server</span></span><br/> | <span data-ttu-id="756fe-126">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="756fe-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="756fe-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="756fe-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="756fe-128"><dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt></span><span class="sxs-lookup"><span data-stu-id="756fe-128"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





