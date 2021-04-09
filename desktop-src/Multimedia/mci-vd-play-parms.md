---
title: Structure MCI_VD_PLAY_PARMS (Mciapi. h)
description: La \_ structure des PARMS de lecture MCI VD contient des \_ \_ informations de position et de vitesse pour la \_ commande MCI Play pour les appareils videodisc.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- Structure de MCI_VD_PLAY_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032902"
---
# <a name="mci_vd_play_parms-structure"></a><span data-ttu-id="1387e-104">\_Structure des \_ PARMS de lecture MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="1387e-104">MCI\_VD\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="1387e-105">La structure des **\_ PARMS de \_ lecture \_ MCI VD** contient des informations de position et de vitesse pour la commande [**MCI \_ Play**](mci-play.md) pour les appareils videodisc.</span><span class="sxs-lookup"><span data-stu-id="1387e-105">The **MCI\_VD\_PLAY\_PARMS** structure contains position and speed information for the [**MCI\_PLAY**](mci-play.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1387e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1387e-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="1387e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1387e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1387e-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="1387e-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="1387e-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="1387e-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="1387e-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="1387e-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="1387e-111">Position à partir de laquelle effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="1387e-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="1387e-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="1387e-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="1387e-113">Position de lecture.</span><span class="sxs-lookup"><span data-stu-id="1387e-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="1387e-114">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="1387e-114">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="1387e-115">Vitesse de lecture en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="1387e-115">Playback speed in frames per second.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1387e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1387e-116">Remarks</span></span>

<span data-ttu-id="1387e-117">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="1387e-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="1387e-118">Vous pouvez utiliser la structure des [**\_ \_ parms de lecture MCI**](mci-play-parms.md) à la place des **\_ \_ \_ parms de lecture MCI** , si vous n’utilisez pas les membres de données étendus.</span><span class="sxs-lookup"><span data-stu-id="1387e-118">You can use the [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure instead of **MCI\_VD\_PLAY\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="1387e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1387e-119">Requirements</span></span>



| <span data-ttu-id="1387e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1387e-120">Requirement</span></span> | <span data-ttu-id="1387e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1387e-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1387e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1387e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1387e-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1387e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1387e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1387e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1387e-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1387e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1387e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1387e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1387e-127"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1387e-127"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1387e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1387e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1387e-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="1387e-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1387e-130">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="1387e-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="1387e-131">**\_lecture MCI**</span><span class="sxs-lookup"><span data-stu-id="1387e-131">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="1387e-132">**\_jeux de lecture MCI \_**</span><span class="sxs-lookup"><span data-stu-id="1387e-132">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
</dt> <dt>

<span data-ttu-id="1387e-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1387e-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

