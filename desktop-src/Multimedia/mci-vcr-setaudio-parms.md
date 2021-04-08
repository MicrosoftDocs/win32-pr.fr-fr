---
title: Structure de MCI_VCR_SETAUDIO_PARMS (VCR. h)
description: La \_ \_ structure SETAUDIO PARMS du magnétoscope MCI contient des \_ paramètres pour la \_ commande MCI SETAUDIO pour les enregistreurs vidéo-cassettes.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- Structure de MCI_VCR_SETAUDIO_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843201"
---
# <a name="mci_vcr_setaudio_parms-structure"></a><span data-ttu-id="c372e-104">MCI \_ VCR \_ SETAUDIO \_ PARMS</span><span class="sxs-lookup"><span data-stu-id="c372e-104">MCI\_VCR\_SETAUDIO\_PARMS structure</span></span>

<span data-ttu-id="c372e-105">La **structure \_ \_ SETAUDIO \_ PARMS du magnétoscope MCI** contient des paramètres pour la commande [**MCI \_ SETAUDIO**](mci-setaudio.md) pour les enregistreurs vidéo-cassettes.</span><span class="sxs-lookup"><span data-stu-id="c372e-105">The **MCI\_VCR\_SETAUDIO\_PARMS** structure contains parameters for the [**MCI\_SETAUDIO**](mci-setaudio.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c372e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c372e-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a><span data-ttu-id="c372e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c372e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c372e-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c372e-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c372e-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="c372e-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c372e-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="c372e-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="c372e-111">Piste audio.</span><span class="sxs-lookup"><span data-stu-id="c372e-111">Audio track.</span></span>

</dd> <dt>

<span data-ttu-id="c372e-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="c372e-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="c372e-113">Type d’entrée ou d’entrée analysée.</span><span class="sxs-lookup"><span data-stu-id="c372e-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="c372e-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="c372e-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c372e-115">Entrée audio (du type spécifié dans le membre **dwTo** ) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c372e-115">Audio input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c372e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c372e-116">Remarks</span></span>

<span data-ttu-id="c372e-117">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="c372e-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c372e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c372e-118">Requirements</span></span>



| <span data-ttu-id="c372e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c372e-119">Requirement</span></span> | <span data-ttu-id="c372e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c372e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c372e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c372e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c372e-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c372e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c372e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c372e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c372e-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c372e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c372e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c372e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c372e-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c372e-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c372e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c372e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c372e-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c372e-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c372e-129">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="c372e-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c372e-130">**\_SETAUDIO MCI**</span><span class="sxs-lookup"><span data-stu-id="c372e-130">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
</dt> <dt>

<span data-ttu-id="c372e-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c372e-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

