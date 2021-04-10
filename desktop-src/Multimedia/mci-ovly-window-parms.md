---
title: Structure MCI_OVLY_WINDOW_PARMS (Mciapi. h)
description: La \_ structure PARMS de la fenêtre OVLY MCI \_ contient des \_ informations de fenêtre pour la \_ commande de fenêtre MCI pour les périphériques de superposition vidéo.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- Structure de MCI_OVLY_WINDOW_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941650"
---
# <a name="mci_ovly_window_parms-structure"></a><span data-ttu-id="d3bf6-104">\_OVLY \_ fenêtre PARMS des fenêtres MCI \_</span><span class="sxs-lookup"><span data-stu-id="d3bf6-104">MCI\_OVLY\_WINDOW\_PARMS structure</span></span>

<span data-ttu-id="d3bf6-105">La structure PARMS de la **\_ \_ \_ fenêtre OVLY MCI** contient des informations de fenêtre pour la commande de [**\_ fenêtre MCI**](mci-window.md) pour les périphériques de superposition vidéo.</span><span class="sxs-lookup"><span data-stu-id="d3bf6-105">The **MCI\_OVLY\_WINDOW\_PARMS** structure contains window-display information for the [**MCI\_WINDOW**](mci-window.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3bf6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3bf6-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a><span data-ttu-id="d3bf6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d3bf6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3bf6-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="d3bf6-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d3bf6-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="d3bf6-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d3bf6-110">**hWnd**</span><span class="sxs-lookup"><span data-stu-id="d3bf6-110">**hWnd**</span></span>
</dt> <dd>

<span data-ttu-id="d3bf6-111">Handle vers la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d3bf6-111">Handle to display window.</span></span>

</dd> <dt>

<span data-ttu-id="d3bf6-112">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="d3bf6-112">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="d3bf6-113">Commande Window-Display.</span><span class="sxs-lookup"><span data-stu-id="d3bf6-113">Window-display command.</span></span>

</dd> <dt>

<span data-ttu-id="d3bf6-114">**lpstrText**</span><span class="sxs-lookup"><span data-stu-id="d3bf6-114">**lpstrText**</span></span>
</dt> <dd>

<span data-ttu-id="d3bf6-115">Titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d3bf6-115">Window caption.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3bf6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d3bf6-116">Remarks</span></span>

<span data-ttu-id="d3bf6-117">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="d3bf6-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3bf6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3bf6-118">Requirements</span></span>



| <span data-ttu-id="d3bf6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3bf6-119">Requirement</span></span> | <span data-ttu-id="d3bf6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3bf6-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d3bf6-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3bf6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d3bf6-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3bf6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d3bf6-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3bf6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d3bf6-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3bf6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d3bf6-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3bf6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3bf6-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3bf6-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3bf6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3bf6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3bf6-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d3bf6-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d3bf6-129">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="d3bf6-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d3bf6-130">**\_fenêtre MCI**</span><span class="sxs-lookup"><span data-stu-id="d3bf6-130">**MCI\_WINDOW**</span></span>](mci-window.md)
</dt> <dt>

<span data-ttu-id="d3bf6-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3bf6-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

