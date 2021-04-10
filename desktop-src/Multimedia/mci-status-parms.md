---
title: Structure MCI_STATUS_PARMS (Mciapi. h)
description: La \_ \_ structure de l’état de MCI contient des informations sur la \_ commande d’État MCI.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- Structure de MCI_STATUS_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941783"
---
# <a name="mci_status_parms-structure"></a><span data-ttu-id="0bafa-104">Structure de l' \_ État MCI \_</span><span class="sxs-lookup"><span data-stu-id="0bafa-104">MCI\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="0bafa-105">La structure de l' **\_ état \_ de MCI** contient des informations sur la commande d' [**\_ État MCI**](mci-status.md) .</span><span class="sxs-lookup"><span data-stu-id="0bafa-105">The **MCI\_STATUS\_PARMS** structure contains information for the [**MCI\_STATUS**](mci-status.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bafa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bafa-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="0bafa-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0bafa-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0bafa-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="0bafa-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0bafa-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="0bafa-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0bafa-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="0bafa-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="0bafa-111">Contient des informations sur le retour.</span><span class="sxs-lookup"><span data-stu-id="0bafa-111">Contains information on return.</span></span>

</dd> <dt>

<span data-ttu-id="0bafa-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="0bafa-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="0bafa-113">Fonctionnalité en cours d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="0bafa-113">Capability being queried.</span></span>

</dd> <dt>

<span data-ttu-id="0bafa-114">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="0bafa-114">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="0bafa-115">Longueur ou nombre de pistes.</span><span class="sxs-lookup"><span data-stu-id="0bafa-115">Length or number of tracks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bafa-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0bafa-116">Remarks</span></span>

<span data-ttu-id="0bafa-117">L' \_ indicateur d’élément d’État MCI \_ doit être défini dans le paramètre *fdwCommand* de la fonction [**MciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider le membre **dwItem** , qui doit contenir l’une des constantes indiquant les informations d’État demandées.</span><span class="sxs-lookup"><span data-stu-id="0bafa-117">The MCI\_STATUS\_ITEM flag must be set in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the **dwItem** member, which should contain one of the constants indicating what status information is being requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bafa-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bafa-118">Requirements</span></span>



| <span data-ttu-id="0bafa-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bafa-119">Requirement</span></span> | <span data-ttu-id="0bafa-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bafa-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0bafa-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bafa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0bafa-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bafa-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0bafa-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bafa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0bafa-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bafa-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0bafa-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bafa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bafa-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bafa-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bafa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bafa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bafa-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="0bafa-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0bafa-129">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="0bafa-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0bafa-130">**\_État MCI**</span><span class="sxs-lookup"><span data-stu-id="0bafa-130">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="0bafa-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bafa-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

