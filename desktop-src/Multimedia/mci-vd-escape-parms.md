---
title: Structure MCI_VD_ESCAPE_PARMS (Mciapi. h)
description: La structure de l' \_ échappement MCI VD \_ \_ contient la commande envoyée à un appareil pour la \_ commande d’échappement MCI pour les appareils videodisc.
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- Structure de MCI_VD_ESCAPE_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80712cd693e2c7ebe290be6b9827c1e051dd86a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511756"
---
# <a name="mci_vd_escape_parms-structure"></a><span data-ttu-id="8ff42-104">Structure de l' \_ échappement MCI VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="8ff42-104">MCI\_VD\_ESCAPE\_PARMS structure</span></span>

<span data-ttu-id="8ff42-105">La structure de l' **\_ \_ \_ échappement MCI VD** contient la commande envoyée à un appareil pour la commande d' [**\_ échappement MCI**](mci-escape.md) pour les appareils videodisc.</span><span class="sxs-lookup"><span data-stu-id="8ff42-105">The **MCI\_VD\_ESCAPE\_PARMS** structure contains the command sent to a device for the [**MCI\_ESCAPE**](mci-escape.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff42-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ff42-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a><span data-ttu-id="8ff42-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8ff42-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ff42-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="8ff42-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8ff42-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="8ff42-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="8ff42-110">**lpstrCommand**</span><span class="sxs-lookup"><span data-stu-id="8ff42-110">**lpstrCommand**</span></span>
</dt> <dd>

<span data-ttu-id="8ff42-111">Commande à envoyer à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8ff42-111">Command to send to device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ff42-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8ff42-112">Remarks</span></span>

<span data-ttu-id="8ff42-113">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="8ff42-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff42-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ff42-114">Requirements</span></span>



| <span data-ttu-id="8ff42-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ff42-115">Requirement</span></span> | <span data-ttu-id="8ff42-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ff42-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff42-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ff42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff42-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ff42-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8ff42-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ff42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff42-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ff42-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8ff42-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ff42-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ff42-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff42-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ff42-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ff42-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff42-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="8ff42-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8ff42-125">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="8ff42-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="8ff42-126">**\_échappement MCI**</span><span class="sxs-lookup"><span data-stu-id="8ff42-126">**MCI\_ESCAPE**</span></span>](mci-escape.md)
</dt> <dt>

<span data-ttu-id="8ff42-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8ff42-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

