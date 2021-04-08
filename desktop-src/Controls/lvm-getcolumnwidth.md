---
title: Message LVM_GETCOLUMNWIDTH (commctrl. h)
description: Obtient la largeur d’une colonne en mode rapport ou liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetColumnWidth.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102900"
---
# <a name="lvm_getcolumnwidth-message"></a><span data-ttu-id="b66df-105">\_Message GETCOLUMNWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="b66df-105">LVM\_GETCOLUMNWIDTH message</span></span>

<span data-ttu-id="b66df-106">Obtient la largeur d’une colonne en mode rapport ou liste.</span><span class="sxs-lookup"><span data-stu-id="b66df-106">Gets the width of a column in report or list view.</span></span> <span data-ttu-id="b66df-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="b66df-107">You can send this message explicitly or by using the [**ListView\_GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b66df-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b66df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b66df-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b66df-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b66df-110">Index de la colonne.</span><span class="sxs-lookup"><span data-stu-id="b66df-110">The index of the column.</span></span> <span data-ttu-id="b66df-111">Ce paramètre est ignoré en mode liste.</span><span class="sxs-lookup"><span data-stu-id="b66df-111">This parameter is ignored in list view.</span></span>

</dd> <dt>

<span data-ttu-id="b66df-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b66df-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b66df-113">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b66df-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b66df-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b66df-114">Return value</span></span>

<span data-ttu-id="b66df-115">Retourne la largeur de colonne en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b66df-115">Returns the column width if successful, or zero otherwise.</span></span> <span data-ttu-id="b66df-116">Si ce message est envoyé à un contrôle List-View avec le style de [**\_ rapport LVS**](list-view-window-styles.md) et que la colonne spécifiée n’existe pas, la valeur de retour n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="b66df-116">If this message is sent to a list-view control with the [**LVS\_REPORT**](list-view-window-styles.md) style and the specified column does not exist, the return value is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="b66df-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b66df-117">Requirements</span></span>



| <span data-ttu-id="b66df-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b66df-118">Requirement</span></span> | <span data-ttu-id="b66df-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b66df-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b66df-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b66df-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b66df-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b66df-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b66df-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b66df-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b66df-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b66df-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b66df-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b66df-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b66df-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b66df-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





