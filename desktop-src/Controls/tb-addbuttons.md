---
title: Message TB_ADDBUTTONS (commctrl. h)
description: Ajoute un ou plusieurs boutons à une barre d’outils.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942914"
---
# <a name="tb_addbuttons-message"></a><span data-ttu-id="95ec1-104">TO \_ ADDBUTTONS message</span><span class="sxs-lookup"><span data-stu-id="95ec1-104">TB\_ADDBUTTONS message</span></span>

<span data-ttu-id="95ec1-105">Ajoute un ou plusieurs boutons à une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="95ec1-105">Adds one or more buttons to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="95ec1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95ec1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ec1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95ec1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95ec1-108">Nombre de boutons à ajouter.</span><span class="sxs-lookup"><span data-stu-id="95ec1-108">Number of buttons to add.</span></span>

</dd> <dt>

<span data-ttu-id="95ec1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95ec1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95ec1-110">Pointeur vers un tableau de structures [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) qui contiennent des informations sur les boutons à ajouter.</span><span class="sxs-lookup"><span data-stu-id="95ec1-110">Pointer to an array of [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures that contain information about the buttons to add.</span></span> <span data-ttu-id="95ec1-111">Le tableau doit contenir le même nombre d’éléments que les boutons spécifiés par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="95ec1-111">There must be the same number of elements in the array as buttons specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ec1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95ec1-112">Return value</span></span>

<span data-ttu-id="95ec1-113">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="95ec1-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="95ec1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="95ec1-114">Remarks</span></span>

<span data-ttu-id="95ec1-115">Si la barre d’outils a été créée à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , vous devez envoyer le message [**to \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) à la barre d’outils avant d’envoyer **to \_ ADDBUTTONS**.</span><span class="sxs-lookup"><span data-stu-id="95ec1-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBUTTONS**.</span></span>

<span data-ttu-id="95ec1-116">Consultez [**to \_ SETIMAGELIST**](tb-setimagelist.md) pour savoir comment assigner des bitmaps à des boutons de barre d’outils à partir d’une ou plusieurs listes d’images.</span><span class="sxs-lookup"><span data-stu-id="95ec1-116">See [**TB\_SETIMAGELIST**](tb-setimagelist.md) for a discussion of how to assign bitmaps to toolbar buttons from one or more image lists.</span></span>

## <a name="examples"></a><span data-ttu-id="95ec1-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="95ec1-117">Examples</span></span>

<span data-ttu-id="95ec1-118">L’exemple de code suivant ajoute trois boutons à une barre d’outils, à l’aide de la bitmap système standard pour les boutons de vue.</span><span class="sxs-lookup"><span data-stu-id="95ec1-118">The following example code adds three buttons to a toolbar, using the standard system bitmap for view buttons.</span></span> <span data-ttu-id="95ec1-119">Le message [**to \_ ADDBITMAP**](tb-addbitmap.md) retourne l’index de la première image de bouton dans la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="95ec1-119">The [**TB\_ADDBITMAP**](tb-addbitmap.md) message returns the index of the first button image within the image list.</span></span> <span data-ttu-id="95ec1-120">Les images individuelles sont identifiées par leurs décalages par rapport à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="95ec1-120">Individual images are identified by their offsets from that value.</span></span>


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a><span data-ttu-id="95ec1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95ec1-121">Requirements</span></span>



| <span data-ttu-id="95ec1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95ec1-122">Requirement</span></span> | <span data-ttu-id="95ec1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="95ec1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95ec1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95ec1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95ec1-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95ec1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95ec1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95ec1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95ec1-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95ec1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95ec1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="95ec1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95ec1-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="95ec1-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="95ec1-130">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="95ec1-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="95ec1-131">**To \_ ADDBUTTONSW** (Unicode) et **to \_ ADDBUTTONSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="95ec1-131">**TB\_ADDBUTTONSW** (Unicode) and **TB\_ADDBUTTONSA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="95ec1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95ec1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ec1-133">**Valeurs d’index d’image du bouton standard de la barre d’outils**</span><span class="sxs-lookup"><span data-stu-id="95ec1-133">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

