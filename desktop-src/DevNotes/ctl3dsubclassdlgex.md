---
description: Sous-classe tous les contrôles dans une boîte de dialogue et dans la fenêtre de dialogue elle-même.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Ctl3dSubclassDlgEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541475"
---
# <a name="ctl3dsubclassdlgex-function"></a><span data-ttu-id="94fe0-103">Ctl3dSubclassDlgEx fonction)</span><span class="sxs-lookup"><span data-stu-id="94fe0-103">Ctl3dSubclassDlgEx function</span></span>

<span data-ttu-id="94fe0-104">Sous-classe tous les contrôles dans une boîte de dialogue et dans la fenêtre de dialogue elle-même.</span><span class="sxs-lookup"><span data-stu-id="94fe0-104">Subclasses all controls in a dialog box and in the dialog window itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="94fe0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94fe0-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a><span data-ttu-id="94fe0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94fe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94fe0-107">*hwndDlg*</span><span class="sxs-lookup"><span data-stu-id="94fe0-107">*hwndDlg*</span></span> 
</dt> <dd>

<span data-ttu-id="94fe0-108">Handle de la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="94fe0-108">A handle to the dialog window.</span></span>

</dd> <dt>

<span data-ttu-id="94fe0-109">*grbit*</span><span class="sxs-lookup"><span data-stu-id="94fe0-109">*grbit*</span></span> 
</dt> <dd>

<span data-ttu-id="94fe0-110">Types de contrôle à sous-classer.</span><span class="sxs-lookup"><span data-stu-id="94fe0-110">The control types to be subclassed.</span></span> <span data-ttu-id="94fe0-111">Cette valeur peut être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="94fe0-111">This value can be any of the following.</span></span>



| <span data-ttu-id="94fe0-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="94fe0-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="94fe0-113">Signification</span><span class="sxs-lookup"><span data-stu-id="94fe0-113">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <span data-ttu-id="94fe0-114"><dt>**CTL3D \_ BOUTONS**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="94fe0-114"><dt>**CTL3D\_BUTTONS**</dt> <dt>0x0001</dt></span></span> </dl>                 | <span data-ttu-id="94fe0-115">Boutons de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="94fe0-115">Subclass buttons.</span></span><br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <span data-ttu-id="94fe0-116"><dt>**CTL3D \_ ZONES de liste**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="94fe0-116"><dt>**CTL3D\_LISTBOXES**</dt> <dt>0x0002</dt></span></span> </dl>           | <span data-ttu-id="94fe0-117">Zones de liste sous-classe.</span><span class="sxs-lookup"><span data-stu-id="94fe0-117">Subclass list boxes.</span></span><br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <span data-ttu-id="94fe0-118"><dt>**CTL3D \_ MODIFIE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="94fe0-118"><dt>**CTL3D\_EDITS**</dt> <dt>0x0004</dt></span></span> </dl>                       | <span data-ttu-id="94fe0-119">Contrôles d’édition de sous-classes.</span><span class="sxs-lookup"><span data-stu-id="94fe0-119">Subclass edit controls.</span></span><br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <span data-ttu-id="94fe0-120"><dt>**CTL3D \_ COMBOS**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="94fe0-120"><dt>**CTL3D\_COMBOS**</dt> <dt>0x0008</dt></span></span> </dl>                    | <span data-ttu-id="94fe0-121">Zones de liste déroulante de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="94fe0-121">Subclass combo boxes.</span></span><br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <span data-ttu-id="94fe0-122"><dt>**CTL3D \_ STATICTEXTS**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="94fe0-122"><dt>**CTL3D\_STATICTEXTS**</dt> <dt>0x0010</dt></span></span> </dl>     | <span data-ttu-id="94fe0-123">Sous-classe les contrôles de texte statique.</span><span class="sxs-lookup"><span data-stu-id="94fe0-123">Subclass static text controls.</span></span><br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <span data-ttu-id="94fe0-124"><dt>**CTL3D \_ STATICFRAMES**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="94fe0-124"><dt>**CTL3D\_STATICFRAMES**</dt> <dt>0x0020</dt></span></span> </dl>  | <span data-ttu-id="94fe0-125">Trames statiques de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="94fe0-125">Subclass static frames.</span></span><br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <span data-ttu-id="94fe0-126"><dt>**CTL3D \_ Toutes les**</dt> <dt>0xFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="94fe0-126"><dt>**CTL3D\_ALL**</dt> <dt>0xffff</dt></span></span> </dl>                             | <span data-ttu-id="94fe0-127">Sous-classez tous les contrôles.</span><span class="sxs-lookup"><span data-stu-id="94fe0-127">Subclass all controls.</span></span><br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <span data-ttu-id="94fe0-128"><dt>**CTL3D \_ NODLGWINDOW**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="94fe0-128"><dt>**CTL3D\_NODLGWINDOW**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="94fe0-129">Ne sous-classez pas la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="94fe0-129">Do not subclass the dialog window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94fe0-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94fe0-130">Return value</span></span>

<span data-ttu-id="94fe0-131">Retourne la **valeur true** si la fonction est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="94fe0-131">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="94fe0-132">Notes</span><span class="sxs-lookup"><span data-stu-id="94fe0-132">Remarks</span></span>

<span data-ttu-id="94fe0-133">Cette fonction est particulièrement utile dans les applications basées sur C++.</span><span class="sxs-lookup"><span data-stu-id="94fe0-133">This function is especially useful in applications based on C++.</span></span>

<span data-ttu-id="94fe0-134">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="94fe0-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="94fe0-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94fe0-135">Requirements</span></span>



| <span data-ttu-id="94fe0-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94fe0-136">Requirement</span></span> | <span data-ttu-id="94fe0-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="94fe0-137">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94fe0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="94fe0-138">DLL</span></span><br/> | <dl> <span data-ttu-id="94fe0-139"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94fe0-139"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
