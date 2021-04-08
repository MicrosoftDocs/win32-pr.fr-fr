---
title: Structure de MCI_VCR_SETTUNER_PARMS (VCR. h)
description: La \_ \_ structure SETTUNER PARMS du magnétoscope MCI contient des \_ paramètres pour la \_ commande MCI SETTUNER pour les enregistreurs vidéo-cassettes.
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- Structure de MCI_VCR_SETTUNER_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741804"
---
# <a name="mci_vcr_settuner_parms-structure"></a><span data-ttu-id="c5d89-104">MCI \_ VCR \_ SETTUNER \_ PARMS</span><span class="sxs-lookup"><span data-stu-id="c5d89-104">MCI\_VCR\_SETTUNER\_PARMS structure</span></span>

<span data-ttu-id="c5d89-105">La **structure \_ \_ SETTUNER \_ PARMS du magnétoscope MCI** contient des paramètres pour la commande [**MCI \_ SETTUNER**](mci-settuner.md) pour les enregistreurs vidéo-cassettes.</span><span class="sxs-lookup"><span data-stu-id="c5d89-105">The **MCI\_VCR\_SETTUNER\_PARMS** structure contains parameters for the [**MCI\_SETTUNER**](mci-settuner.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d89-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5d89-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a><span data-ttu-id="c5d89-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c5d89-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5d89-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c5d89-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="c5d89-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-110">**dwChannel**</span><span class="sxs-lookup"><span data-stu-id="c5d89-110">**dwChannel**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-111">Nouveau numéro de canal.</span><span class="sxs-lookup"><span data-stu-id="c5d89-111">New channel number.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-112">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="c5d89-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-113">Tuner logique affecté par la commande [**MCI \_ SETTUNER**](mci-settuner.md) .</span><span class="sxs-lookup"><span data-stu-id="c5d89-113">Logical tuner that the [**MCI\_SETTUNER**](mci-settuner.md) command affects.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5d89-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c5d89-114">Remarks</span></span>

<span data-ttu-id="c5d89-115">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="c5d89-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d89-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5d89-116">Requirements</span></span>



| <span data-ttu-id="c5d89-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5d89-117">Requirement</span></span> | <span data-ttu-id="c5d89-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d89-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5d89-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5d89-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d89-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5d89-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c5d89-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5d89-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d89-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5d89-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c5d89-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5d89-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5d89-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d89-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d89-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5d89-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d89-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c5d89-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c5d89-127">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="c5d89-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c5d89-128">**\_SETTUNER MCI**</span><span class="sxs-lookup"><span data-stu-id="c5d89-128">**MCI\_SETTUNER**</span></span>](mci-settuner.md)
</dt> <dt>

<span data-ttu-id="c5d89-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5d89-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

