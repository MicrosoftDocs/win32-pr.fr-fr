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
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202792"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="bb245-104">\_Message FMEVENT TOOLBARLOAD</span><span class="sxs-lookup"><span data-stu-id="bb245-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="bb245-105">Envoyé à une DLL d’extension lorsque le gestionnaire de fichiers charge sa barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="bb245-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="bb245-106">Ce message permet à une DLL d’extension d’ajouter un bouton à la barre d’outils du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="bb245-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb245-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb245-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb245-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb245-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bb245-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bb245-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bb245-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="bb245-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="bb245-111">Adresse d’une structure [**FMS \_ TOOLBARLOAD**](fms-toolbarload.md) .</span><span class="sxs-lookup"><span data-stu-id="bb245-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="bb245-112">Si la DLL d’extension ajoute un bouton à la barre d’outils dans le gestionnaire de fichiers, la DLL doit remplir la structure avec des informations sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="bb245-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb245-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb245-113">Return value</span></span>

<span data-ttu-id="bb245-114">Une DLL d’extension doit retourner la **valeur true** pour ajouter le bouton à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="bb245-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="bb245-115">Si la DLL retourne la **valeur false**, le gestionnaire de fichiers n’ajoute pas le bouton.</span><span class="sxs-lookup"><span data-stu-id="bb245-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb245-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bb245-116">Requirements</span></span>



| <span data-ttu-id="bb245-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb245-117">Requirement</span></span> | <span data-ttu-id="bb245-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb245-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb245-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb245-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb245-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb245-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bb245-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb245-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb245-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb245-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb245-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb245-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb245-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb245-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb245-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb245-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb245-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="bb245-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




