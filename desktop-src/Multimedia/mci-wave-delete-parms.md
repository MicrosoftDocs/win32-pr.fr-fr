---
title: Structure MCI_WAVE_DELETE_PARMS (Mciapi. h)
description: La \_ structure MCI Wave \_ Delete \_ PARMS contient des informations sur la position de la \_ commande MCI Delete pour les périphériques audio Waveform.
ms.assetid: 5c0bf0ca-773b-4b96-8b55-9ef7b5a306d9
keywords:
- Structure de MCI_WAVE_DELETE_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_WAVE_DELETE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 286c6443a229da266dae4992687c0e9ead5640bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464619"
---
# <a name="mci_wave_delete_parms-structure"></a><span data-ttu-id="3c033-104">Structure de suppression des sons MCI \_ Wave \_ \_</span><span class="sxs-lookup"><span data-stu-id="3c033-104">MCI\_WAVE\_DELETE\_PARMS structure</span></span>

<span data-ttu-id="3c033-105">La structure **MCI \_ Wave \_ Delete \_ PARMS** contient des informations sur la position de la commande [**MCI \_ Delete**](mci-delete.md) pour les périphériques audio Waveform.</span><span class="sxs-lookup"><span data-stu-id="3c033-105">The **MCI\_WAVE\_DELETE\_PARMS** structure contains position information for the [**MCI\_DELETE**](mci-delete.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c033-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c033-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_WAVE_DELETE_PARMS;
```



## <a name="members"></a><span data-ttu-id="3c033-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3c033-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3c033-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="3c033-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3c033-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="3c033-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3c033-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="3c033-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="3c033-111">Position à partir de laquelle effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="3c033-111">Position to delete from.</span></span>

</dd> <dt>

<span data-ttu-id="3c033-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="3c033-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="3c033-113">Position à supprimer.</span><span class="sxs-lookup"><span data-stu-id="3c033-113">Position to delete to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c033-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3c033-114">Remarks</span></span>

<span data-ttu-id="3c033-115">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="3c033-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c033-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c033-116">Requirements</span></span>



| <span data-ttu-id="3c033-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c033-117">Requirement</span></span> | <span data-ttu-id="3c033-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c033-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c033-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c033-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c033-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c033-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3c033-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c033-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c033-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c033-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3c033-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c033-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c033-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c033-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c033-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c033-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c033-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3c033-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3c033-127">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="3c033-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3c033-128">**suppression de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="3c033-128">**MCI\_DELETE**</span></span>](mci-delete.md)
</dt> <dt>

<span data-ttu-id="3c033-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c033-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

