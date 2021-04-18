---
title: Structure de MCI_VCR_RECORD_PARMS (VCR. h)
description: La \_ structure de \_ paramètres d’enregistrement magnétoscope MCI \_ contient des paramètres pour la \_ commande d’enregistrement MCI pour les enregistreurs vidéo-cassettes.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- Structure de MCI_VCR_RECORD_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512157"
---
# <a name="mci_vcr_record_parms-structure"></a><span data-ttu-id="810ce-104">\_Structure des \_ PARMS des enregistrements magnétoscope MCI \_</span><span class="sxs-lookup"><span data-stu-id="810ce-104">MCI\_VCR\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="810ce-105">La structure de paramètres d' **\_ \_ \_ enregistrement magnétoscope MCI** contient des paramètres pour la commande d' [**\_ enregistrement MCI**](mci-record.md) pour les enregistreurs vidéo-cassettes.</span><span class="sxs-lookup"><span data-stu-id="810ce-105">The **MCI\_VCR\_RECORD\_PARMS** structure contains parameters for the [**MCI\_RECORD**](mci-record.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="810ce-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="810ce-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="810ce-107">Membres</span><span class="sxs-lookup"><span data-stu-id="810ce-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="810ce-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="810ce-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="810ce-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="810ce-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="810ce-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="810ce-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="810ce-111">Position à partir de laquelle effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="810ce-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="810ce-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="810ce-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="810ce-113">Position de lecture.</span><span class="sxs-lookup"><span data-stu-id="810ce-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="810ce-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="810ce-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="810ce-115">Valeur d’heure qui affecte [**l' \_ enregistrement MCI**](mci-record.md) ou la commande [**MCI \_ CUE**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="810ce-115">Time value that affects the [**MCI\_RECORD**](mci-record.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="810ce-116">Pour **l' \_ enregistrement MCI**, il s’agit de l’heure de début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="810ce-116">For **MCI\_RECORD**, this is the time when recording begins.</span></span> <span data-ttu-id="810ce-117">Pour **le \_ signal MCI**, il s’agit de l’heure à laquelle l’appareil de passage atteint la position donnée dans **dwFrom**.</span><span class="sxs-lookup"><span data-stu-id="810ce-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="810ce-118">Notes</span><span class="sxs-lookup"><span data-stu-id="810ce-118">Remarks</span></span>

<span data-ttu-id="810ce-119">Les positions sont spécifiées dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="810ce-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="810ce-120">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="810ce-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="810ce-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="810ce-121">Requirements</span></span>



| <span data-ttu-id="810ce-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="810ce-122">Requirement</span></span> | <span data-ttu-id="810ce-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="810ce-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="810ce-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="810ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="810ce-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="810ce-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="810ce-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="810ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="810ce-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="810ce-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="810ce-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="810ce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="810ce-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="810ce-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="810ce-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="810ce-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810ce-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="810ce-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="810ce-132">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="810ce-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="810ce-133">**\_signal MCI**</span><span class="sxs-lookup"><span data-stu-id="810ce-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="810ce-134">**\_enregistrement MCI**</span><span class="sxs-lookup"><span data-stu-id="810ce-134">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="810ce-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="810ce-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

