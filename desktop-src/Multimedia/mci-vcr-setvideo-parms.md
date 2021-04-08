---
title: Structure de MCI_VCR_SETVIDEO_PARMS (VCR. h)
description: La \_ \_ structure SETVIDEO PARMS du magnétoscope MCI contient des \_ paramètres pour la \_ commande MCI SETVIDEO pour les enregistreurs vidéo-cassettes.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- Structure de MCI_VCR_SETVIDEO_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844161"
---
# <a name="mci_vcr_setvideo_parms-structure"></a><span data-ttu-id="ac041-104">MCI \_ VCR \_ SETVIDEO \_ PARMS</span><span class="sxs-lookup"><span data-stu-id="ac041-104">MCI\_VCR\_SETVIDEO\_PARMS structure</span></span>

<span data-ttu-id="ac041-105">La **structure \_ \_ SETVIDEO \_ PARMS du magnétoscope MCI** contient des paramètres pour la commande [**MCI \_ SETVIDEO**](mci-setvideo.md) pour les enregistreurs vidéo-cassettes.</span><span class="sxs-lookup"><span data-stu-id="ac041-105">The **MCI\_VCR\_SETVIDEO\_PARMS** structure contains parameters for the [**MCI\_SETVIDEO**](mci-setvideo.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac041-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac041-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a><span data-ttu-id="ac041-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ac041-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac041-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="ac041-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="ac041-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="ac041-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="ac041-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="ac041-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="ac041-111">Suivi affecté.</span><span class="sxs-lookup"><span data-stu-id="ac041-111">Affected track.</span></span>

</dd> <dt>

<span data-ttu-id="ac041-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="ac041-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="ac041-113">Type d’entrée ou d’entrée analysée.</span><span class="sxs-lookup"><span data-stu-id="ac041-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="ac041-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="ac041-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="ac041-115">Entrée vidéo (du type spécifié dans le membre **dwTo** ) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ac041-115">Video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac041-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ac041-116">Remarks</span></span>

<span data-ttu-id="ac041-117">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="ac041-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac041-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac041-118">Requirements</span></span>



| <span data-ttu-id="ac041-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac041-119">Requirement</span></span> | <span data-ttu-id="ac041-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac041-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ac041-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac041-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ac041-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac041-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ac041-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac041-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ac041-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac041-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ac041-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac041-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac041-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac041-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac041-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac041-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac041-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="ac041-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ac041-129">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="ac041-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="ac041-130">**\_SETVIDEO MCI**</span><span class="sxs-lookup"><span data-stu-id="ac041-130">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
</dt> <dt>

<span data-ttu-id="ac041-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ac041-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

