---
title: Structure de MCI_VCR_STATUS_PARMS (VCR. h)
description: La \_ structure d’état des magnétoscopes MCI contient des \_ \_ paramètres pour la \_ commande d’État MCI pour les enregistreurs vidéo-cassettes.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- Structure de MCI_VCR_STATUS_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941735"
---
# <a name="mci_vcr_status_parms-structure"></a><span data-ttu-id="cc090-104">Structure de l' \_ État des magnétoscopes MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="cc090-104">MCI\_VCR\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="cc090-105">La structure d' **\_ \_ état \_ des magnétoscopes MCI** contient des paramètres pour la commande d' [**\_ État MCI**](mci-status.md) pour les enregistreurs vidéo-cassettes.</span><span class="sxs-lookup"><span data-stu-id="cc090-105">The **MCI\_VCR\_STATUS\_PARMS** structure contains parameters for the [**MCI\_STATUS**](mci-status.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc090-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc090-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="cc090-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cc090-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc090-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="cc090-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="cc090-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="cc090-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="cc090-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="cc090-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="cc090-111">Valeur renvoyée par la commande d' [**\_ État MCI**](mci-status.md) .</span><span class="sxs-lookup"><span data-stu-id="cc090-111">Value returned by the [**MCI\_STATUS**](mci-status.md) command.</span></span> <span data-ttu-id="cc090-112">La valeur de retour varie en fonction de la recherche de la commande.</span><span class="sxs-lookup"><span data-stu-id="cc090-112">The return value varies according to the inquiry of the command.</span></span> <span data-ttu-id="cc090-113">Pour plus d’informations, consultez la description de la commande d' [**\_ État MCI**](mci-status-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="cc090-113">For more information, see the description of the [**MCI\_STATUS**](mci-status-parms.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="cc090-114">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="cc090-114">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="cc090-115">Type d’informations demandées.</span><span class="sxs-lookup"><span data-stu-id="cc090-115">Type of information requested.</span></span>

</dd> <dt>

<span data-ttu-id="cc090-116">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="cc090-116">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="cc090-117">Piste audio ou vidéo qui stocke les informations lors de l’enregistrement suivant.</span><span class="sxs-lookup"><span data-stu-id="cc090-117">Audio or video track that will store information during the next recording.</span></span> <span data-ttu-id="cc090-118">Ce membre est utilisé pour retourner des informations lorsque la commande d' [**\_ État MCI**](mci-status-parms.md) se renseigne sur l’état de l’enregistrement vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="cc090-118">This member is used to return information when the [**MCI\_STATUS**](mci-status-parms.md) command inquires about the video or audio recording status.</span></span>

</dd> <dt>

<span data-ttu-id="cc090-119">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="cc090-119">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="cc090-120">Tuner logique auquel le canal actuel est associé.</span><span class="sxs-lookup"><span data-stu-id="cc090-120">Logical tuner that the current channel is associated with.</span></span> <span data-ttu-id="cc090-121">Ce membre est utilisé pour retourner des informations lorsque la commande d' [**\_ État MCI**](mci-status.md) se renseigne sur le numéro de canal actuel.</span><span class="sxs-lookup"><span data-stu-id="cc090-121">This member is used to return information when the [**MCI\_STATUS**](mci-status.md) command inquires about the current channel number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc090-122">Notes</span><span class="sxs-lookup"><span data-stu-id="cc090-122">Remarks</span></span>

<span data-ttu-id="cc090-123">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="cc090-123">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc090-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc090-124">Requirements</span></span>



| <span data-ttu-id="cc090-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc090-125">Requirement</span></span> | <span data-ttu-id="cc090-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc090-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cc090-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc090-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cc090-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc090-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cc090-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc090-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cc090-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc090-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cc090-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc090-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc090-132"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc090-132"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc090-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc090-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc090-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="cc090-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cc090-135">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="cc090-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="cc090-136">**\_État MCI**</span><span class="sxs-lookup"><span data-stu-id="cc090-136">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="cc090-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc090-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

