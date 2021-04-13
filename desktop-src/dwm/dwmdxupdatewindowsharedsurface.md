---
description: Notifie le DWM d’une mise à jour entrante à une surface partagée de fenêtre.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: DwmDxUpdateWindowSharedSurface fonction)
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528131"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a><span data-ttu-id="b77bc-103">DwmDxUpdateWindowSharedSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="b77bc-103">DwmDxUpdateWindowSharedSurface function</span></span>

<span data-ttu-id="b77bc-104">Notifie le DWM d’une mise à jour entrante à une surface partagée de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b77bc-104">Notifies the DWM of an incoming update to a window shared surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b77bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b77bc-105">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a><span data-ttu-id="b77bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b77bc-106">Parameters</span></span>

`hwnd`

<span data-ttu-id="b77bc-107">[**HWND**](/windows/desktop/winprog/windows-data-types) spécifiant la fenêtre en cours de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b77bc-107">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window being updated.</span></span>

`uiUpdateId`

<span data-ttu-id="b77bc-108">ID de mise à jour extrait de [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span><span class="sxs-lookup"><span data-stu-id="b77bc-108">The update ID retrieved from [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span></span>

`dwFlags`

<span data-ttu-id="b77bc-109">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b77bc-109">Reserved.</span></span>

`hmonitorAssociation`

<span data-ttu-id="b77bc-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b77bc-110">Reserved.</span></span>

`prc`

<span data-ttu-id="b77bc-111">Rectangle de la fenêtre en cours de mise à jour, dans l’espace de coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b77bc-111">The rect of the window being updated, in window coordinate space.</span></span> <span data-ttu-id="b77bc-112">Un rectangle NULL indique qu’aucune région n’a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b77bc-112">A NULL rectangle indicates that no region was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="b77bc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b77bc-113">Return value</span></span>

<span data-ttu-id="b77bc-114">**S \_ OK** en cas de réussite, sinon un HRESULT en échec **.**</span><span class="sxs-lookup"><span data-stu-id="b77bc-114">**S\_OK** if successful, otherwise a FAILED **HRESULT.**</span></span>

## <a name="remarks"></a><span data-ttu-id="b77bc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b77bc-115">Remarks</span></span>

<span data-ttu-id="b77bc-116">Cette API est destinée à l’implémentation d’un pilote ou d’un Runtime Graphics.</span><span class="sxs-lookup"><span data-stu-id="b77bc-116">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="b77bc-117">Une application ne peut pas appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b77bc-117">An application may not call this method.</span></span> <span data-ttu-id="b77bc-118">Cette documentation n’est valide que pour Windows 7, et il n’est pas garanti que cette API existe et qu’elle se comporte de manière similaire sur d’autres versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="b77bc-118">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="b77bc-119">Cette fonction n’est pas présente dans un en-tête ou une bibliothèque de liens statiques, et elle se trouve à l’ordinal 101 dans dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="b77bc-119">This function is not present in any header or static-link library, and it is located at ordinal 101 in dwmapi.dll.</span></span>

<span data-ttu-id="b77bc-120">Cette méthode ne doit être appelée qu’une fois que [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) a retourné la valeur **\_ OK** et qu’elle doit être appelée dans ce scénario, que la surface soit mise à jour ou non.</span><span class="sxs-lookup"><span data-stu-id="b77bc-120">This method should only ever be called after [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) returns **S\_OK**, and must be called in that scenario, regardless of whether the surface is updated or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="b77bc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b77bc-121">Requirements</span></span>

| <span data-ttu-id="b77bc-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b77bc-122">Requirement</span></span> | <span data-ttu-id="b77bc-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b77bc-123">Value</span></span> |
|-|-|
| <span data-ttu-id="b77bc-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b77bc-124">Minimum supported client</span></span> | <span data-ttu-id="b77bc-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b77bc-125">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="b77bc-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b77bc-126">Minimum supported server</span></span> | <span data-ttu-id="b77bc-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b77bc-127">None supported</span></span> |
| <span data-ttu-id="b77bc-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b77bc-128">End of client support</span></span> | <span data-ttu-id="b77bc-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b77bc-129">Windows 7</span></span> |
| <span data-ttu-id="b77bc-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="b77bc-130">Header</span></span> | <span data-ttu-id="b77bc-131">N/A</span><span class="sxs-lookup"><span data-stu-id="b77bc-131">N/A</span></span> |
| <span data-ttu-id="b77bc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b77bc-132">DLL</span></span> | <span data-ttu-id="b77bc-133">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="b77bc-133">Dwmapi.dll</span></span> |
