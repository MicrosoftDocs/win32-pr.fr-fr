---
description: Envoyé à une DLL d’extension lors du chargement de la DLL par le gestionnaire de fichiers.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Message FMEVENT_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973226"
---
# <a name="fmevent_load-message"></a><span data-ttu-id="1e69a-103">FMEVENT le \_ message de chargement</span><span class="sxs-lookup"><span data-stu-id="1e69a-103">FMEVENT\_LOAD message</span></span>

<span data-ttu-id="1e69a-104">Envoyé à une DLL d’extension lors du chargement de la DLL par le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1e69a-104">Sent to an extension DLL when File Manager is loading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e69a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e69a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e69a-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e69a-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e69a-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1e69a-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1e69a-108">*lpfmsld*</span><span class="sxs-lookup"><span data-stu-id="1e69a-108">*lpfmsld*</span></span> 
</dt> <dd>

<span data-ttu-id="1e69a-109">Adresse d’une structure [**de \_ charge FMS**](fms-load.md) qui spécifie la valeur delta de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="1e69a-109">The address of an [**FMS\_LOAD**](fms-load.md) structure that specifies the menu item delta value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e69a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e69a-110">Return value</span></span>

<span data-ttu-id="1e69a-111">Une DLL d’extension doit retourner la **valeur true** pour continuer le chargement de la dll.</span><span class="sxs-lookup"><span data-stu-id="1e69a-111">An extension DLL must return **TRUE** to continue loading the DLL.</span></span> <span data-ttu-id="1e69a-112">Si la DLL retourne la **valeur false**, le gestionnaire de fichiers appelle la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) et met fin à toute communication avec la dll d’extension.</span><span class="sxs-lookup"><span data-stu-id="1e69a-112">If the DLL returns **FALSE**, File Manager calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function and ends any communication with the extension DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e69a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1e69a-113">Remarks</span></span>

<span data-ttu-id="1e69a-114">Une application doit remplir les membres **dwSize nul**, **szMenuName** et **HMENU** dans la structure [**de \_ chargement FMS**](fms-load.md) .</span><span class="sxs-lookup"><span data-stu-id="1e69a-114">An application should fill the **dwSize**, **szMenuName**, and **hMenu** members in the [**FMS\_LOAD**](fms-load.md) structure.</span></span> <span data-ttu-id="1e69a-115">Elle doit également enregistrer la valeur du membre **wMenuDelta** et l’utiliser pour identifier les éléments de menu lors de la modification du menu.</span><span class="sxs-lookup"><span data-stu-id="1e69a-115">It should also save the value of the **wMenuDelta** member and use it to identify menu items when modifying the menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e69a-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1e69a-116">Requirements</span></span>



| <span data-ttu-id="1e69a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e69a-117">Requirement</span></span> | <span data-ttu-id="1e69a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e69a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e69a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e69a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1e69a-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e69a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1e69a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e69a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1e69a-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e69a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1e69a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e69a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e69a-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e69a-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e69a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e69a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e69a-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="1e69a-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
