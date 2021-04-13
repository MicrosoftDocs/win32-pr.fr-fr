---
title: Message SB_SETTIPTEXT (commctrl. h)
description: Définit le texte d’info-bulle pour un composant dans une barre d’État. La barre d’État doit avoir été créée avec le \_ style info-bulles SBT pour activer les info-bulles.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- SB_SETTIPTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466227"
---
# <a name="sb_settiptext-message"></a><span data-ttu-id="0cdc3-105">\_Message SB SETTIPTEXT</span><span class="sxs-lookup"><span data-stu-id="0cdc3-105">SB\_SETTIPTEXT message</span></span>

<span data-ttu-id="0cdc3-106">Définit le texte d’info-bulle pour un composant dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="0cdc3-106">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="0cdc3-107">La barre d’État doit avoir été créée avec le style [**\_ info-bulles SBT**](status-bar-styles.md) pour activer les info-bulles.</span><span class="sxs-lookup"><span data-stu-id="0cdc3-107">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="0cdc3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cdc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cdc3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0cdc3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cdc3-110">Index de base zéro du composant qui recevra le texte d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="0cdc3-110">Zero-based index of the part that will receive the tooltip text.</span></span>

</dd> <dt>

<span data-ttu-id="0cdc3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cdc3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cdc3-112">Pointeur vers une mémoire tampon de caractères qui contient le nouveau texte d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="0cdc3-112">Pointer to a character buffer that contains the new tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cdc3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cdc3-113">Return value</span></span>

<span data-ttu-id="0cdc3-114">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0cdc3-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cdc3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0cdc3-115">Remarks</span></span>

<span data-ttu-id="0cdc3-116">Ce texte d’info-bulle s’affiche dans deux situations :</span><span class="sxs-lookup"><span data-stu-id="0cdc3-116">This tooltip text is displayed in two situations:</span></span>

-   <span data-ttu-id="0cdc3-117">Lorsque le volet correspondant dans la barre d’état contient uniquement une icône.</span><span class="sxs-lookup"><span data-stu-id="0cdc3-117">When the corresponding pane in the status bar contains only an icon.</span></span>
-   <span data-ttu-id="0cdc3-118">Lorsque le volet correspondant dans la barre d’état contient du texte tronqué en raison de la taille du volet.</span><span class="sxs-lookup"><span data-stu-id="0cdc3-118">When the corresponding pane in the status bar contains text that is truncated due to the size of the pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cdc3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cdc3-119">Requirements</span></span>



| <span data-ttu-id="0cdc3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cdc3-120">Requirement</span></span> | <span data-ttu-id="0cdc3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cdc3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cdc3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cdc3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0cdc3-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cdc3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0cdc3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cdc3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0cdc3-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cdc3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cdc3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cdc3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cdc3-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cdc3-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0cdc3-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="0cdc3-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0cdc3-129">**SB \_ SETTIPTEXTW** (Unicode) et **SB \_ SETTIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0cdc3-129">**SB\_SETTIPTEXTW** (Unicode) and **SB\_SETTIPTEXTA** (ANSI)</span></span><br/>               |



 

 





