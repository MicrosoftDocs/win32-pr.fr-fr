---
title: Message TVM_GETISEARCHSTRING (commctrl. h)
description: Récupère la chaîne de recherche incrémentielle pour un contrôle Tree-View.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105958"
---
# <a name="tvm_getisearchstring-message"></a><span data-ttu-id="f67a9-104">TVM \_ GETISEARCHSTRING message</span><span class="sxs-lookup"><span data-stu-id="f67a9-104">TVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="f67a9-105">Récupère la chaîne de recherche incrémentielle pour un contrôle Tree-View.</span><span class="sxs-lookup"><span data-stu-id="f67a9-105">Retrieves the incremental search string for a tree-view control.</span></span> <span data-ttu-id="f67a9-106">Le contrôle Tree-View utilise la chaîne de recherche incrémentielle pour sélectionner un élément en fonction des caractères tapés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f67a9-106">The tree-view control uses the incremental search string to select an item based on characters typed by the user.</span></span> <span data-ttu-id="f67a9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetISearchString TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="f67a9-107">You can send this message explicitly or by using the [**TreeView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f67a9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f67a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f67a9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f67a9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f67a9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f67a9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f67a9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f67a9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f67a9-112">Pointeur vers la mémoire tampon qui reçoit la chaîne de recherche incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="f67a9-112">Pointer to the buffer that receives the incremental search string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f67a9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f67a9-113">Return value</span></span>

<span data-ttu-id="f67a9-114">Retourne le nombre de caractères dans la chaîne de recherche incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="f67a9-114">Returns the number of characters in the incremental search string.</span></span>

## <a name="remarks"></a><span data-ttu-id="f67a9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f67a9-115">Remarks</span></span>

<span data-ttu-id="f67a9-116">**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="f67a9-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="f67a9-117">Vous devez allouer une mémoire tampon suffisamment grande pour contenir la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f67a9-117">You must allocate a large enough buffer to hold the string.</span></span> <span data-ttu-id="f67a9-118">Appelez tout d’abord le message qui passe **null** dans *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f67a9-118">First call the message passing **NULL** in *lParam*.</span></span> <span data-ttu-id="f67a9-119">Cela retourne le nombre de caractères, à l’exception de **null**, qui sont requis.</span><span class="sxs-lookup"><span data-stu-id="f67a9-119">This returns the number of characters, excluding **NULL**, that are required.</span></span> <span data-ttu-id="f67a9-120">Ensuite, appelez le message une seconde fois pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f67a9-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="f67a9-121">Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="f67a9-121">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="f67a9-122">Si le contrôle Tree-View n’est pas en mode de recherche incrémentielle, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="f67a9-122">If the tree-view control is not in incremental search mode, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f67a9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f67a9-123">Requirements</span></span>



| <span data-ttu-id="f67a9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f67a9-124">Requirement</span></span> | <span data-ttu-id="f67a9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f67a9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f67a9-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f67a9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f67a9-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f67a9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f67a9-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f67a9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f67a9-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f67a9-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f67a9-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f67a9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f67a9-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f67a9-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f67a9-132">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f67a9-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f67a9-133">**TVM \_ GETISEARCHSTRINGW** (Unicode) et **TVM \_ GETISEARCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f67a9-133">**TVM\_GETISEARCHSTRINGW** (Unicode) and **TVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





