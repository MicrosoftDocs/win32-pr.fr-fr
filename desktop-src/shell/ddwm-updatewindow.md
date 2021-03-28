---
description: Indique à une fenêtre d’image de dépôt d’effectuer la mise à jour à l’aide des nouvelles informations DROPDESCRIPTION.
title: Message DDWM_UPDATEWINDOW
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972027"
---
# <a name="ddwm_updatewindow-message"></a><span data-ttu-id="45f4f-103">\_Message DDWM UPDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="45f4f-103">DDWM\_UPDATEWINDOW message</span></span>

<span data-ttu-id="45f4f-104">Indique à une fenêtre d’image de dépôt d’effectuer la mise à jour à l’aide des nouvelles informations [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .</span><span class="sxs-lookup"><span data-stu-id="45f4f-104">Instructs a drop image window to update using new [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) information.</span></span>

## <a name="parameters"></a><span data-ttu-id="45f4f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45f4f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f4f-106">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45f4f-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f4f-107">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="45f4f-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="45f4f-108">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45f4f-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f4f-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="45f4f-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45f4f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="45f4f-110">Remarks</span></span>

<span data-ttu-id="45f4f-111">DDWM \_ UPDATEWINDOW est défini en tant qu' \_ utilisateur WM + 3.</span><span class="sxs-lookup"><span data-stu-id="45f4f-111">DDWM\_UPDATEWINDOW is defined as WM\_USER+3.</span></span>

<span data-ttu-id="45f4f-112">Lorsque l’état d’une opération de suppression change (par exemple, en réponse à une touche de modification)[**IDropTarget ::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) retourne une nouvelle valeur [**DROPEFFECT**](../com/dropeffect-constants.md) (cette valeur **DROPEFFECT** peut également être reçue via [**IDropSource :: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span><span class="sxs-lookup"><span data-stu-id="45f4f-112">When the state of a drop operation changes—such as in response to a modifier key—[**IDropTarget::DragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) returns a new [**DROPEFFECT**](../com/dropeffect-constants.md) value (this **DROPEFFECT** value can also be received through [**IDropSource::GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span></span> <span data-ttu-id="45f4f-113">En réponse, l’application met à jour la structure [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) de la cible de déplacement avec une nouvelle valeur [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) qui indique la décoration à appliquer au visuel de la fenêtre de glissement. par exemple, une indication que le fichier est copié plutôt que déplacé ou que l’objet ne peut pas être supprimé à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="45f4f-113">In response, the application updates the drop target's [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) structure with a new [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) value that indicates the decoration to be applied to the drag window's visual; for instance, an indication that the file is being copied rather than moved or that the object cannot be dropped to that location.</span></span> <span data-ttu-id="45f4f-114">Toutefois, les éléments visuels ne sont pas mis à jour tant que l’objet n’a pas reçu un message **DDWM \_ UPDATEWINDOW** .</span><span class="sxs-lookup"><span data-stu-id="45f4f-114">However, the visuals are not updated until the object receives a **DDWM\_UPDATEWINDOW** message.</span></span>

<span data-ttu-id="45f4f-115">Le format de presse-papiers [DragWindow](clipboard.md) fournit le **HWND** de la fenêtre de glissement du destinataire à l’expéditeur du message **DDWM \_ UPDATEWINDOW** .</span><span class="sxs-lookup"><span data-stu-id="45f4f-115">The [DragWindow](clipboard.md) clipboard format provides the **HWND** of the recipient drag window to the sender of the **DDWM\_UPDATEWINDOW** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="45f4f-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="45f4f-116">Requirements</span></span>



| <span data-ttu-id="45f4f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45f4f-117">Requirement</span></span> | <span data-ttu-id="45f4f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="45f4f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45f4f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45f4f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="45f4f-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45f4f-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="45f4f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45f4f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="45f4f-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45f4f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
