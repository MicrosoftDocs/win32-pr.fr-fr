---
title: Message TB_ADDBITMAP (commctrl. h)
description: Ajoute une ou plusieurs images à la liste des images de bouton disponibles pour une barre d’outils.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- TB_ADDBITMAP les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743972"
---
# <a name="tb_addbitmap-message"></a><span data-ttu-id="f26f4-104">TO \_ ADDBITMAP message</span><span class="sxs-lookup"><span data-stu-id="f26f4-104">TB\_ADDBITMAP message</span></span>

<span data-ttu-id="f26f4-105">Ajoute une ou plusieurs images à la liste des images de bouton disponibles pour une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="f26f4-105">Adds one or more images to the list of button images available for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f26f4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f26f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f26f4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f26f4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f26f4-108">Nombre d’images de bouton dans l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="f26f4-108">Number of button images in the bitmap.</span></span> <span data-ttu-id="f26f4-109">Si *lParam* spécifie une image bitmap définie par le système, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f26f4-109">If *lParam* specifies a system-defined bitmap, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="f26f4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f26f4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f26f4-111">Pointeur vers une structure [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) qui contient l’identificateur d’une ressource bitmap et le handle vers l’instance de module avec le fichier exécutable qui contient la ressource bitmap.</span><span class="sxs-lookup"><span data-stu-id="f26f4-111">Pointer to a [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) structure that contains the identifier of a bitmap resource and the handle to the module instance with the executable file that contains the bitmap resource.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f26f4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f26f4-112">Return value</span></span>

<span data-ttu-id="f26f4-113">Retourne l’index de la première nouvelle image en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f26f4-113">Returns the index of the first new image if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f26f4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f26f4-114">Remarks</span></span>

<span data-ttu-id="f26f4-115">Si la barre d’outils a été créée à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , vous devez envoyer le message [**to \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) à la barre d’outils avant d’envoyer **to \_ ADDBITMAP**.</span><span class="sxs-lookup"><span data-stu-id="f26f4-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBITMAP**.</span></span>

## <a name="examples"></a><span data-ttu-id="f26f4-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="f26f4-116">Examples</span></span>

<span data-ttu-id="f26f4-117">L’exemple suivant crée une image bitmap à partir d’une ressource (IDB \_ bitmap1), mappe la couleur d’arrière-plan (noir dans ce cas) à la couleur de la face du bouton système et l’ajoute à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="f26f4-117">The following example creates a bitmap from a resource (IDB\_BITMAP1), maps the background color (black in this case) to the system button face color, and adds it to the toolbar.</span></span>


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a><span data-ttu-id="f26f4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f26f4-118">Requirements</span></span>



| <span data-ttu-id="f26f4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f26f4-119">Requirement</span></span> | <span data-ttu-id="f26f4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f26f4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f26f4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f26f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f26f4-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f26f4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f26f4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f26f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f26f4-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f26f4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f26f4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f26f4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f26f4-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f26f4-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

