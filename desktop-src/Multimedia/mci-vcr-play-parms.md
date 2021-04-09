---
title: Structure de MCI_VCR_PLAY_PARMS (VCR. h)
description: La \_ structure des paramètres MCI VCR \_ Play contient des \_ paramètres pour la \_ commande MCI Play pour les enregistreurs vidéo-cassettes.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- Structure de MCI_VCR_PLAY_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942236"
---
# <a name="mci_vcr_play_parms-structure"></a><span data-ttu-id="a13d8-104">La \_ \_ structure des PARMS de lecture MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="a13d8-104">MCI\_VCR\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="a13d8-105">La structure des paramètres **MCI \_ VCR \_ Play \_** contient des paramètres pour la commande [**MCI \_ Play**](mci-play.md) pour les enregistreurs vidéo-cassettes.</span><span class="sxs-lookup"><span data-stu-id="a13d8-105">The **MCI\_VCR\_PLAY\_PARMS** structure contains parameters for the [**MCI\_PLAY**](mci-play.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="a13d8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a13d8-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="a13d8-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a13d8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a13d8-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="a13d8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="a13d8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="a13d8-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="a13d8-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-111">Position à partir de laquelle effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="a13d8-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="a13d8-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="a13d8-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-113">Position de lecture.</span><span class="sxs-lookup"><span data-stu-id="a13d8-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="a13d8-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="a13d8-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-115">Valeur de temps qui affecte la commande [**MCI \_ Play**](mci-play.md) ou [**MCI \_ CUE**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="a13d8-115">Time value that affects the [**MCI\_PLAY**](mci-play.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="a13d8-116">Pour la lecture [**MCI \_**](mci-play-parms.md), il s’agit de l’heure de début de la lecture.</span><span class="sxs-lookup"><span data-stu-id="a13d8-116">For [**MCI\_PLAY**](mci-play-parms.md), this is the time when playback begins.</span></span> <span data-ttu-id="a13d8-117">Pour **le \_ signal MCI**, il s’agit de l’heure à laquelle l’appareil de passage atteint la position donnée dans **dwFrom**.</span><span class="sxs-lookup"><span data-stu-id="a13d8-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a13d8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a13d8-118">Remarks</span></span>

<span data-ttu-id="a13d8-119">Les positions sont spécifiées dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="a13d8-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="a13d8-120">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="a13d8-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="a13d8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a13d8-121">Requirements</span></span>



| <span data-ttu-id="a13d8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a13d8-122">Requirement</span></span> | <span data-ttu-id="a13d8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a13d8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a13d8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a13d8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a13d8-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a13d8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a13d8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a13d8-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a13d8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a13d8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a13d8-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="a13d8-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a13d8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a13d8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a13d8-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="a13d8-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a13d8-132">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="a13d8-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="a13d8-133">**\_signal MCI**</span><span class="sxs-lookup"><span data-stu-id="a13d8-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="a13d8-134">**\_lecture MCI**</span><span class="sxs-lookup"><span data-stu-id="a13d8-134">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="a13d8-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a13d8-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

