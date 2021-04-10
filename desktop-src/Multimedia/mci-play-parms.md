---
title: Structure MCI_PLAY_PARMS (Mciapi. h)
description: La \_ \_ structure des PARMS de lecture MCI contient des informations de positionnement pour la \_ commande MCI Play.
ms.assetid: f1bacf61-ec14-4391-b227-20b35c0bbbc3
keywords:
- Structure de MCI_PLAY_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f207737d4eb93e280355d0e5041b6e7bfc1b3048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941649"
---
# <a name="mci_play_parms-structure"></a><span data-ttu-id="3275c-104">La \_ structure des PARMS de lecture MCI \_</span><span class="sxs-lookup"><span data-stu-id="3275c-104">MCI\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="3275c-105">La structure des **\_ \_ PARMS de lecture MCI** contient des informations de positionnement pour la commande [**MCI \_ Play**](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="3275c-105">The **MCI\_PLAY\_PARMS** structure contains positioning information for the [**MCI\_PLAY**](mci-play.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="3275c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3275c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="3275c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3275c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3275c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="3275c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="3275c-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="3275c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="3275c-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="3275c-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="3275c-111">Position à partir de laquelle effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="3275c-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="3275c-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="3275c-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="3275c-113">Position de lecture.</span><span class="sxs-lookup"><span data-stu-id="3275c-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3275c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3275c-114">Remarks</span></span>

<span data-ttu-id="3275c-115">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="3275c-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="3275c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3275c-116">Requirements</span></span>



| <span data-ttu-id="3275c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3275c-117">Requirement</span></span> | <span data-ttu-id="3275c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3275c-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3275c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3275c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3275c-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3275c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3275c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3275c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3275c-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3275c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3275c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3275c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3275c-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3275c-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3275c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3275c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3275c-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="3275c-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3275c-127">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="3275c-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="3275c-128">**\_lecture MCI**</span><span class="sxs-lookup"><span data-stu-id="3275c-128">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="3275c-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3275c-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

