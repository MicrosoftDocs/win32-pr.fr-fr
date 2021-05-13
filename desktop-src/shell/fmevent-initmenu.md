---
description: Envoyé à une DLL d’extension lorsque l’utilisateur sélectionne le menu de l’extension à partir de la barre de menus du gestionnaire de fichiers. L’extension peut utiliser cette notification pour initialiser les éléments de menu.
title: Message FMEVENT_INITMENU (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 82ec9130a681bdfd36ff6259392c0608e4cde9cf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842280"
---
# <a name="fmevent_initmenu-message"></a><span data-ttu-id="89463-104">\_Message FMEVENT INITMENU</span><span class="sxs-lookup"><span data-stu-id="89463-104">FMEVENT\_INITMENU message</span></span>

<span data-ttu-id="89463-105">Envoyé à une DLL d’extension lorsque l’utilisateur sélectionne le menu de l’extension à partir de la barre de menus du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="89463-105">Sent to an extension DLL when the user selects the menu for the extension from the File Manager menu bar.</span></span> <span data-ttu-id="89463-106">L’extension peut utiliser cette notification pour initialiser les éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="89463-106">The extension can use this notification to initialize menu items.</span></span>

## <a name="parameters"></a><span data-ttu-id="89463-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89463-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89463-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89463-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="89463-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="89463-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="89463-110">*HMENU*</span><span class="sxs-lookup"><span data-stu-id="89463-110">*hmenu*</span></span> 
</dt> <dd>

<span data-ttu-id="89463-111">Handle vers la barre de menus du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="89463-111">A handle to the File Manager menu bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89463-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89463-112">Return value</span></span>

<span data-ttu-id="89463-113">Une DLL d’extension doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="89463-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="89463-114">Notes</span><span class="sxs-lookup"><span data-stu-id="89463-114">Remarks</span></span>

<span data-ttu-id="89463-115">Une DLL d’extension reçoit ce message uniquement lorsque l’utilisateur sélectionne le menu de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="89463-115">An extension DLL receives this message only when the user selects the top-level menu.</span></span> <span data-ttu-id="89463-116">Si l’extension contient des sous-menus, elle doit être initialisée en même temps qu’elle Initialise le menu de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="89463-116">If the extension contains submenus, it must initialize them at the same time it initializes the top-level menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="89463-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="89463-117">Requirements</span></span>



| <span data-ttu-id="89463-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89463-118">Requirement</span></span> | <span data-ttu-id="89463-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="89463-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89463-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89463-120">Minimum supported client</span></span><br/> | <span data-ttu-id="89463-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89463-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="89463-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89463-122">Minimum supported server</span></span><br/> | <span data-ttu-id="89463-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89463-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89463-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="89463-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="89463-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="89463-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89463-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89463-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89463-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="89463-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




