---
title: Message CBEM_SETIMAGELIST (commctrl. h)
description: Définit une liste d’images pour un contrôle ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942769"
---
# <a name="cbem_setimagelist-message"></a><span data-ttu-id="8f2ea-104">\_Message CBEM SETIMAGELIST</span><span class="sxs-lookup"><span data-stu-id="8f2ea-104">CBEM\_SETIMAGELIST message</span></span>

<span data-ttu-id="8f2ea-105">Définit une liste d’images pour un contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-105">Sets an image list for a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f2ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f2ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f2ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f2ea-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8f2ea-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8f2ea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f2ea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f2ea-110">Handle de la liste d’images à définir pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-110">A handle to the image list to be set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f2ea-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f2ea-111">Return value</span></span>

<span data-ttu-id="8f2ea-112">Retourne le handle de la liste d’images précédemment associée au contrôle, ou retourne la **valeur null** si aucune liste d’images n’a été définie précédemment.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-112">Returns the handle to the image list previously associated with the control, or returns **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f2ea-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8f2ea-113">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f2ea-114">La hauteur des images de votre liste d’images peut modifier les exigences de taille du contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-114">The height of images in your image list might change the size requirements of the ComboBoxEx control.</span></span> <span data-ttu-id="8f2ea-115">Il est recommandé de redimensionner le contrôle après l’envoi de ce message pour vous assurer qu’il s’affiche correctement.</span><span class="sxs-lookup"><span data-stu-id="8f2ea-115">It is recommended that you resize the control after sending this message to ensure that it is displayed properly.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8f2ea-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f2ea-116">Requirements</span></span>



| <span data-ttu-id="8f2ea-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f2ea-117">Requirement</span></span> | <span data-ttu-id="8f2ea-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2ea-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2ea-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f2ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8f2ea-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f2ea-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f2ea-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f2ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8f2ea-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f2ea-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f2ea-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f2ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f2ea-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ea-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





