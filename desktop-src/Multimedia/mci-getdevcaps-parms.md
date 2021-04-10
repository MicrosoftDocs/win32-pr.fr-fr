---
title: Structure MCI_GETDEVCAPS_PARMS (Mciapi. h)
description: La structure de MCI \_ GETDEVCAPS \_ PARMS contient des informations sur les fonctionnalités de l’appareil pour la \_ commande MCI GETDEVCAPS.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- Structure de MCI_GETDEVCAPS_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032553"
---
# <a name="mci_getdevcaps_parms-structure"></a><span data-ttu-id="e2591-104">MCI \_ GETDEVCAPS \_ PARMS, structure</span><span class="sxs-lookup"><span data-stu-id="e2591-104">MCI\_GETDEVCAPS\_PARMS structure</span></span>

<span data-ttu-id="e2591-105">La structure de **MCI \_ GETDEVCAPS \_ PARMS** contient des informations sur les fonctionnalités de l’appareil pour la commande [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="e2591-105">The **MCI\_GETDEVCAPS\_PARMS** structure contains device-capability information for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2591-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2591-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a><span data-ttu-id="e2591-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e2591-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2591-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="e2591-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="e2591-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="e2591-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="e2591-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="e2591-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="e2591-111">Contient des informations à la sortie.</span><span class="sxs-lookup"><span data-stu-id="e2591-111">Contains information on exit.</span></span>

</dd> <dt>

<span data-ttu-id="e2591-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="e2591-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="e2591-113">Fonctionnalité en cours d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="e2591-113">Capability being queried.</span></span> <span data-ttu-id="e2591-114">Ce membre peut être l’une des constantes listées dans la documentation de référence pour la commande [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="e2591-114">This member can be one of the constants listed in the reference material for the [**MCI\_GETDEVCAPS**](mci-getdevcaps.md) command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2591-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e2591-115">Remarks</span></span>

<span data-ttu-id="e2591-116">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="e2591-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2591-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2591-117">Requirements</span></span>



| <span data-ttu-id="e2591-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2591-118">Requirement</span></span> | <span data-ttu-id="e2591-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2591-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2591-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2591-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e2591-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2591-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e2591-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2591-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e2591-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2591-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e2591-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2591-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2591-125"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2591-125"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2591-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2591-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2591-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="e2591-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e2591-128">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="e2591-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="e2591-129">**\_GETDEVCAPS MCI**</span><span class="sxs-lookup"><span data-stu-id="e2591-129">**MCI\_GETDEVCAPS**</span></span>](mci-getdevcaps.md)
</dt> <dt>

<span data-ttu-id="e2591-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e2591-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

