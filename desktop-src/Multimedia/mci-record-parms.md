---
title: Structure MCI_RECORD_PARMS (Mciapi. h)
description: La \_ \_ structure d’enregistrements MCI contient des informations de positionnement pour la \_ commande d’enregistrement MCI.
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- Structure de MCI_RECORD_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633ce192d0f4b2467cb744d614ea38056eafb60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464222"
---
# <a name="mci_record_parms-structure"></a><span data-ttu-id="b1eb7-104">Structure des PARMS des \_ enregistrements MCI \_</span><span class="sxs-lookup"><span data-stu-id="b1eb7-104">MCI\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="b1eb7-105">La structure d' **\_ enregistrements \_ MCI** contient des informations de positionnement pour la commande d' [**\_ enregistrement MCI**](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="b1eb7-105">The **MCI\_RECORD\_PARMS** structure contains positioning information for the [**MCI\_RECORD**](mci-record.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1eb7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1eb7-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="b1eb7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b1eb7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1eb7-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="b1eb7-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="b1eb7-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="b1eb7-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="b1eb7-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="b1eb7-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="b1eb7-111">Position à partir de laquelle effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="b1eb7-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="b1eb7-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="b1eb7-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="b1eb7-113">Position de lecture.</span><span class="sxs-lookup"><span data-stu-id="b1eb7-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1eb7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b1eb7-114">Remarks</span></span>

<span data-ttu-id="b1eb7-115">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="b1eb7-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1eb7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1eb7-116">Requirements</span></span>



| <span data-ttu-id="b1eb7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1eb7-117">Requirement</span></span> | <span data-ttu-id="b1eb7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1eb7-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b1eb7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1eb7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1eb7-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1eb7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b1eb7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1eb7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1eb7-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1eb7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b1eb7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1eb7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1eb7-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1eb7-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1eb7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1eb7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1eb7-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="b1eb7-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b1eb7-127">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="b1eb7-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="b1eb7-128">**\_enregistrement MCI**</span><span class="sxs-lookup"><span data-stu-id="b1eb7-128">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="b1eb7-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1eb7-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

