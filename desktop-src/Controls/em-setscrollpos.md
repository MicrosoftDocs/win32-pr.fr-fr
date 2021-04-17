---
title: Message EM_SETSCROLLPOS (RichEdit. h)
description: Fait défiler le contenu d’un contrôle Rich Edit jusqu’au point spécifié.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466535"
---
# <a name="em_setscrollpos-message"></a><span data-ttu-id="67e17-104">\_Message SETSCROLLPOS em</span><span class="sxs-lookup"><span data-stu-id="67e17-104">EM\_SETSCROLLPOS message</span></span>

<span data-ttu-id="67e17-105">Fait défiler le contenu d’un contrôle Rich Edit jusqu’au point spécifié.</span><span class="sxs-lookup"><span data-stu-id="67e17-105">Scrolls the contents of a rich edit control to the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="67e17-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67e17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67e17-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67e17-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67e17-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="67e17-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="67e17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67e17-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67e17-110">Pointeur vers une structure de [**point**](/previous-versions//dd162805(v=vs.85)) qui spécifie un point dans l’espace du texte virtuel du document, exprimé en pixels.</span><span class="sxs-lookup"><span data-stu-id="67e17-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure which specifies a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="67e17-111">Le document est défilant jusqu’à ce que ce point se trouve dans l’angle supérieur gauche de la fenêtre de contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="67e17-111">The document will be scrolled until this point is located in the upper-left corner of the edit control window.</span></span> <span data-ttu-id="67e17-112">Si vous souhaitez modifier l’affichage de manière à ce que l’angle supérieur gauche de la vue comporte deux lignes et un caractère dans le bord gauche.</span><span class="sxs-lookup"><span data-stu-id="67e17-112">If you want to change the view such that the upper left corner of the view is two lines down and one character in from the left edge.</span></span> <span data-ttu-id="67e17-113">Vous devez passer un point de (7, 22).</span><span class="sxs-lookup"><span data-stu-id="67e17-113">You would pass a point of (7, 22).</span></span>

<span data-ttu-id="67e17-114">Le contrôle RichEdit vérifie les coordonnées x et y et les ajuste si nécessaire, afin qu’une ligne complète s’affiche en haut.</span><span class="sxs-lookup"><span data-stu-id="67e17-114">The rich edit control checks the x and y coordinates and adjusts them if necessary, so that a complete line is displayed at the top.</span></span> <span data-ttu-id="67e17-115">Elle garantit également que le texte n’est jamais complètement défilant du rectangle d’affichage.</span><span class="sxs-lookup"><span data-stu-id="67e17-115">It also ensures that the text is never completely scrolled off the view rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67e17-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67e17-116">Return value</span></span>

<span data-ttu-id="67e17-117">Ce message retourne toujours la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="67e17-117">This message always returns 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="67e17-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67e17-118">Requirements</span></span>



| <span data-ttu-id="67e17-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67e17-119">Requirement</span></span> | <span data-ttu-id="67e17-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="67e17-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67e17-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67e17-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67e17-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67e17-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67e17-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67e17-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67e17-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67e17-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67e17-125">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="67e17-125">Redistributable</span></span><br/>          | <span data-ttu-id="67e17-126">Édition enrichie 3,0</span><span class="sxs-lookup"><span data-stu-id="67e17-126">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="67e17-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="67e17-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="67e17-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="67e17-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67e17-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67e17-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e17-130">**\_GETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="67e17-130">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> </dl>

 

