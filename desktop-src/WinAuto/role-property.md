---
title: Role, propriété
description: La propriété Role décrit l’élément d’interface utilisateur d’un objet. Tous les objets prennent en charge la propriété Role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510197"
---
# <a name="role-property"></a><span data-ttu-id="f63b5-104">Role, propriété</span><span class="sxs-lookup"><span data-stu-id="f63b5-104">Role Property</span></span>

<span data-ttu-id="f63b5-105">La propriété **role** décrit l’élément d’interface utilisateur d’un objet.</span><span class="sxs-lookup"><span data-stu-id="f63b5-105">The **Role** property describes an object's user interface element.</span></span> <span data-ttu-id="f63b5-106">Tous les objets prennent en charge la propriété **role** .</span><span class="sxs-lookup"><span data-stu-id="f63b5-106">All objects support the **Role** property.</span></span>

<span data-ttu-id="f63b5-107">Dans de nombreux cas, le rôle de l’objet est évident.</span><span class="sxs-lookup"><span data-stu-id="f63b5-107">In many cases, the object's role is obvious.</span></span> <span data-ttu-id="f63b5-108">Par exemple, Windows ont le rôle de [**\_ \_ fenêtre système rôle**](object-roles.md) et les boutons de commande Push ont le rôle [**\_ \_ PUSHBUTTON système rôle**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="f63b5-108">For example, windows have the [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) role and push buttons have the [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md) role.</span></span>

<span data-ttu-id="f63b5-109">La propriété **role** est récupérée en appelant [**IAccessible :: \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span><span class="sxs-lookup"><span data-stu-id="f63b5-109">The **Role** property is retrieved by calling [**IAccessible::get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span></span>

## <a name="identifying-an-objects-role"></a><span data-ttu-id="f63b5-110">Identification du rôle d’un objet</span><span class="sxs-lookup"><span data-stu-id="f63b5-110">Identifying an Object's Role</span></span>

<span data-ttu-id="f63b5-111">Microsoft Active Accessibility fournit des [constantes de rôle](object-roles.md), définies dans oleacc. h, qui identifient les rôles d’objet communs.</span><span class="sxs-lookup"><span data-stu-id="f63b5-111">Microsoft Active Accessibility provides [role constants](object-roles.md), defined in oleacc.h, that identify common object roles.</span></span> <span data-ttu-id="f63b5-112">Il est recommandé que les développeurs de serveurs utilisent ces valeurs de rôle prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="f63b5-112">It is recommended that server developers use these predefined role values.</span></span> <span data-ttu-id="f63b5-113">Si une constante de rôle prédéfinie est retournée, les clients utilisent la fonction [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) pour récupérer une chaîne localisée qui décrit le rôle.</span><span class="sxs-lookup"><span data-stu-id="f63b5-113">If a predefined role constant is returned, clients use the [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) function to retrieve a localized string that describes the role.</span></span>

<span data-ttu-id="f63b5-114">Pour les contrôles d’animation, tels que le contrôle d’animation affiché lors de la copie de fichiers, utilisez l' [**\_ \_ animation de système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f63b5-114">For animation controls, such as the animation control displayed when copying files, use [**ROLE\_SYSTEM\_ANIMATION**](object-roles.md).</span></span> <span data-ttu-id="f63b5-115">Les graphiques qui sont parfois animés sont décrits comme un [**\_ \_ graphique de système de rôle**](object-roles.md) avec la propriété [**État**](state-property.md) définie sur [**état \_ système \_ animé**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f63b5-115">Graphics that are occasionally animated are described as [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md) with the [**State**](state-property.md) property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md).</span></span>

<span data-ttu-id="f63b5-116">Notez que certains rôles ne sont pas faciles à décrire.</span><span class="sxs-lookup"><span data-stu-id="f63b5-116">Note that some roles are not easy to describe.</span></span> <span data-ttu-id="f63b5-117">Par exemple, la vue de grande icône d’un dossier permet une disposition arbitraire des icônes, donc son rôle peut être décrit comme [**\_ \_ regroupement de système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f63b5-117">For example, a folder's large-icon view allows arbitrary arrangement of icons, so its role could be described as [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span> <span data-ttu-id="f63b5-118">Ou un contrôle qui fournit des éléments dans des lignes et des colonnes fixes peut avoir le rôle de [**\_ \_ table système Role**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="f63b5-118">Or, a control that provides items in fixed rows and columns could have the [**ROLE\_SYSTEM\_TABLE**](object-roles.md) role.</span></span> <span data-ttu-id="f63b5-119">Étant donné qu’un rôle est utilisé pour communiquer le modèle d’utilisation à un utilisateur final, il est important d’utiliser le rôle approprié.</span><span class="sxs-lookup"><span data-stu-id="f63b5-119">Since a role is used to communicate the use model to an end user, it is important to use the appropriate role.</span></span> <span data-ttu-id="f63b5-120">Par exemple, si votre contrôle agit comme un bouton, utilisez le [**\_ \_ PUSHBUTTON système de rôle**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f63b5-120">For example, if your control acts like a button, then use [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md).</span></span>

 

 




