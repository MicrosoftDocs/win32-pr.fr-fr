---
title: Autres rôles d’objet et méthodes prises en charge (référence des éléments d’interface utilisateur MSAA)
description: Cette rubrique fournit des informations sur les rôles d’objet qui ne sont pas inclus dans les rubriques précédentes relatives aux éléments d’interface utilisateur.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729028"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="fdb66-103">Autres rôles d’objet et méthodes prises en charge (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="fdb66-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="fdb66-104">Cette rubrique fournit des informations sur les rôles d’objet qui ne sont pas inclus dans les rubriques précédentes relatives aux éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fdb66-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="fdb66-105">Chaque rôle d’objet comprend une liste des méthodes et des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) prises en charge pour le rôle d’objet.</span><span class="sxs-lookup"><span data-stu-id="fdb66-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="fdb66-106">Tandis que d’autres rubriques documentées ont pris en charge les méthodes et propriétés **IAccessible** pour les éléments d’interface utilisateur, cette rubrique répertorie les méthodes et les propriétés que vous pouvez vous attendre à prendre en charge pour un rôle d’objet particulier.</span><span class="sxs-lookup"><span data-stu-id="fdb66-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="fdb66-107">La plupart des éléments d’interface utilisateur qui peuvent avoir l’un des rôles répertoriés ici sont généralement affichés dans les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="fdb66-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="fdb66-108">Utilisez cette rubrique comme indication.</span><span class="sxs-lookup"><span data-stu-id="fdb66-108">Use this topic as a guideline.</span></span> <span data-ttu-id="fdb66-109">Nous vous suggérons vivement d’utiliser les outils de Active Accessibility Microsoft pour vérifier le comportement attendu pour un rôle d’objet individuel.</span><span class="sxs-lookup"><span data-stu-id="fdb66-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="fdb66-110">Le tableau suivant répertorie les rôles d’objet supplémentaires que Oleacc.dll prend en charge.</span><span class="sxs-lookup"><span data-stu-id="fdb66-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="fdb66-111">**\_alerte du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="fdb66-112">**déroulant système de rôle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="fdb66-113">**\_application de système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="fdb66-114">**\_équation du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="fdb66-115">**\_bordure du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="fdb66-116">**\_graphique du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="fdb66-117">**système de rôle \_ \_ BUTTONDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="fdb66-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="fdb66-118">**système de rôle \_ \_ HELPBALLOON**</span><span class="sxs-lookup"><span data-stu-id="fdb66-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="fdb66-119">**système de rôle \_ \_ BUTTONDROPDOWNGRID**</span><span class="sxs-lookup"><span data-stu-id="fdb66-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="fdb66-120">**\_adresse IP du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="fdb66-121">**système de rôle \_ \_ BUTTONMENU**</span><span class="sxs-lookup"><span data-stu-id="fdb66-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="fdb66-122">**\_lien système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="fdb66-123">**\_cellule système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="fdb66-124">**\_volet système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="fdb66-125">**\_caractère système du rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="fdb66-126">**\_ligne du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="fdb66-127">**\_graphique de système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="fdb66-128">**système de rôle \_ \_ ROWHEADER**</span><span class="sxs-lookup"><span data-stu-id="fdb66-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="fdb66-129">**\_horloge système du rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="fdb66-130">**\_séparateur système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="fdb66-131">**\_colonne système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="fdb66-132">**\_son du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="fdb66-133">**\_diagramme du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="fdb66-134">**système de rôle \_ \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="fdb66-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="fdb66-135">**\_numérotation du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="fdb66-136">**\_table système des rôles \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="fdb66-137">**\_document système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="fdb66-138">**\_espace blanc du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="fdb66-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="fdb66-139">\_alerte du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="fdb66-140">Pour plus d’informations sur ce rôle, [**consultez \_ \_ alerte du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-141">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-142">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-142">get\_accName</span></span>
-   <span data-ttu-id="fdb66-143">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-143">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-144">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="fdb66-145">\_application de système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="fdb66-146">Pour plus d’informations sur ce rôle, consultez rôle de l' [**\_ \_ application système**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-147">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-148">accHitTest</span></span>
-   <span data-ttu-id="fdb66-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-149">accLocation</span></span>
-   <span data-ttu-id="fdb66-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-150">accNavigate</span></span>
-   <span data-ttu-id="fdb66-151">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-151">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-152">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-152">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-153">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-153">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-154">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-154">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-155">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-156">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-157">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-157">get\_accName</span></span>
-   <span data-ttu-id="fdb66-158">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-158">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-159">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-159">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-160">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="fdb66-161">\_bordure du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="fdb66-162">Pour plus d’informations sur ce rôle, consultez la rubrique [**\_ \_ bordure du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-163">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-164">accHitTest</span></span>
-   <span data-ttu-id="fdb66-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-165">accLocation</span></span>
-   <span data-ttu-id="fdb66-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-166">accNavigate</span></span>
-   <span data-ttu-id="fdb66-167">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-167">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-168">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="fdb66-169">système de rôle \_ \_ BUTTONDROPDOWN</span><span class="sxs-lookup"><span data-stu-id="fdb66-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="fdb66-170">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ BUTTONDROPDOWN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-171">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="fdb66-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-173">accHitTest</span></span>
-   <span data-ttu-id="fdb66-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-174">accLocation</span></span>
-   <span data-ttu-id="fdb66-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-175">accNavigate</span></span>
-   <span data-ttu-id="fdb66-176">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-176">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-177">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-177">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-178">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="fdb66-179">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-179">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-180">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-180">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-181">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-182">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-183">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-183">get\_accName</span></span>
-   <span data-ttu-id="fdb66-184">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-184">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-185">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-185">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-186">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="fdb66-187">système de rôle \_ \_ BUTTONDROPDOWNGRID</span><span class="sxs-lookup"><span data-stu-id="fdb66-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="fdb66-188">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ BUTTONDROPDOWNGRID**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-189">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="fdb66-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-191">accHitTest</span></span>
-   <span data-ttu-id="fdb66-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-192">accLocation</span></span>
-   <span data-ttu-id="fdb66-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-193">accNavigate</span></span>
-   <span data-ttu-id="fdb66-194">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-194">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-195">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-195">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-196">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="fdb66-197">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-197">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-198">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-198">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-199">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-200">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-201">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-201">get\_accName</span></span>
-   <span data-ttu-id="fdb66-202">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-202">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-203">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-203">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-204">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="fdb66-205">système de rôle \_ \_ BUTTONMENU</span><span class="sxs-lookup"><span data-stu-id="fdb66-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="fdb66-206">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ BUTTONMENU**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-207">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="fdb66-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-209">accHitTest</span></span>
-   <span data-ttu-id="fdb66-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-210">accLocation</span></span>
-   <span data-ttu-id="fdb66-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-211">accNavigate</span></span>
-   <span data-ttu-id="fdb66-212">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="fdb66-213">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-213">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-214">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-214">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-215">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-216">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-217">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-217">get\_accName</span></span>
-   <span data-ttu-id="fdb66-218">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-218">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-219">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-219">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-220">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="fdb66-221">\_cellule système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="fdb66-222">Pour plus d’informations sur ce rôle, consultez la rubrique [**\_ \_ cellule système Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-223">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-224">accHitTest</span></span>
-   <span data-ttu-id="fdb66-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-225">accLocation</span></span>
-   <span data-ttu-id="fdb66-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-226">accNavigate</span></span>
-   <span data-ttu-id="fdb66-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="fdb66-227">accSelect</span></span>
-   <span data-ttu-id="fdb66-228">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-228">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-229">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-229">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-230">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-230">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-231">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-231">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-232">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-233">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-234">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-234">get\_accName</span></span>
-   <span data-ttu-id="fdb66-235">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-235">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-236">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-236">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-237">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-237">get\_accState</span></span>
-   <span data-ttu-id="fdb66-238">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="fdb66-239">\_caractère système du rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="fdb66-240">Pour plus d’informations sur ce rôle, [**consultez \_ \_ caractère système du rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-241">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-242">accHitTest</span></span>
-   <span data-ttu-id="fdb66-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-243">accLocation</span></span>
-   <span data-ttu-id="fdb66-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-244">accNavigate</span></span>
-   <span data-ttu-id="fdb66-245">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="fdb66-245">get\_accDescription</span></span>
-   <span data-ttu-id="fdb66-246">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-246">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-247">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-248">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-248">get\_accName</span></span>
-   <span data-ttu-id="fdb66-249">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-249">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-250">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-250">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-251">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-251">get\_accState</span></span>
-   <span data-ttu-id="fdb66-252">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="fdb66-253">\_graphique de système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="fdb66-254">Pour plus d’informations sur ce rôle, consultez la rubrique [**\_ \_ graphique de système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-255">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-256">accHitTest</span></span>
-   <span data-ttu-id="fdb66-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-257">accLocation</span></span>
-   <span data-ttu-id="fdb66-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-258">accNavigate</span></span>
-   <span data-ttu-id="fdb66-259">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-259">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-260">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-260">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-261">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-261">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-262">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-262">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-263">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-264">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-265">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-265">get\_accName</span></span>
-   <span data-ttu-id="fdb66-266">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-266">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-267">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-267">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-268">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="fdb66-269">\_horloge système du rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="fdb66-270">Pour plus d’informations sur ce rôle, [**consultez \_ \_ horloge du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-271">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-272">accHitTest</span></span>
-   <span data-ttu-id="fdb66-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-273">accLocation</span></span>
-   <span data-ttu-id="fdb66-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-274">accNavigate</span></span>
-   <span data-ttu-id="fdb66-275">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-275">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-276">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-276">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-277">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-278">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-279">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-279">get\_accName</span></span>
-   <span data-ttu-id="fdb66-280">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-280">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-281">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-281">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-282">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-282">get\_accState</span></span>
-   <span data-ttu-id="fdb66-283">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="fdb66-284">\_colonne système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="fdb66-285">Pour plus d’informations sur ce rôle, [**consultez \_ \_ colonne système Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-286">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-287">accHitTest</span></span>
-   <span data-ttu-id="fdb66-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-288">accLocation</span></span>
-   <span data-ttu-id="fdb66-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-289">accNavigate</span></span>
-   <span data-ttu-id="fdb66-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="fdb66-290">accSelect</span></span>
-   <span data-ttu-id="fdb66-291">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-291">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-292">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-292">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-293">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-293">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-294">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-294">get\_accName</span></span>
-   <span data-ttu-id="fdb66-295">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-295">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-296">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-296">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-297">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-297">get\_accState</span></span>
-   <span data-ttu-id="fdb66-298">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="fdb66-299">\_diagramme du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="fdb66-300">Pour plus d’informations sur ce rôle, [**consultez \_ \_ diagramme du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-301">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-302">accHitTest</span></span>
-   <span data-ttu-id="fdb66-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-303">accLocation</span></span>
-   <span data-ttu-id="fdb66-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-304">accNavigate</span></span>
-   <span data-ttu-id="fdb66-305">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-305">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-306">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-306">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-307">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-307">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-308">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-308">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-309">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-310">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-311">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-311">get\_accName</span></span>
-   <span data-ttu-id="fdb66-312">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-312">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-313">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-313">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-314">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="fdb66-315">\_numérotation du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="fdb66-316">Pour plus d’informations sur ce rôle, consultez la page [**\_ \_ accès au système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-317">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="fdb66-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-319">accHitTest</span></span>
-   <span data-ttu-id="fdb66-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-320">accLocation</span></span>
-   <span data-ttu-id="fdb66-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-321">accNavigate</span></span>
-   <span data-ttu-id="fdb66-322">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="fdb66-323">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-323">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-324">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-324">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-325">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-326">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-327">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-327">get\_accName</span></span>
-   <span data-ttu-id="fdb66-328">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-328">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-329">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-329">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-330">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-330">get\_accState</span></span>
-   <span data-ttu-id="fdb66-331">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="fdb66-332">\_document système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="fdb66-333">Pour plus d’informations sur ce rôle, [**consultez \_ \_ document de système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-334">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-335">accHitTest</span></span>
-   <span data-ttu-id="fdb66-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-336">accLocation</span></span>
-   <span data-ttu-id="fdb66-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-337">accNavigate</span></span>
-   <span data-ttu-id="fdb66-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="fdb66-338">accSelect</span></span>
-   <span data-ttu-id="fdb66-339">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-339">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-340">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-340">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-341">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-341">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-342">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-342">get\_accName</span></span>
-   <span data-ttu-id="fdb66-343">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-343">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-344">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-344">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-345">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="fdb66-346">déroulant système de rôle \_ \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="fdb66-347">Pour plus d’informations sur ce rôle, consultez la page [**\_ \_ déroulante système de rôles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-348">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="fdb66-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-350">accHitTest</span></span>
-   <span data-ttu-id="fdb66-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-351">accLocation</span></span>
-   <span data-ttu-id="fdb66-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-352">accNavigate</span></span>
-   <span data-ttu-id="fdb66-353">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-353">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-354">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-354">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-355">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="fdb66-356">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-356">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-357">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-357">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-358">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-359">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-360">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-360">get\_accName</span></span>
-   <span data-ttu-id="fdb66-361">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-361">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-362">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-362">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-363">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="fdb66-364">\_équation du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="fdb66-365">Pour plus d’informations sur ce rôle, [**consultez \_ \_ équation du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-366">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-367">accHitTest</span></span>
-   <span data-ttu-id="fdb66-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-368">accLocation</span></span>
-   <span data-ttu-id="fdb66-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-369">accNavigate</span></span>
-   <span data-ttu-id="fdb66-370">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-370">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-371">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-371">get\_accName</span></span>
-   <span data-ttu-id="fdb66-372">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-372">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-373">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-373">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-374">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-374">get\_accState</span></span>
-   <span data-ttu-id="fdb66-375">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="fdb66-376">\_graphique du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="fdb66-377">Pour plus d’informations sur ce rôle, [**consultez \_ \_ graphique du système de rôles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-378">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-379">accHitTest</span></span>
-   <span data-ttu-id="fdb66-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-380">accLocation</span></span>
-   <span data-ttu-id="fdb66-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-381">accNavigate</span></span>
-   <span data-ttu-id="fdb66-382">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-382">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-383">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-383">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-384">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-385">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-386">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-386">get\_accName</span></span>
-   <span data-ttu-id="fdb66-387">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-387">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-388">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-388">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-389">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="fdb66-390">système de rôle \_ \_ HELPBALLOON</span><span class="sxs-lookup"><span data-stu-id="fdb66-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="fdb66-391">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ HELPBALLOON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-392">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-393">accHitTest</span></span>
-   <span data-ttu-id="fdb66-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-394">accLocation</span></span>
-   <span data-ttu-id="fdb66-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-395">accNavigate</span></span>
-   <span data-ttu-id="fdb66-396">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-396">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-397">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-397">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-398">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="fdb66-399">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-399">get\_accName</span></span>
-   <span data-ttu-id="fdb66-400">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-400">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-401">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-401">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-402">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-402">get\_accState</span></span>
-   <span data-ttu-id="fdb66-403">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="fdb66-404">\_adresse IP du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="fdb66-405">Pour plus d’informations sur ce rôle, [**consultez \_ \_ adresse IP du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-406">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-407">accHitTest</span></span>
-   <span data-ttu-id="fdb66-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-408">accLocation</span></span>
-   <span data-ttu-id="fdb66-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-409">accNavigate</span></span>
-   <span data-ttu-id="fdb66-410">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-410">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-411">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-411">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-412">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-412">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-413">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-413">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-414">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-415">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-416">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-416">get\_accName</span></span>
-   <span data-ttu-id="fdb66-417">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-417">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-418">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-418">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-419">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-419">get\_accState</span></span>
-   <span data-ttu-id="fdb66-420">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="fdb66-421">\_lien système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="fdb66-422">Pour plus d’informations sur ce rôle, [**consultez \_ \_ lien système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-423">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="fdb66-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-425">accHitTest</span></span>
-   <span data-ttu-id="fdb66-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-426">accLocation</span></span>
-   <span data-ttu-id="fdb66-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-427">accNavigate</span></span>
-   <span data-ttu-id="fdb66-428">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-428">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-429">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-429">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-430">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="fdb66-431">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="fdb66-431">get\_accDescription</span></span>
-   <span data-ttu-id="fdb66-432">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-432">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-433">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-434">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-434">get\_accName</span></span>
-   <span data-ttu-id="fdb66-435">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-435">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-436">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-436">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-437">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-437">get\_accState</span></span>
-   <span data-ttu-id="fdb66-438">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="fdb66-439">\_volet système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="fdb66-440">Pour plus d’informations sur ce rôle, [**consultez \_ \_ volet système de rôles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-441">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-442">accHitTest</span></span>
-   <span data-ttu-id="fdb66-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-443">accLocation</span></span>
-   <span data-ttu-id="fdb66-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-444">accNavigate</span></span>
-   <span data-ttu-id="fdb66-445">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-445">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-446">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-446">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-447">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-447">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-448">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-448">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-449">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-450">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-451">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-451">get\_accName</span></span>
-   <span data-ttu-id="fdb66-452">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-452">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-453">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-453">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-454">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="fdb66-455">\_ligne du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="fdb66-456">Pour plus d’informations sur ce rôle, consultez rôle de la [**\_ \_ ligne système**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-457">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-458">accHitTest</span></span>
-   <span data-ttu-id="fdb66-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-459">accLocation</span></span>
-   <span data-ttu-id="fdb66-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-460">accNavigate</span></span>
-   <span data-ttu-id="fdb66-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="fdb66-461">accSelect</span></span>
-   <span data-ttu-id="fdb66-462">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-462">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-463">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-463">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-464">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="fdb66-464">get\_accDescription</span></span>
-   <span data-ttu-id="fdb66-465">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-465">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-466">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-466">get\_accName</span></span>
-   <span data-ttu-id="fdb66-467">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-467">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-468">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-468">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-469">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-469">get\_accState</span></span>
-   <span data-ttu-id="fdb66-470">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="fdb66-471">système de rôle \_ \_ ROWHEADER</span><span class="sxs-lookup"><span data-stu-id="fdb66-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="fdb66-472">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ ROWHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-473">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-474">accHitTest</span></span>
-   <span data-ttu-id="fdb66-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-475">accLocation</span></span>
-   <span data-ttu-id="fdb66-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-476">accNavigate</span></span>
-   <span data-ttu-id="fdb66-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="fdb66-477">accSelect</span></span>
-   <span data-ttu-id="fdb66-478">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-478">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-479">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-479">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-480">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="fdb66-481">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="fdb66-481">get\_accDescription</span></span>
-   <span data-ttu-id="fdb66-482">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-482">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-483">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-483">get\_accName</span></span>
-   <span data-ttu-id="fdb66-484">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-484">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-485">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-485">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-486">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-486">get\_accState</span></span>
-   <span data-ttu-id="fdb66-487">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="fdb66-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="fdb66-488">\_séparateur système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="fdb66-489">Pour plus d’informations sur ce rôle, [**consultez \_ \_ séparateur de système de rôles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-490">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-491">accHitTest</span></span>
-   <span data-ttu-id="fdb66-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-492">accLocation</span></span>
-   <span data-ttu-id="fdb66-493">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-493">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-494">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-494">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-495">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-495">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-496">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-496">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-497">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="fdb66-498">\_son du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="fdb66-499">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ audio**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-500">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-501">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="fdb66-501">get\_accDescription</span></span>
-   <span data-ttu-id="fdb66-502">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-502">get\_accName</span></span>
-   <span data-ttu-id="fdb66-503">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-503">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-504">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="fdb66-505">système de rôle \_ \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="fdb66-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="fdb66-506">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-507">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="fdb66-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-509">accHitTest</span></span>
-   <span data-ttu-id="fdb66-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-510">accLocation</span></span>
-   <span data-ttu-id="fdb66-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-511">accNavigate</span></span>
-   <span data-ttu-id="fdb66-512">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="fdb66-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="fdb66-513">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-513">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-514">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-515">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-516">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-516">get\_accName</span></span>
-   <span data-ttu-id="fdb66-517">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-517">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-518">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-518">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-519">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="fdb66-520">\_table système des rôles \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="fdb66-521">Pour plus d’informations sur ce rôle, [**consultez \_ \_ table système Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-522">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="fdb66-523">accHitTest</span></span>
-   <span data-ttu-id="fdb66-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-524">accLocation</span></span>
-   <span data-ttu-id="fdb66-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="fdb66-525">accNavigate</span></span>
-   <span data-ttu-id="fdb66-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="fdb66-526">accSelect</span></span>
-   <span data-ttu-id="fdb66-527">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="fdb66-527">get\_accChild</span></span>
-   <span data-ttu-id="fdb66-528">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="fdb66-528">get\_accChildCount</span></span>
-   <span data-ttu-id="fdb66-529">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="fdb66-529">get\_accDescription</span></span>
-   <span data-ttu-id="fdb66-530">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="fdb66-530">get\_accFocus</span></span>
-   <span data-ttu-id="fdb66-531">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="fdb66-531">get\_accHelp</span></span>
-   <span data-ttu-id="fdb66-532">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="fdb66-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="fdb66-533">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="fdb66-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="fdb66-534">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="fdb66-534">get\_accName</span></span>
-   <span data-ttu-id="fdb66-535">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-535">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-536">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-536">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-537">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="fdb66-538">\_espace blanc du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="fdb66-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="fdb66-539">Pour plus d’informations sur ce rôle, [**consultez \_ \_ espace système du rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fdb66-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="fdb66-540">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="fdb66-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="fdb66-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="fdb66-541">accLocation</span></span>
-   <span data-ttu-id="fdb66-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="fdb66-542">accSelect</span></span>
-   <span data-ttu-id="fdb66-543">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="fdb66-543">get\_accParent</span></span>
-   <span data-ttu-id="fdb66-544">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="fdb66-544">get\_accRole</span></span>
-   <span data-ttu-id="fdb66-545">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="fdb66-545">get\_accState</span></span>

 

 