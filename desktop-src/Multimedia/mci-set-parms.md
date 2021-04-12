---
title: Structure MCI_SET_PARMS (Mciapi. h)
description: La \_ structure set \_ PARMS de MCI contient des informations pour la \_ commande Set MCI.
ms.assetid: 58811a0f-dc89-4303-b2b2-c98933ebab80
keywords:
- Structure de MCI_SET_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971affd319ecae817b9c1159ab0f307d0c2a5c91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032548"
---
# <a name="mci_set_parms-structure"></a><span data-ttu-id="ab2a2-104">MCI \_ définir la \_ structure des PARMS</span><span class="sxs-lookup"><span data-stu-id="ab2a2-104">MCI\_SET\_PARMS structure</span></span>

<span data-ttu-id="ab2a2-105">La **structure \_ Set \_ PARMS de MCI** contient des informations pour la commande [**\_ Set MCI**](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="ab2a2-105">The **MCI\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab2a2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab2a2-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
} MCI_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="ab2a2-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ab2a2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ab2a2-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="ab2a2-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="ab2a2-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="ab2a2-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="ab2a2-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="ab2a2-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ab2a2-111">Format d’heure de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ab2a2-111">Time format for device.</span></span>

</dd> <dt>

<span data-ttu-id="ab2a2-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="ab2a2-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="ab2a2-113">Canal de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="ab2a2-113">Audio output channel.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab2a2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ab2a2-114">Remarks</span></span>

<span data-ttu-id="ab2a2-115">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="ab2a2-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab2a2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab2a2-116">Requirements</span></span>



| <span data-ttu-id="ab2a2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab2a2-117">Requirement</span></span> | <span data-ttu-id="ab2a2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab2a2-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab2a2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab2a2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab2a2-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab2a2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ab2a2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab2a2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab2a2-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab2a2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ab2a2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab2a2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab2a2-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab2a2-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab2a2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab2a2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2a2-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="ab2a2-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ab2a2-127">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="ab2a2-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="ab2a2-128">**jeu de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="ab2a2-128">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="ab2a2-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab2a2-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

