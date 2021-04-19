---
description: L’interface IScanProfileUI permet aux applications d’afficher une boîte de dialogue afin que les utilisateurs puissent créer, modifier et supprimer des profils de numérisation.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Interface IScanProfileUI (Scanprofileui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514226"
---
# <a name="iscanprofileui-interface"></a><span data-ttu-id="aee2b-103">Interface IScanProfileUI</span><span class="sxs-lookup"><span data-stu-id="aee2b-103">IScanProfileUI interface</span></span>

<span data-ttu-id="aee2b-104">L’interface **IScanProfileUI** permet aux applications d’afficher une boîte de dialogue afin que les utilisateurs puissent créer, modifier et supprimer des profils de numérisation.</span><span class="sxs-lookup"><span data-stu-id="aee2b-104">The **IScanProfileUI** interface enables applications to display a dialog box so that users can create, modify, and delete scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="aee2b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="aee2b-105">Members</span></span>

<span data-ttu-id="aee2b-106">L’interface **IScanProfileUI** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="aee2b-106">The **IScanProfileUI** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="aee2b-107">**IScanProfileUI** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aee2b-107">**IScanProfileUI** also has these types of members:</span></span>

-   [<span data-ttu-id="aee2b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aee2b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aee2b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aee2b-109">Methods</span></span>

<span data-ttu-id="aee2b-110">L’interface **IScanProfileUI** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="aee2b-110">The **IScanProfileUI** interface has these methods.</span></span>



| <span data-ttu-id="aee2b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="aee2b-111">Method</span></span>                                                             | <span data-ttu-id="aee2b-112">Description</span><span class="sxs-lookup"><span data-stu-id="aee2b-112">Description</span></span>                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aee2b-113">**ScanProfileDialog**</span><span class="sxs-lookup"><span data-stu-id="aee2b-113">**ScanProfileDialog**</span></span>](-wia-iscanprofileui-scanprofiledialog.md) | <span data-ttu-id="aee2b-114">Affiche une boîte de dialogue qui permet aux utilisateurs de créer, de modifier et de supprimer des profils de numérisation.</span><span class="sxs-lookup"><span data-stu-id="aee2b-114">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aee2b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="aee2b-115">Remarks</span></span>

<span data-ttu-id="aee2b-116">La boîte de dialogue est modale. l’utilisateur ne peut pas basculer vers la fenêtre parente tant que la boîte de dialogue n’est pas fermée.</span><span class="sxs-lookup"><span data-stu-id="aee2b-116">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee2b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aee2b-117">Requirements</span></span>



| <span data-ttu-id="aee2b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aee2b-118">Requirement</span></span> | <span data-ttu-id="aee2b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="aee2b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="aee2b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aee2b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aee2b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aee2b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="aee2b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aee2b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aee2b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aee2b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aee2b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="aee2b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee2b-125"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="aee2b-125"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="aee2b-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="aee2b-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aee2b-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aee2b-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee2b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aee2b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee2b-129">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="aee2b-129">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="aee2b-130">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="aee2b-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
