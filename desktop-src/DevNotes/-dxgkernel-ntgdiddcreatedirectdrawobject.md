---
description: Crée une représentation côté noyau de l’objet Microsoft DirectDraw.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: NtGdiDdCreateDirectDrawObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110130"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a><span data-ttu-id="f9e7b-103">NtGdiDdCreateDirectDrawObject fonction)</span><span class="sxs-lookup"><span data-stu-id="f9e7b-103">NtGdiDdCreateDirectDrawObject function</span></span>

<span data-ttu-id="f9e7b-104">\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f9e7b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="f9e7b-105">Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]</span><span class="sxs-lookup"><span data-stu-id="f9e7b-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="f9e7b-106">Crée une représentation côté noyau de l’objet Microsoft DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f9e7b-106">Creates a kernel-side representation of the Microsoft DirectDraw object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e7b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9e7b-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a><span data-ttu-id="f9e7b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9e7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9e7b-109">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9e7b-109">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9e7b-110">Tout périphérique d’affichage DC pour lequel l’objet DirectDraw doit être créé.</span><span class="sxs-lookup"><span data-stu-id="f9e7b-110">Any DC display device for which the DirectDraw object should be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9e7b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9e7b-111">Return value</span></span>

<span data-ttu-id="f9e7b-112">En cas de réussite, cette fonction retourne un handle vers la représentation d’objet en mode noyau. Sinon, elle retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f9e7b-112">If successful, this function returns a handle to the kernel-mode object representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9e7b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f9e7b-113">Remarks</span></span>

<span data-ttu-id="f9e7b-114">Il est recommandé aux applications d’utiliser les API DirectDraw et [Direct3D](../direct3d10/d3d10-graphics-reference.md) pour créer et gérer des objets d’appareils graphiques.</span><span class="sxs-lookup"><span data-stu-id="f9e7b-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="f9e7b-115">Ces constructions résument le processus de création d’appareils de façon simplifiée et indépendante du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f9e7b-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e7b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9e7b-116">Requirements</span></span>



| <span data-ttu-id="f9e7b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9e7b-117">Requirement</span></span> | <span data-ttu-id="f9e7b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9e7b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e7b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9e7b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e7b-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9e7b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f9e7b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9e7b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e7b-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9e7b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f9e7b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9e7b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9e7b-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e7b-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9e7b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9e7b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e7b-126">Prise en charge des clients de bas niveau</span><span class="sxs-lookup"><span data-stu-id="f9e7b-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="f9e7b-127">**DdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="f9e7b-127">**DdCreateDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
