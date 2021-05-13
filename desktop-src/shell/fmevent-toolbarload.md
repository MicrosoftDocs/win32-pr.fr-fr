---
description: Envoyé à une DLL d’extension lorsque le gestionnaire de fichiers charge sa barre d’outils. Ce message permet à une DLL d’extension d’ajouter un bouton à la barre d’outils du gestionnaire de fichiers.
title: Message FMEVENT_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: c4195acedbd696679a2deea2f4d6e268717566d1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841270"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="41000-104">\_Message FMEVENT TOOLBARLOAD</span><span class="sxs-lookup"><span data-stu-id="41000-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="41000-105">Envoyé à une DLL d’extension lorsque le gestionnaire de fichiers charge sa barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="41000-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="41000-106">Ce message permet à une DLL d’extension d’ajouter un bouton à la barre d’outils du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="41000-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="41000-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41000-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41000-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41000-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="41000-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="41000-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="41000-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="41000-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="41000-111">Adresse d’une structure [**FMS \_ TOOLBARLOAD**](fms-toolbarload.md) .</span><span class="sxs-lookup"><span data-stu-id="41000-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="41000-112">Si la DLL d’extension ajoute un bouton à la barre d’outils dans le gestionnaire de fichiers, la DLL doit remplir la structure avec des informations sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="41000-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41000-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41000-113">Return value</span></span>

<span data-ttu-id="41000-114">Une DLL d’extension doit retourner la **valeur true** pour ajouter le bouton à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="41000-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="41000-115">Si la DLL retourne la **valeur false**, le gestionnaire de fichiers n’ajoute pas le bouton.</span><span class="sxs-lookup"><span data-stu-id="41000-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="41000-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41000-116">Requirements</span></span>



| <span data-ttu-id="41000-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41000-117">Requirement</span></span> | <span data-ttu-id="41000-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="41000-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41000-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41000-119">Minimum supported client</span></span><br/> | <span data-ttu-id="41000-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41000-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="41000-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41000-121">Minimum supported server</span></span><br/> | <span data-ttu-id="41000-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41000-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="41000-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="41000-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="41000-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="41000-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41000-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41000-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41000-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="41000-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




