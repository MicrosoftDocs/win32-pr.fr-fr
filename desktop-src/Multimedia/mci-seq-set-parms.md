---
title: Structure MCI_SEQ_SET_PARMS (Mciapi. h)
description: La \_ structure MCI Seq \_ Set \_ PARMS contient des informations pour la \_ commande MCI Set pour les périphériques MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- Structure de MCI_SEQ_SET_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941784"
---
# <a name="mci_seq_set_parms-structure"></a><span data-ttu-id="c1852-104">MCI \_ Seq \_ définir la \_ structure des PARMS</span><span class="sxs-lookup"><span data-stu-id="c1852-104">MCI\_SEQ\_SET\_PARMS structure</span></span>

<span data-ttu-id="c1852-105">La structure **MCI \_ Seq \_ Set \_ PARMS** contient des informations pour la commande [**MCI \_ Set**](mci-set.md) pour les périphériques MIDI Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c1852-105">The **MCI\_SEQ\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for MIDI sequencer devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1852-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1852-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="c1852-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c1852-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1852-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c1852-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c1852-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="c1852-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c1852-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="c1852-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="c1852-111">Format d’heure de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c1852-111">Sequencer's time format.</span></span>

</dd> <dt>

<span data-ttu-id="c1852-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="c1852-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="c1852-113">Canal de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="c1852-113">Audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="c1852-114">**dwTempo**</span><span class="sxs-lookup"><span data-stu-id="c1852-114">**dwTempo**</span></span>
</dt> <dd>

<span data-ttu-id="c1852-115">Tempo.</span><span class="sxs-lookup"><span data-stu-id="c1852-115">Tempo.</span></span>

</dd> <dt>

<span data-ttu-id="c1852-116">**dwPort**</span><span class="sxs-lookup"><span data-stu-id="c1852-116">**dwPort**</span></span>
</dt> <dd>

<span data-ttu-id="c1852-117">Port.</span><span class="sxs-lookup"><span data-stu-id="c1852-117">Port.</span></span>

</dd> <dt>

<span data-ttu-id="c1852-118">**dwSlave**</span><span class="sxs-lookup"><span data-stu-id="c1852-118">**dwSlave**</span></span>
</dt> <dd>

<span data-ttu-id="c1852-119">Type de synchronisation utilisé par Sequencer pour l’opération subordonnée.</span><span class="sxs-lookup"><span data-stu-id="c1852-119">Type of synchronization used by the sequencer for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="c1852-120">**dwMaster**</span><span class="sxs-lookup"><span data-stu-id="c1852-120">**dwMaster**</span></span>
</dt> <dd>

<span data-ttu-id="c1852-121">Type de synchronisation utilisé par Sequencer pour l’opération maître.</span><span class="sxs-lookup"><span data-stu-id="c1852-121">Type of synchronization used by the sequencer for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="c1852-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="c1852-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c1852-123">Décalage des données.</span><span class="sxs-lookup"><span data-stu-id="c1852-123">Data offset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1852-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c1852-124">Remarks</span></span>

<span data-ttu-id="c1852-125">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="c1852-125">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1852-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1852-126">Requirements</span></span>



| <span data-ttu-id="c1852-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1852-127">Requirement</span></span> | <span data-ttu-id="c1852-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1852-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1852-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1852-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c1852-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1852-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c1852-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1852-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c1852-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1852-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c1852-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1852-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1852-134"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1852-134"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1852-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1852-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1852-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c1852-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c1852-137">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="c1852-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c1852-138">**jeu de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="c1852-138">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="c1852-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c1852-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

