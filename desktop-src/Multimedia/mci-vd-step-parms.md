---
title: Structure MCI_VD_STEP_PARMS (Mciapi. h)
description: La structure des étapes de l’étape MCI MCI \_ \_ contient des \_ informations pour la \_ commande d’étape MCI pour les appareils videodisc.
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- Structure de MCI_VD_STEP_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508598"
---
# <a name="mci_vd_step_parms-structure"></a><span data-ttu-id="86819-104">La \_ \_ structure des étapes \_ de MCI VD</span><span class="sxs-lookup"><span data-stu-id="86819-104">MCI\_VD\_STEP\_PARMS structure</span></span>

<span data-ttu-id="86819-105">La structure des étapes de l' **\_ \_ étape \_ MCI MCI** contient des informations pour la commande d' [**\_ étape MCI**](mci-step.md) pour les appareils videodisc.</span><span class="sxs-lookup"><span data-stu-id="86819-105">The **MCI\_VD\_STEP\_PARMS** structure contains information for the [**MCI\_STEP**](mci-step.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="86819-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86819-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="86819-107">Membres</span><span class="sxs-lookup"><span data-stu-id="86819-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="86819-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="86819-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="86819-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="86819-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="86819-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="86819-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="86819-111">Nombre de frames à exécuter à l’étape.</span><span class="sxs-lookup"><span data-stu-id="86819-111">Number of frames to step.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86819-112">Notes</span><span class="sxs-lookup"><span data-stu-id="86819-112">Remarks</span></span>

<span data-ttu-id="86819-113">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="86819-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="86819-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86819-114">Requirements</span></span>



| <span data-ttu-id="86819-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86819-115">Requirement</span></span> | <span data-ttu-id="86819-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="86819-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="86819-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86819-117">Minimum supported client</span></span><br/> | <span data-ttu-id="86819-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86819-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="86819-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86819-119">Minimum supported server</span></span><br/> | <span data-ttu-id="86819-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86819-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="86819-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="86819-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="86819-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="86819-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86819-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86819-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86819-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="86819-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="86819-125">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="86819-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="86819-126">**\_étape MCI**</span><span class="sxs-lookup"><span data-stu-id="86819-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="86819-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86819-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

