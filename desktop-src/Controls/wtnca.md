---
title: Valeurs WTNCA (uxtheme. h)
description: Spécifie les indicateurs qui modifient les attributs de style visuel de la fenêtre. Utilisez un ou une combinaison d’opérations de bits des valeurs suivantes.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaf543b688d0b403962da43029ac9aa85422bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105940"
---
# <a name="wtnca-values"></a><span data-ttu-id="489e1-104">Valeurs WTNCA</span><span class="sxs-lookup"><span data-stu-id="489e1-104">WTNCA Values</span></span>

<span data-ttu-id="489e1-105">Spécifie les indicateurs qui modifient les attributs de style visuel de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="489e1-105">Specifies flags that modify window visual style attributes.</span></span> <span data-ttu-id="489e1-106">Utilisez un ou une combinaison d’opérations de bits des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="489e1-106">Use one, or a bitwise combination of the following values.</span></span>



| <span data-ttu-id="489e1-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="489e1-107">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="489e1-108">Description</span><span class="sxs-lookup"><span data-stu-id="489e1-108">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <span data-ttu-id="489e1-109"><dt>**WTNCA \_ NODRAWCAPTION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="489e1-109"><dt>**WTNCA\_NODRAWCAPTION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="489e1-110">Empêche la légende de la fenêtre d’être dessinée.</span><span class="sxs-lookup"><span data-stu-id="489e1-110">Prevents the window caption from being drawn.</span></span><br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <span data-ttu-id="489e1-111"><dt>**WTNCA \_ NODRAWICON**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="489e1-111"><dt>**WTNCA\_NODRAWICON**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="489e1-112">Empêche le dessin de l’icône système.</span><span class="sxs-lookup"><span data-stu-id="489e1-112">Prevents the system icon from being drawn.</span></span><br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <span data-ttu-id="489e1-113"><dt>**WTNCA \_ NOSYSMENU**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="489e1-113"><dt>**WTNCA\_NOSYSMENU**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="489e1-114">Empêche l’affichage du menu de l’icône système.</span><span class="sxs-lookup"><span data-stu-id="489e1-114">Prevents the system icon menu from appearing.</span></span><br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <span data-ttu-id="489e1-115"><dt>**WTNCA \_ NOMIRRORHELP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="489e1-115"><dt>**WTNCA\_NOMIRRORHELP**</dt> <dt>0x00000008</dt></span></span> </dl>    | <span data-ttu-id="489e1-116">Empêche la mise en miroir du point d’interrogation, même dans une disposition de droite à gauche (RTL).</span><span class="sxs-lookup"><span data-stu-id="489e1-116">Prevents mirroring of the question mark, even in right-to-left (RTL) layout.</span></span><br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <span data-ttu-id="489e1-117"><dt>**WTNCA \_ VALIDBITS**</dt></span><span class="sxs-lookup"><span data-stu-id="489e1-117"><dt>**WTNCA\_VALIDBITS**</dt></span></span> </dl>                                                                             | <span data-ttu-id="489e1-118">Masque qui contient tous les bits valides.</span><span class="sxs-lookup"><span data-stu-id="489e1-118">A mask that contains all the valid bits.</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="489e1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="489e1-119">Requirements</span></span>



| <span data-ttu-id="489e1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="489e1-120">Requirement</span></span> | <span data-ttu-id="489e1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="489e1-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="489e1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="489e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="489e1-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="489e1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="489e1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="489e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="489e1-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="489e1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="489e1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="489e1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="489e1-127"><dt>Uxtheme. h</dt></span><span class="sxs-lookup"><span data-stu-id="489e1-127"><dt>Uxtheme.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489e1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="489e1-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="489e1-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="489e1-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="489e1-130">**OPTIONS de WTA \_**</span><span class="sxs-lookup"><span data-stu-id="489e1-130">**WTA\_OPTIONS**</span></span>](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[<span data-ttu-id="489e1-131">**SetWindowThemeNonClientAttributes**</span><span class="sxs-lookup"><span data-stu-id="489e1-131">**SetWindowThemeNonClientAttributes**</span></span>](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





