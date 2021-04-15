---
title: Structure MCI_BREAK_PARMS (Mciapi. h)
description: La \_ structure des interruptions MCI \_ contient le code de clé virtuelle et les informations de fenêtre pour la \_ commande MCI Break.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- Structure de MCI_BREAK_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508477"
---
# <a name="mci_break_parms-structure"></a><span data-ttu-id="08d14-104">\_Structure des arrêts MCI \_</span><span class="sxs-lookup"><span data-stu-id="08d14-104">MCI\_BREAK\_PARMS structure</span></span>

<span data-ttu-id="08d14-105">La structure des **\_ interruptions \_ MCI** contient le code de clé virtuelle et les informations de fenêtre pour la commande [**MCI \_ break**](mci-break.md) .</span><span class="sxs-lookup"><span data-stu-id="08d14-105">The **MCI\_BREAK\_PARMS** structure contains virtual-key code and window information for the [**MCI\_BREAK**](mci-break.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d14-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08d14-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a><span data-ttu-id="08d14-107">Membres</span><span class="sxs-lookup"><span data-stu-id="08d14-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="08d14-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="08d14-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="08d14-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="08d14-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="08d14-110">**nVirtKey**</span><span class="sxs-lookup"><span data-stu-id="08d14-110">**nVirtKey**</span></span>
</dt> <dd>

<span data-ttu-id="08d14-111">Code de la touche virtuelle pour la touche arrêt.</span><span class="sxs-lookup"><span data-stu-id="08d14-111">Virtual-key code for break key.</span></span>

</dd> <dt>

<span data-ttu-id="08d14-112">**hwndBreak**</span><span class="sxs-lookup"><span data-stu-id="08d14-112">**hwndBreak**</span></span>
</dt> <dd>

<span data-ttu-id="08d14-113">Handle de la fenêtre qui doit être la fenêtre active pour la détection des arrêts.</span><span class="sxs-lookup"><span data-stu-id="08d14-113">Handle to the window that must be the current window for break detection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08d14-114">Notes</span><span class="sxs-lookup"><span data-stu-id="08d14-114">Remarks</span></span>

<span data-ttu-id="08d14-115">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="08d14-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span> <span data-ttu-id="08d14-116">Les indicateurs suivants sont définis :</span><span class="sxs-lookup"><span data-stu-id="08d14-116">The following flags are defined:</span></span>

<span data-ttu-id="08d14-117">\_HWND de pause MCI \_</span><span class="sxs-lookup"><span data-stu-id="08d14-117">MCI\_BREAK\_HWND</span></span>

<span data-ttu-id="08d14-118">Valide le membre **hwndBreak** qui spécifie la fenêtre qui doit avoir le focus pour activer la détection de rupture.</span><span class="sxs-lookup"><span data-stu-id="08d14-118">Validates the **hwndBreak** member specifying the window that must have focus to enable break detection.</span></span>

<span data-ttu-id="08d14-119">\_touche pause \_ MCI</span><span class="sxs-lookup"><span data-stu-id="08d14-119">MCI\_BREAK\_KEY</span></span>

<span data-ttu-id="08d14-120">Valide le membre **nVirtKey** spécifiant le code de la touche virtuelle à utiliser pour la touche Attn.</span><span class="sxs-lookup"><span data-stu-id="08d14-120">Validates the **nVirtKey** member specifying the virtual-key code to be used for the break key.</span></span>

<span data-ttu-id="08d14-121">\_Pause MCI \_</span><span class="sxs-lookup"><span data-stu-id="08d14-121">MCI\_BREAK\_OFF</span></span>

<span data-ttu-id="08d14-122">Désactive une clé d’arrêt existante.</span><span class="sxs-lookup"><span data-stu-id="08d14-122">Disables any existing break key.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d14-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08d14-123">Requirements</span></span>



| <span data-ttu-id="08d14-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08d14-124">Requirement</span></span> | <span data-ttu-id="08d14-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="08d14-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="08d14-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08d14-126">Minimum supported client</span></span><br/> | <span data-ttu-id="08d14-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08d14-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="08d14-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08d14-128">Minimum supported server</span></span><br/> | <span data-ttu-id="08d14-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08d14-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="08d14-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="08d14-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="08d14-131"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="08d14-131"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08d14-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08d14-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d14-133">**MCI**</span><span class="sxs-lookup"><span data-stu-id="08d14-133">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="08d14-134">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="08d14-134">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="08d14-135">**\_Pause MCI**</span><span class="sxs-lookup"><span data-stu-id="08d14-135">**MCI\_BREAK**</span></span>](mci-break.md)
</dt> <dt>

<span data-ttu-id="08d14-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08d14-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

