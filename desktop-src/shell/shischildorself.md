---
UID: ''
title: SHIsChildOrSelf fonction)
description: Compare si une fenêtre est égale à, un enfant ou un descendant de, une deuxième fenêtre.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104990876"
---
# <a name="shischildorself-function"></a><span data-ttu-id="d943f-103">SHIsChildOrSelf fonction)</span><span class="sxs-lookup"><span data-stu-id="d943f-103">SHIsChildOrSelf function</span></span>

## <a name="description"></a><span data-ttu-id="d943f-104">Description</span><span class="sxs-lookup"><span data-stu-id="d943f-104">Description</span></span>

<span data-ttu-id="d943f-105">\[Cette fonction est disponible via Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d943f-105">\[This function is available through Windows XP and Windows Server 2003.</span></span>
<span data-ttu-id="d943f-106">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d943f-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d943f-107">Compare si une fenêtre est égale à, un enfant ou un descendant de, une deuxième fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d943f-107">Compares whether a window is equal to, a child of, or a descendant of, a second window.</span></span>

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a><span data-ttu-id="d943f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d943f-108">Parameters</span></span>

### <a name="hwndparent-in"></a><span data-ttu-id="d943f-109">hwndParent [in]</span><span class="sxs-lookup"><span data-stu-id="d943f-109">hwndParent [in]</span></span>

<span data-ttu-id="d943f-110">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="d943f-110">Type: **HWND**</span></span>

<span data-ttu-id="d943f-111">Handle de la première fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d943f-111">A handle to the first window.</span></span>

### <a name="hwnd-in"></a><span data-ttu-id="d943f-112">HWND [in]</span><span class="sxs-lookup"><span data-stu-id="d943f-112">hwnd [in]</span></span>

<span data-ttu-id="d943f-113">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="d943f-113">Type: **HWND**</span></span>

<span data-ttu-id="d943f-114">Handle d’une fenêtre à tester par rapport à *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="d943f-114">A handle to a window to be tested against *hwndParent*.</span></span>

## <a name="returns"></a><span data-ttu-id="d943f-115">Retours</span><span class="sxs-lookup"><span data-stu-id="d943f-115">Returns</span></span>

<span data-ttu-id="d943f-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d943f-116">Type: **HRESULT**</span></span>

<span data-ttu-id="d943f-117">Retourne **S_OK** si la fenêtre spécifiée par *HWND* est égale à, un enfant de ou un descendant de la fenêtre spécifiée par *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="d943f-117">Returns **S_OK** if the window specified by *hwnd* is equal to, a child of, or a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="d943f-118">Retourne **S_FALSE** si la fenêtre spécifiée par HWND n’est pas égale à, pas un enfant de, et pas un descendant de la fenêtre spécifiée par *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="d943f-118">Returns **S_FALSE** if the window specified by hwnd is not equal to, not a child of, and not a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="d943f-119">La valeur de retour n’est pas définie si l’un des handles de fenêtre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d943f-119">The return value is undefined if either window handle is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="d943f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d943f-120">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="d943f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d943f-121">See also</span></span>

[<span data-ttu-id="d943f-122">IsChild,</span><span class="sxs-lookup"><span data-stu-id="d943f-122">IsChild</span></span>](/windows/desktop/api/winuser/nf-winuser-ischild)
