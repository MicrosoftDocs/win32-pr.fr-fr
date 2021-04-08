---
title: Structure MCI_SEEK_PARMS (Mciapi. h)
description: La \_ structure MCI Seek \_ PARMS contient des informations de positionnement pour la \_ commande MCI Seek.
ms.assetid: 2c199855-2134-4709-9313-5b8d66ce4f03
keywords:
- Structure de MCI_SEEK_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SEEK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c31f419b2458dedc19c6533e8f0f7fade97026e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740485"
---
# <a name="mci_seek_parms-structure"></a><span data-ttu-id="422ad-104">La \_ structure des PARMS de recherche MCI \_</span><span class="sxs-lookup"><span data-stu-id="422ad-104">MCI\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="422ad-105">La structure **MCI \_ Seek \_ PARMS** contient des informations de positionnement pour la commande [**MCI \_ Seek**](mci-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="422ad-105">The **MCI\_SEEK\_PARMS** structure contains positioning information for the [**MCI\_SEEK**](mci-seek.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="422ad-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="422ad-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
} MCI_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="422ad-107">Membres</span><span class="sxs-lookup"><span data-stu-id="422ad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="422ad-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="422ad-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="422ad-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="422ad-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="422ad-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="422ad-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="422ad-111">Position à laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="422ad-111">Position to seek to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="422ad-112">Notes</span><span class="sxs-lookup"><span data-stu-id="422ad-112">Remarks</span></span>

<span data-ttu-id="422ad-113">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="422ad-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="422ad-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="422ad-114">Requirements</span></span>



| <span data-ttu-id="422ad-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="422ad-115">Requirement</span></span> | <span data-ttu-id="422ad-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="422ad-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="422ad-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="422ad-117">Minimum supported client</span></span><br/> | <span data-ttu-id="422ad-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="422ad-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="422ad-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="422ad-119">Minimum supported server</span></span><br/> | <span data-ttu-id="422ad-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="422ad-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="422ad-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="422ad-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="422ad-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="422ad-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="422ad-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="422ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="422ad-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="422ad-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="422ad-125">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="422ad-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="422ad-126">**\_recherche MCI**</span><span class="sxs-lookup"><span data-stu-id="422ad-126">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="422ad-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="422ad-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

