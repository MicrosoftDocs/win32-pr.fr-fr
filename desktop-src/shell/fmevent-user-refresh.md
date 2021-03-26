---
description: Envoyé à une DLL d’extension lorsque l’utilisateur choisit la commande Actualiser dans le menu Affichage du gestionnaire de fichiers. L’extension peut utiliser cette notification pour mettre à jour son menu.
title: Message FMEVENT_USER_REFRESH (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: c3c4596b0ea589545c6e59953b9c7b5977e07b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973223"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="11713-104">Message d’actualisation de l' \_ utilisateur FMEVENT \_</span><span class="sxs-lookup"><span data-stu-id="11713-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="11713-105">Envoyé à une DLL d’extension lorsque l’utilisateur choisit la commande **Actualiser** dans le menu **affichage** du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="11713-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="11713-106">L’extension peut utiliser cette notification pour mettre à jour son menu.</span><span class="sxs-lookup"><span data-stu-id="11713-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="11713-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11713-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11713-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11713-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="11713-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="11713-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="11713-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11713-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="11713-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="11713-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11713-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11713-112">Return value</span></span>

<span data-ttu-id="11713-113">Une DLL d’extension doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="11713-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="11713-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="11713-114">Requirements</span></span>



| <span data-ttu-id="11713-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11713-115">Requirement</span></span> | <span data-ttu-id="11713-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="11713-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11713-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11713-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11713-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11713-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="11713-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11713-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11713-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11713-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="11713-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="11713-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="11713-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="11713-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11713-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11713-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11713-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="11713-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




