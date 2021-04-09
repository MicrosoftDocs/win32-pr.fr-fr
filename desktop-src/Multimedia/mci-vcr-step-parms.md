---
title: Structure de MCI_VCR_STEP_PARMS (VCR. h)
description: La structure de l' \_ \_ étape de magnétoscope MCI contient des \_ paramètres pour la \_ commande d’étape MCI pour les enregistreurs vidéo-cassettes.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- Structure de MCI_VCR_STEP_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032471"
---
# <a name="mci_vcr_step_parms-structure"></a><span data-ttu-id="c0cf4-104">\_Étape de \_ \_ gestion des magnétoscopes MCI</span><span class="sxs-lookup"><span data-stu-id="c0cf4-104">MCI\_VCR\_STEP\_PARMS structure</span></span>

<span data-ttu-id="c0cf4-105">La structure de l' **\_ étape de magnétoscope \_ \_ MCI** contient des paramètres pour la commande d' [**\_ étape MCI**](mci-step.md) pour les enregistreurs vidéo-cassettes.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-105">The **MCI\_VCR\_STEP\_PARMS** structure contains parameters for the [**MCI\_STEP**](mci-step.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0cf4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0cf4-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="c0cf4-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c0cf4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0cf4-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c0cf4-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c0cf4-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c0cf4-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="c0cf4-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="c0cf4-111">Nombre de frames à sauter (longueur d’une seule étape) à mesure que la commande d' [**\_ étape MCI**](mci-step.md) progresse vers l’avant ou vers l’arrière dans le contenu.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-111">Number of frames to jump (the length of a single step) as the [**MCI\_STEP**](mci-step.md) command steps forward or backward through the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0cf4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c0cf4-112">Remarks</span></span>

<span data-ttu-id="c0cf4-113">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="c0cf4-113">When assigning data to the members in this structure, set the corresponding flags in the *fdwCommand* parameter of [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0cf4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0cf4-114">Requirements</span></span>



| <span data-ttu-id="c0cf4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0cf4-115">Requirement</span></span> | <span data-ttu-id="c0cf4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0cf4-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c0cf4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0cf4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c0cf4-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0cf4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c0cf4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0cf4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c0cf4-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0cf4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c0cf4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0cf4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0cf4-122"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0cf4-122"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0cf4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0cf4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0cf4-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c0cf4-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c0cf4-125">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="c0cf4-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c0cf4-126">**\_étape MCI**</span><span class="sxs-lookup"><span data-stu-id="c0cf4-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="c0cf4-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0cf4-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

