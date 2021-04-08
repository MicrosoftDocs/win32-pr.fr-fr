---
title: Structure de MCI_VCR_CUE_PARMS (VCR. h)
description: La \_ structure de paramètres MCI VCR \_ CUE contient des \_ paramètres pour la \_ commande MCI CUE pour les enregistreurs vidéo-cassette.
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- Structure de MCI_VCR_CUE_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_CUE_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eeae20495281640718f95066476f0f3ac89dc6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844229"
---
# <a name="mci_vcr_cue_parms-structure"></a><span data-ttu-id="c6e9b-104">La \_ \_ structure des \_ PARMS du magnétoscope MCI</span><span class="sxs-lookup"><span data-stu-id="c6e9b-104">MCI\_VCR\_CUE\_PARMS structure</span></span>

<span data-ttu-id="c6e9b-105">La structure de paramètres **MCI \_ VCR \_ CUE \_** contient des paramètres pour la commande [**MCI \_ CUE**](mci-cue.md) pour les enregistreurs vidéo-cassette.</span><span class="sxs-lookup"><span data-stu-id="c6e9b-105">The **MCI\_VCR\_CUE\_PARMS** structure contains parameters for the [**MCI\_CUE**](mci-cue.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e9b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6e9b-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_CUE_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_VCR_CUE_PARMS;
```



## <a name="members"></a><span data-ttu-id="c6e9b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c6e9b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c6e9b-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c6e9b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c6e9b-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="c6e9b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c6e9b-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="c6e9b-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="c6e9b-111">Position de départ.</span><span class="sxs-lookup"><span data-stu-id="c6e9b-111">Position to cue from.</span></span>

</dd> <dt>

<span data-ttu-id="c6e9b-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="c6e9b-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="c6e9b-113">Position à laquelle signaler.</span><span class="sxs-lookup"><span data-stu-id="c6e9b-113">Position to cue to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6e9b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c6e9b-114">Remarks</span></span>

<span data-ttu-id="c6e9b-115">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="c6e9b-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e9b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6e9b-116">Requirements</span></span>



| <span data-ttu-id="c6e9b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6e9b-117">Requirement</span></span> | <span data-ttu-id="c6e9b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6e9b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c6e9b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e9b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e9b-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e9b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c6e9b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e9b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e9b-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e9b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c6e9b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6e9b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e9b-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6e9b-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6e9b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6e9b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e9b-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c6e9b-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c6e9b-127">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="c6e9b-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c6e9b-128">**\_signal MCI**</span><span class="sxs-lookup"><span data-stu-id="c6e9b-128">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

<span data-ttu-id="c6e9b-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6e9b-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

