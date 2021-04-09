---
title: Message TB_BUTTONSTRUCTSIZE (commctrl. h)
description: Spécifie la taille de la structure TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- TB_BUTTONSTRUCTSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033267"
---
# <a name="tb_buttonstructsize-message"></a><span data-ttu-id="14c38-104">TO \_ BUTTONSTRUCTSIZE message</span><span class="sxs-lookup"><span data-stu-id="14c38-104">TB\_BUTTONSTRUCTSIZE message</span></span>

<span data-ttu-id="14c38-105">Spécifie la taille de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="14c38-105">Specifies the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

## <a name="parameters"></a><span data-ttu-id="14c38-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14c38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c38-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14c38-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14c38-108">Taille, en octets, de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="14c38-108">Size, in bytes, of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

</dd> <dt>

<span data-ttu-id="14c38-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14c38-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="14c38-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="14c38-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c38-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14c38-111">Return value</span></span>

<span data-ttu-id="14c38-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="14c38-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14c38-113">Notes</span><span class="sxs-lookup"><span data-stu-id="14c38-113">Remarks</span></span>

<span data-ttu-id="14c38-114">Le système utilise la taille pour déterminer la version de la bibliothèque de liens dynamiques (DLL) de contrôle commun qui est utilisée.</span><span class="sxs-lookup"><span data-stu-id="14c38-114">The system uses the size to determine which version of the common control dynamic-link library (DLL) is being used.</span></span>

<span data-ttu-id="14c38-115">Si une application utilise la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) pour créer la barre d’outils, l’application doit envoyer ce message à la barre d’outils avant d’envoyer le message [**to \_ ADDBITMAP**](tb-addbitmap.md) ou [**to \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="14c38-115">If an application uses the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create the toolbar, the application must send this message to the toolbar before sending the [**TB\_ADDBITMAP**](tb-addbitmap.md) or [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="14c38-116">La fonction [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) envoie automatiquement **to \_ BUTTONSTRUCTSIZE**, et la taille de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) est un paramètre de la fonction.</span><span class="sxs-lookup"><span data-stu-id="14c38-116">The [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function automatically sends **TB\_BUTTONSTRUCTSIZE**, and the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure is a parameter of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c38-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14c38-117">Requirements</span></span>



| <span data-ttu-id="14c38-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14c38-118">Requirement</span></span> | <span data-ttu-id="14c38-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="14c38-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14c38-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14c38-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14c38-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14c38-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14c38-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14c38-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14c38-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14c38-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14c38-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="14c38-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="14c38-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c38-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

