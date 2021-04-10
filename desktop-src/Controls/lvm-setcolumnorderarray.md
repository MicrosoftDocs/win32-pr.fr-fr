---
title: Message LVM_SETCOLUMNORDERARRAY (commctrl. h)
description: Définit l’ordre de gauche à droite des colonnes dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetColumnOrderArray.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032351"
---
# <a name="lvm_setcolumnorderarray-message"></a><span data-ttu-id="55e22-105">\_Message SETCOLUMNORDERARRAY LVM</span><span class="sxs-lookup"><span data-stu-id="55e22-105">LVM\_SETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="55e22-106">Définit l’ordre de gauche à droite des colonnes dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="55e22-106">Sets the left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="55e22-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="55e22-107">You can send this message explicitly or use the [**ListView\_SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="55e22-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55e22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55e22-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55e22-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55e22-110">Taille, en éléments, de la mémoire tampon au niveau de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="55e22-110">Size, in elements, of the buffer at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="55e22-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55e22-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55e22-112">Pointeur vers un tableau qui spécifie l’ordre dans lequel les colonnes doivent être affichées, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="55e22-112">Pointer to an array that specifies the order in which columns should be displayed, from left to right.</span></span> <span data-ttu-id="55e22-113">Par exemple, si le contenu du tableau est {2,0,1} , le contrôle affiche la colonne 2, la colonne 0 et la colonne 1 dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="55e22-113">For example, if the contents of the array are {2,0,1}, the control displays column 2, column 0, and column 1 in that order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55e22-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55e22-114">Return value</span></span>

<span data-ttu-id="55e22-115">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="55e22-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="55e22-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55e22-116">Requirements</span></span>



| <span data-ttu-id="55e22-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55e22-117">Requirement</span></span> | <span data-ttu-id="55e22-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="55e22-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55e22-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55e22-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55e22-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55e22-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55e22-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55e22-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55e22-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55e22-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55e22-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="55e22-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55e22-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55e22-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





