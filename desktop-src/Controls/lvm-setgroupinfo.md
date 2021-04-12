---
title: Message LVM_SETGROUPINFO (commctrl. h)
description: Définit les informations de groupe.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032350"
---
# <a name="lvm_setgroupinfo-message"></a><span data-ttu-id="f0055-104">\_Message SETGROUPINFO LVM</span><span class="sxs-lookup"><span data-stu-id="f0055-104">LVM\_SETGROUPINFO message</span></span>

<span data-ttu-id="f0055-105">Définit les informations de groupe.</span><span class="sxs-lookup"><span data-stu-id="f0055-105">Sets group information.</span></span> <span data-ttu-id="f0055-106">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) .</span><span class="sxs-lookup"><span data-stu-id="f0055-106">Send this message explicitly or by using the [**ListView\_SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0055-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0055-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0055-108">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0055-108">*wParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="f0055-109">ID qui spécifie le groupe dont les informations doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="f0055-109">ID that specifies the group whose information is to be set.</span></span></dd> <dt>

<span data-ttu-id="f0055-110">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0055-110">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="f0055-111">Pointeur vers une structure [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) qui contient les informations à définir.</span><span class="sxs-lookup"><span data-stu-id="f0055-111">Pointer to a [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0055-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0055-112">Return value</span></span>

<span data-ttu-id="f0055-113">Retourne l’ID du groupe en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f0055-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0055-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f0055-114">Remarks</span></span>

<span data-ttu-id="f0055-115">Pour modifier l’ID de groupe d’un groupe existant, ajoutez <b>LVGF_GROUPID</b> à <b>LVGROUP. Mask</b> et définissez <b>LVGROUP. iGroupId</b> sur le nouvel ID.</span><span class="sxs-lookup"><span data-stu-id="f0055-115">To change a group ID of an existing group add <b>LVGF_GROUPID</b> to <b>LVGROUP.mask</b> and set <b>LVGROUP.iGroupId</b> to the new ID.</span></span> <span data-ttu-id="f0055-116">L’appel échoue si <b>LVGROUP. iGroupId</b> contient l’ID d’un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="f0055-116">The call will fail if <b>LVGROUP.iGroupId</b> contains ID of an existing group.</span></span>

<span data-ttu-id="f0055-117">Pour mettre à jour d’autres propriétés d’un groupe existant (par exemple, mettre à jour un alignement du texte d’en-tête ou de pied de page pour le groupe, <b>uAlign</b>) <b>LVGROUP. Mask</b> ne doit pas contenir de <b>LVGF_GROUPID</b>, sinon la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="f0055-117">To update other properties of an existing group (e.g. update an alignment of the header or footer text for the group, <b>uAlign</b>) <b>LVGROUP.mask</b> must not contain <b>LVGF_GROUPID</b>, else the update will fail.</span></span>

> [!Note]  
> <span data-ttu-id="f0055-118">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="f0055-118">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f0055-119">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f0055-119">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0055-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0055-120">Requirements</span></span>



| <span data-ttu-id="f0055-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0055-121">Requirement</span></span> | <span data-ttu-id="f0055-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0055-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0055-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0055-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f0055-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0055-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0055-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0055-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f0055-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0055-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0055-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0055-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0055-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0055-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





