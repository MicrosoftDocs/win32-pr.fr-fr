---
title: UI_ALL_COMMANDS (UIRibbon. h)
description: Spécifie une constante qui identifie la collection de commandes déclarée dans le fichier de ressources de balisage.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce287d6ee03734ecbb0dd84e020ec542a83f04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511936"
---
# <a name="ui_all_commands"></a><span data-ttu-id="50fe2-103">interface utilisateur \_ toutes les \_ commandes</span><span class="sxs-lookup"><span data-stu-id="50fe2-103">UI\_ALL\_COMMANDS</span></span>

<span data-ttu-id="50fe2-104">Spécifie une constante qui identifie la collection de commandes déclarée dans le fichier de ressources de balisage.</span><span class="sxs-lookup"><span data-stu-id="50fe2-104">Specifies a constant that identifies the collection of Commands declared in the Markup resource file.</span></span>

## <a name="remarks"></a><span data-ttu-id="50fe2-105">Notes</span><span class="sxs-lookup"><span data-stu-id="50fe2-105">Remarks</span></span>

<span data-ttu-id="50fe2-106">**Interface utilisateur \_ Toutes les \_ commandes** sont utiles lorsqu’il est nécessaire d’accéder à des propriétés similaires dans toutes les commandes.</span><span class="sxs-lookup"><span data-stu-id="50fe2-106">**UI\_ALL\_COMMANDS** is useful when it is necessary to access similar properties across all Commands.</span></span> <span data-ttu-id="50fe2-107">Par exemple, **l’interface utilisateur \_ peut être \_** passée à [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) pour invalider et actualiser toutes les commandes de ruban en interrogeant l’application hôte à la recherche de nouvelles valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="50fe2-107">For example, **UI\_ALL\_COMMANDS** can be passed to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) to invalidate and refresh all Ribbon Commands by querying the host application for new property values.</span></span>

## <a name="requirements"></a><span data-ttu-id="50fe2-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50fe2-108">Requirements</span></span>



| <span data-ttu-id="50fe2-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50fe2-109">Requirement</span></span> | <span data-ttu-id="50fe2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="50fe2-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50fe2-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50fe2-111">Minimum supported client</span></span><br/> | <span data-ttu-id="50fe2-112">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50fe2-112">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="50fe2-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50fe2-113">Minimum supported server</span></span><br/> | <span data-ttu-id="50fe2-114">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de plateforme pour les applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50fe2-114">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="50fe2-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="50fe2-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="50fe2-116"><dt>UIRibbon. h</dt></span><span class="sxs-lookup"><span data-stu-id="50fe2-116"><dt>Uiribbon.h</dt></span></span> </dl>                                             |
| <span data-ttu-id="50fe2-117">MIDL</span><span class="sxs-lookup"><span data-stu-id="50fe2-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50fe2-118"><dt>UIRibbon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50fe2-118"><dt>Uiribbon.idl</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="50fe2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50fe2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50fe2-120">Constantes et énumérations</span><span class="sxs-lookup"><span data-stu-id="50fe2-120">Constants and Enumerations</span></span>](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

