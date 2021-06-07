---
title: Autres rôles d’objet et méthodes prises en charge (référence des éléments d’interface utilisateur MSAA)
description: Cette rubrique fournit des informations sur les rôles d’objet qui ne sont pas inclus dans les rubriques précédentes relatives aux éléments d’interface utilisateur.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444000"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="2cf8b-103">Autres rôles d’objet et méthodes prises en charge (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="2cf8b-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="2cf8b-104">Cette rubrique fournit des informations sur les rôles d’objet qui ne sont pas inclus dans les rubriques précédentes relatives aux éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2cf8b-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="2cf8b-105">Chaque rôle d’objet comprend une liste des méthodes et des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) prises en charge pour le rôle d’objet.</span><span class="sxs-lookup"><span data-stu-id="2cf8b-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="2cf8b-106">Tandis que d’autres rubriques documentées ont pris en charge les méthodes et propriétés **IAccessible** pour les éléments d’interface utilisateur, cette rubrique répertorie les méthodes et les propriétés que vous pouvez vous attendre à prendre en charge pour un rôle d’objet particulier.</span><span class="sxs-lookup"><span data-stu-id="2cf8b-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="2cf8b-107">La plupart des éléments d’interface utilisateur qui peuvent avoir l’un des rôles répertoriés ici sont généralement affichés dans les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="2cf8b-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="2cf8b-108">Utilisez cette rubrique comme indication.</span><span class="sxs-lookup"><span data-stu-id="2cf8b-108">Use this topic as a guideline.</span></span> <span data-ttu-id="2cf8b-109">Nous vous suggérons vivement d’utiliser les outils de Active Accessibility Microsoft pour vérifier le comportement attendu pour un rôle d’objet individuel.</span><span class="sxs-lookup"><span data-stu-id="2cf8b-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="2cf8b-110">Le tableau suivant répertorie les rôles d’objet supplémentaires que Oleacc.dll prend en charge.</span><span class="sxs-lookup"><span data-stu-id="2cf8b-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="2cf8b-111">**\_alerte du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="2cf8b-112">**déroulant système de rôle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="2cf8b-113">**\_application de système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="2cf8b-114">**\_équation du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="2cf8b-115">**\_bordure du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="2cf8b-116">**\_graphique du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="2cf8b-117">**système de rôle \_ \_ BUTTONDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="2cf8b-118">**système de rôle \_ \_ HELPBALLOON**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="2cf8b-119">**système de rôle \_ \_ BUTTONDROPDOWNGRID**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="2cf8b-120">**\_adresse IP du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="2cf8b-121">**système de rôle \_ \_ BUTTONMENU**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="2cf8b-122">**\_lien système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="2cf8b-123">**\_cellule système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="2cf8b-124">**\_volet système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="2cf8b-125">**\_caractère système du rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="2cf8b-126">**\_ligne du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="2cf8b-127">**\_graphique de système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="2cf8b-128">**système de rôle \_ \_ ROWHEADER**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="2cf8b-129">**\_horloge système du rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="2cf8b-130">**\_séparateur système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="2cf8b-131">**\_colonne système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="2cf8b-132">**\_son du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="2cf8b-133">**\_diagramme du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="2cf8b-134">**système de rôle \_ \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="2cf8b-135">**\_numérotation du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="2cf8b-136">**\_table système des rôles \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="2cf8b-137">**\_document système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="2cf8b-138">**\_espace blanc du système de rôle \_**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="2cf8b-139">\_alerte du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="2cf8b-140">Pour plus d’informations sur ce rôle, [**consultez \_ \_ alerte du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-141">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-142">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-142">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-143">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-143">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-144">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="2cf8b-145">\_application de système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="2cf8b-146">Pour plus d’informations sur ce rôle, consultez rôle de l' [**\_ \_ application système**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-147">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-148">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-149">accLocation</span></span>
-   <span data-ttu-id="2cf8b-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-150">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-151">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-151">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-152">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-152">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-153">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-153">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-154">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-154">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-155">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-156">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-157">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-157">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-158">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-158">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-159">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-159">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-160">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="2cf8b-161">\_bordure du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="2cf8b-162">Pour plus d’informations sur ce rôle, consultez la rubrique [**\_ \_ bordure du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-163">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-164">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-165">accLocation</span></span>
-   <span data-ttu-id="2cf8b-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-166">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-167">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-167">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-168">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="2cf8b-169">système de rôle \_ \_ BUTTONDROPDOWN</span><span class="sxs-lookup"><span data-stu-id="2cf8b-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="2cf8b-170">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ BUTTONDROPDOWN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-171">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-173">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-174">accLocation</span></span>
-   <span data-ttu-id="2cf8b-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-175">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-176">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-176">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-177">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-177">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-178">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-179">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-179">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-180">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-180">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-181">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-182">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-183">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-183">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-184">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-184">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-185">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-185">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-186">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="2cf8b-187">système de rôle \_ \_ BUTTONDROPDOWNGRID</span><span class="sxs-lookup"><span data-stu-id="2cf8b-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="2cf8b-188">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ BUTTONDROPDOWNGRID**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-189">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-191">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-192">accLocation</span></span>
-   <span data-ttu-id="2cf8b-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-193">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-194">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-194">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-195">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-195">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-196">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-197">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-197">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-198">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-198">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-199">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-200">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-201">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-201">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-202">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-202">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-203">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-203">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-204">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="2cf8b-205">système de rôle \_ \_ BUTTONMENU</span><span class="sxs-lookup"><span data-stu-id="2cf8b-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="2cf8b-206">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ BUTTONMENU**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-207">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-209">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-210">accLocation</span></span>
-   <span data-ttu-id="2cf8b-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-211">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-212">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-213">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-213">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-214">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-214">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-215">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-216">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-217">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-217">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-218">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-218">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-219">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-219">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-220">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="2cf8b-221">\_cellule système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="2cf8b-222">Pour plus d’informations sur ce rôle, consultez la rubrique [**\_ \_ cellule système Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-223">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-224">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-225">accLocation</span></span>
-   <span data-ttu-id="2cf8b-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-226">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="2cf8b-227">accSelect</span></span>
-   <span data-ttu-id="2cf8b-228">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-228">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-229">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-229">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-230">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-230">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-231">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-231">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-232">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-233">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-234">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-234">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-235">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-235">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-236">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-236">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-237">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-237">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-238">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="2cf8b-239">\_caractère système du rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="2cf8b-240">Pour plus d’informations sur ce rôle, [**consultez \_ \_ caractère système du rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-241">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-242">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-243">accLocation</span></span>
-   <span data-ttu-id="2cf8b-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-244">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-245">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="2cf8b-245">get\_accDescription</span></span>
-   <span data-ttu-id="2cf8b-246">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-246">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-247">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-248">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-248">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-249">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-249">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-250">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-250">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-251">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-251">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-252">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="2cf8b-253">\_graphique de système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="2cf8b-254">Pour plus d’informations sur ce rôle, consultez la rubrique [**\_ \_ graphique de système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-255">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-256">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-257">accLocation</span></span>
-   <span data-ttu-id="2cf8b-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-258">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-259">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-259">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-260">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-260">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-261">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-261">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-262">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-262">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-263">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-264">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-265">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-265">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-266">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-266">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-267">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-267">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-268">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="2cf8b-269">\_horloge système du rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="2cf8b-270">Pour plus d’informations sur ce rôle, [**consultez \_ \_ horloge du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-271">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-272">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-273">accLocation</span></span>
-   <span data-ttu-id="2cf8b-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-274">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-275">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-275">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-276">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-276">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-277">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-278">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-279">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-279">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-280">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-280">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-281">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-281">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-282">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-282">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-283">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="2cf8b-284">\_colonne système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="2cf8b-285">Pour plus d’informations sur ce rôle, [**consultez \_ \_ colonne système Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-286">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-287">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-288">accLocation</span></span>
-   <span data-ttu-id="2cf8b-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-289">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="2cf8b-290">accSelect</span></span>
-   <span data-ttu-id="2cf8b-291">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-291">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-292">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-292">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-293">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-293">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-294">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-294">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-295">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-295">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-296">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-296">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-297">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-297">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-298">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="2cf8b-299">\_diagramme du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="2cf8b-300">Pour plus d’informations sur ce rôle, [**consultez \_ \_ diagramme du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-301">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-302">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-303">accLocation</span></span>
-   <span data-ttu-id="2cf8b-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-304">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-305">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-305">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-306">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-306">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-307">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-307">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-308">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-308">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-309">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-310">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-311">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-311">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-312">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-312">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-313">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-313">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-314">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="2cf8b-315">\_numérotation du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="2cf8b-316">Pour plus d’informations sur ce rôle, consultez la page [**\_ \_ accès au système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-317">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-319">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-320">accLocation</span></span>
-   <span data-ttu-id="2cf8b-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-321">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-322">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-323">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-323">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-324">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-324">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-325">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-326">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-327">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-327">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-328">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-328">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-329">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-329">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-330">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-330">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-331">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="2cf8b-332">\_document système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="2cf8b-333">Pour plus d’informations sur ce rôle, [**consultez \_ \_ document de système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-334">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-335">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-336">accLocation</span></span>
-   <span data-ttu-id="2cf8b-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-337">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="2cf8b-338">accSelect</span></span>
-   <span data-ttu-id="2cf8b-339">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-339">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-340">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-340">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-341">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-341">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-342">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-342">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-343">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-343">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-344">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-344">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-345">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="2cf8b-346">déroulant système de rôle \_ \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="2cf8b-347">Pour plus d’informations sur ce rôle, consultez la page [**\_ \_ déroulante système de rôles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-348">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-350">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-351">accLocation</span></span>
-   <span data-ttu-id="2cf8b-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-352">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-353">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-353">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-354">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-354">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-355">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-356">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-356">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-357">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-357">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-358">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-359">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-360">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-360">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-361">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-361">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-362">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-362">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-363">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="2cf8b-364">\_équation du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="2cf8b-365">Pour plus d’informations sur ce rôle, [**consultez \_ \_ équation du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-366">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-367">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-368">accLocation</span></span>
-   <span data-ttu-id="2cf8b-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-369">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-370">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-370">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-371">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-371">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-372">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-372">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-373">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-373">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-374">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-374">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-375">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="2cf8b-376">\_graphique du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="2cf8b-377">Pour plus d’informations sur ce rôle, [**consultez \_ \_ graphique du système de rôles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-378">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-379">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-380">accLocation</span></span>
-   <span data-ttu-id="2cf8b-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-381">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-382">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-382">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-383">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-383">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-384">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-385">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-386">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-386">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-387">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-387">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-388">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-388">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-389">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="2cf8b-390">système de rôle \_ \_ HELPBALLOON</span><span class="sxs-lookup"><span data-stu-id="2cf8b-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="2cf8b-391">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ HELPBALLOON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-392">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-393">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-394">accLocation</span></span>
-   <span data-ttu-id="2cf8b-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-395">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-396">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-396">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-397">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-397">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-398">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-399">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-399">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-400">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-400">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-401">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-401">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-402">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-402">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-403">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="2cf8b-404">\_adresse IP du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="2cf8b-405">Pour plus d’informations sur ce rôle, [**consultez \_ \_ adresse IP du système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-406">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-407">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-408">accLocation</span></span>
-   <span data-ttu-id="2cf8b-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-409">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-410">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-410">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-411">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-411">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-412">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-412">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-413">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-413">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-414">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-415">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-416">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-416">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-417">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-417">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-418">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-418">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-419">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-419">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-420">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="2cf8b-421">\_lien système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="2cf8b-422">Pour plus d’informations sur ce rôle, [**consultez \_ \_ lien système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-423">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-425">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-426">accLocation</span></span>
-   <span data-ttu-id="2cf8b-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-427">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-428">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-428">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-429">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-429">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-430">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-431">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="2cf8b-431">get\_accDescription</span></span>
-   <span data-ttu-id="2cf8b-432">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-432">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-433">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-434">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-434">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-435">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-435">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-436">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-436">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-437">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-437">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-438">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="2cf8b-439">\_volet système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="2cf8b-440">Pour plus d’informations sur ce rôle, [**consultez \_ \_ volet système de rôles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-441">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-442">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-443">accLocation</span></span>
-   <span data-ttu-id="2cf8b-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-444">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-445">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-445">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-446">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-446">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-447">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-447">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-448">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-448">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-449">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-450">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-451">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-451">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-452">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-452">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-453">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-453">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-454">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="2cf8b-455">\_ligne du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="2cf8b-456">Pour plus d’informations sur ce rôle, consultez rôle de la [**\_ \_ ligne système**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-457">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-458">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-459">accLocation</span></span>
-   <span data-ttu-id="2cf8b-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-460">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="2cf8b-461">accSelect</span></span>
-   <span data-ttu-id="2cf8b-462">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-462">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-463">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-463">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-464">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="2cf8b-464">get\_accDescription</span></span>
-   <span data-ttu-id="2cf8b-465">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-465">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-466">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-466">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-467">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-467">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-468">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-468">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-469">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-469">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-470">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="2cf8b-471">système de rôle \_ \_ ROWHEADER</span><span class="sxs-lookup"><span data-stu-id="2cf8b-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="2cf8b-472">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ ROWHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-473">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-474">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-475">accLocation</span></span>
-   <span data-ttu-id="2cf8b-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-476">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="2cf8b-477">accSelect</span></span>
-   <span data-ttu-id="2cf8b-478">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-478">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-479">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-479">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-480">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-481">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="2cf8b-481">get\_accDescription</span></span>
-   <span data-ttu-id="2cf8b-482">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-482">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-483">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-483">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-484">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-484">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-485">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-485">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-486">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-486">get\_accState</span></span>
-   <span data-ttu-id="2cf8b-487">Obtient \_ accValue</span><span class="sxs-lookup"><span data-stu-id="2cf8b-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="2cf8b-488">\_séparateur système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="2cf8b-489">Pour plus d’informations sur ce rôle, [**consultez \_ \_ séparateur de système de rôles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-490">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-491">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-492">accLocation</span></span>
-   <span data-ttu-id="2cf8b-493">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-493">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-494">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-494">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-495">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-495">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-496">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-496">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-497">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="2cf8b-498">\_son du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="2cf8b-499">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ audio**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-500">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-501">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="2cf8b-501">get\_accDescription</span></span>
-   <span data-ttu-id="2cf8b-502">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-502">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-503">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-503">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-504">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="2cf8b-505">système de rôle \_ \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="2cf8b-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="2cf8b-506">Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-507">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-509">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-510">accLocation</span></span>
-   <span data-ttu-id="2cf8b-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-511">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-512">Obtient \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="2cf8b-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="2cf8b-513">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-513">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-514">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-515">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-516">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-516">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-517">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-517">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-518">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-518">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-519">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="2cf8b-520">\_table système des rôles \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="2cf8b-521">Pour plus d’informations sur ce rôle, [**consultez \_ \_ table système Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-522">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="2cf8b-523">accHitTest</span></span>
-   <span data-ttu-id="2cf8b-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-524">accLocation</span></span>
-   <span data-ttu-id="2cf8b-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="2cf8b-525">accNavigate</span></span>
-   <span data-ttu-id="2cf8b-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="2cf8b-526">accSelect</span></span>
-   <span data-ttu-id="2cf8b-527">Obtient \_ accChild</span><span class="sxs-lookup"><span data-stu-id="2cf8b-527">get\_accChild</span></span>
-   <span data-ttu-id="2cf8b-528">Obtient \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="2cf8b-528">get\_accChildCount</span></span>
-   <span data-ttu-id="2cf8b-529">Obtient \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="2cf8b-529">get\_accDescription</span></span>
-   <span data-ttu-id="2cf8b-530">Obtient \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="2cf8b-530">get\_accFocus</span></span>
-   <span data-ttu-id="2cf8b-531">Obtient \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="2cf8b-531">get\_accHelp</span></span>
-   <span data-ttu-id="2cf8b-532">Obtient \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="2cf8b-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="2cf8b-533">Obtient \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2cf8b-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="2cf8b-534">Obtient \_ accName</span><span class="sxs-lookup"><span data-stu-id="2cf8b-534">get\_accName</span></span>
-   <span data-ttu-id="2cf8b-535">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-535">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-536">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-536">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-537">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="2cf8b-538">\_espace blanc du système de rôle \_</span><span class="sxs-lookup"><span data-stu-id="2cf8b-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="2cf8b-539">Pour plus d’informations sur ce rôle, [**consultez \_ \_ espace système du rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cf8b-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="2cf8b-540">**Propriétés et méthodes prises en charge**</span><span class="sxs-lookup"><span data-stu-id="2cf8b-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="2cf8b-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="2cf8b-541">accLocation</span></span>
-   <span data-ttu-id="2cf8b-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="2cf8b-542">accSelect</span></span>
-   <span data-ttu-id="2cf8b-543">Obtient \_ accParent</span><span class="sxs-lookup"><span data-stu-id="2cf8b-543">get\_accParent</span></span>
-   <span data-ttu-id="2cf8b-544">Obtient \_ accRole</span><span class="sxs-lookup"><span data-stu-id="2cf8b-544">get\_accRole</span></span>
-   <span data-ttu-id="2cf8b-545">Obtient \_ accState</span><span class="sxs-lookup"><span data-stu-id="2cf8b-545">get\_accState</span></span>

 

 