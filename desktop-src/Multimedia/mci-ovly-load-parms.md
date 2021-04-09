---
title: Structure de MCI_OVLY_LOAD_PARMS (mmsystem. h)
description: La \_ structure des PARMS de charge OVLY MCI contient des \_ \_ informations pour la \_ commande de chargement MCI pour les périphériques de superposition vidéo.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- Structure de MCI_OVLY_LOAD_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032330"
---
# <a name="mci_ovly_load_parms-structure"></a><span data-ttu-id="50194-104">\_OVLY de \_ charge de chargement MCI \_</span><span class="sxs-lookup"><span data-stu-id="50194-104">MCI\_OVLY\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="50194-105">La structure des **\_ \_ \_ PARMS de charge OVLY MCI** contient des informations pour la commande de [**\_ chargement MCI**](mci-load.md) pour les périphériques de superposition vidéo.</span><span class="sxs-lookup"><span data-stu-id="50194-105">The **MCI\_OVLY\_LOAD\_PARMS** structure contains information for the [**MCI\_LOAD**](mci-load.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="50194-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50194-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="50194-107">Membres</span><span class="sxs-lookup"><span data-stu-id="50194-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="50194-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="50194-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="50194-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="50194-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="50194-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="50194-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="50194-111">Nom du fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="50194-111">Name of file to load.</span></span>

</dd> <dt>

<span data-ttu-id="50194-112">**Release**</span><span class="sxs-lookup"><span data-stu-id="50194-112">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="50194-113">Identifie la zone de la mémoire tampon vidéo à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="50194-113">Identifies the area of the video buffer to update.</span></span> <span data-ttu-id="50194-114">Les structures [Rect](/previous-versions//ms536136(v=vs.85)) sont gérées différemment dans MCI et dans d’autres parties de Windows. dans MCI, **RC. Right** contient la largeur du rectangle et **RC. Bottom** contient sa hauteur.</span><span class="sxs-lookup"><span data-stu-id="50194-114">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50194-115">Notes</span><span class="sxs-lookup"><span data-stu-id="50194-115">Remarks</span></span>

<span data-ttu-id="50194-116">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="50194-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="50194-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50194-117">Requirements</span></span>



| <span data-ttu-id="50194-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50194-118">Requirement</span></span> | <span data-ttu-id="50194-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="50194-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50194-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50194-120">Minimum supported client</span></span><br/> | <span data-ttu-id="50194-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50194-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="50194-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50194-122">Minimum supported server</span></span><br/> | <span data-ttu-id="50194-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50194-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50194-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="50194-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="50194-125"><dt>MMSYSTEM. h</dt></span><span class="sxs-lookup"><span data-stu-id="50194-125"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50194-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50194-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50194-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="50194-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="50194-128">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="50194-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="50194-129">**\_chargement MCI**</span><span class="sxs-lookup"><span data-stu-id="50194-129">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="50194-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="50194-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="50194-131">[RECTANGULAIRE](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="50194-131">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

