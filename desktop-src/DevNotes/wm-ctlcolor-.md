---
description: Le \_ message WM CTLCOLOR est utilisé dans les versions 16 bits de Windows pour modifier le jeu de couleurs des zones de liste, les zones de liste des zones de liste déroulante, les boîtes de message, les contrôles de bouton, les contrôles d’édition, les contrôles statiques et les boîtes de dialogue. Remarque pour plus d’informations sur ce message et les versions 32 bits de Windows, consultez la section Notes.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: Message WM_CTLCOLOR (WindowsX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528756"
---
# <a name="wm_ctlcolor-message"></a><span data-ttu-id="5943c-103">\_Message WM CTLCOLOR</span><span class="sxs-lookup"><span data-stu-id="5943c-103">WM\_CTLCOLOR message</span></span>

<span data-ttu-id="5943c-104">Le message **WM \_ CTLCOLOR** est utilisé dans les versions 16 bits de Windows pour modifier le jeu de couleurs des zones de liste, les zones de liste des zones de liste déroulante, les boîtes de message, les contrôles de bouton, les contrôles d’édition, les contrôles statiques et les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5943c-104">The **WM\_CTLCOLOR** message is used in 16-bit versions of Windows to change the color scheme of list boxes, the list boxes of combo boxes, message boxes, button controls, edit controls, static controls, and dialog boxes.</span></span>

> [!Note]  
> <span data-ttu-id="5943c-105">Pour plus d’informations sur ce message et les versions 32 bits de Windows, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5943c-105">For information related to this message and 32-bit versions of Windows, see Remarks.</span></span>

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a><span data-ttu-id="5943c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5943c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5943c-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="5943c-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5943c-108">Handle de la fenêtre de destination.</span><span class="sxs-lookup"><span data-stu-id="5943c-108">A handle to destination window.</span></span>

</dd> <dt>

<span data-ttu-id="5943c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5943c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5943c-110">Handle d’un contexte d’affichage (DC).</span><span class="sxs-lookup"><span data-stu-id="5943c-110">A handle to a display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="5943c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5943c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5943c-112">Handle d’une fenêtre enfant (contrôle).</span><span class="sxs-lookup"><span data-stu-id="5943c-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5943c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5943c-113">Return value</span></span>

<span data-ttu-id="5943c-114">Si une application traite ce message, elle retourne un handle à un pinceau.</span><span class="sxs-lookup"><span data-stu-id="5943c-114">If an application processes this message, it returns a handle to a brush.</span></span> <span data-ttu-id="5943c-115">Le système utilise le pinceau pour peindre l’arrière-plan du contrôle.</span><span class="sxs-lookup"><span data-stu-id="5943c-115">The system uses the brush to paint the background of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="5943c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5943c-116">Remarks</span></span>

<span data-ttu-id="5943c-117">Le message **WM \_ CTLCOLOR** de Windows 16 bits a été remplacé par des notifications plus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5943c-117">The **WM\_CTLCOLOR** message from 16-bit Windows has been replaced by more specific notifications.</span></span> <span data-ttu-id="5943c-118">Ces remplacements sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="5943c-118">These replacements include the following:</span></span>

-   [<span data-ttu-id="5943c-119">**\_CTLCOLORBTN WM**</span><span class="sxs-lookup"><span data-stu-id="5943c-119">**WM\_CTLCOLORBTN**</span></span>](../controls/wm-ctlcolorbtn.md)
-   [<span data-ttu-id="5943c-120">**\_CTLCOLOREDIT WM**</span><span class="sxs-lookup"><span data-stu-id="5943c-120">**WM\_CTLCOLOREDIT**</span></span>](../controls/wm-ctlcoloredit.md)
-   [<span data-ttu-id="5943c-121">**\_CTLCOLORDLG WM**</span><span class="sxs-lookup"><span data-stu-id="5943c-121">**WM\_CTLCOLORDLG**</span></span>](../dlgbox/wm-ctlcolordlg.md)
-   [<span data-ttu-id="5943c-122">**\_CTLCOLORLISTBOX WM**</span><span class="sxs-lookup"><span data-stu-id="5943c-122">**WM\_CTLCOLORLISTBOX**</span></span>](../controls/wm-ctlcolorlistbox.md)
-   [<span data-ttu-id="5943c-123">**\_CTLCOLORSCROLLBAR WM**</span><span class="sxs-lookup"><span data-stu-id="5943c-123">**WM\_CTLCOLORSCROLLBAR**</span></span>](../controls/wm-ctlcolorscrollbar.md)
-   [<span data-ttu-id="5943c-124">**\_CTLCOLORSTATIC WM**</span><span class="sxs-lookup"><span data-stu-id="5943c-124">**WM\_CTLCOLORSTATIC**</span></span>](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a><span data-ttu-id="5943c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5943c-125">Requirements</span></span>



| <span data-ttu-id="5943c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5943c-126">Requirement</span></span> | <span data-ttu-id="5943c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5943c-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5943c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5943c-128">Header</span></span><br/> | <dl> <span data-ttu-id="5943c-129"><dt>WindowsX. h</dt></span><span class="sxs-lookup"><span data-stu-id="5943c-129"><dt>WindowsX.h</dt></span></span> </dl> |



 

 
