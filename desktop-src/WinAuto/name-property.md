---
title: Propriété Name
description: La propriété Name est une chaîne utilisée par les clients pour identifier, Rechercher ou annoncer un objet pour l’utilisateur. Tous les objets prennent en charge la propriété Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512669"
---
# <a name="name-property"></a><span data-ttu-id="f47f6-104">Propriété Name</span><span class="sxs-lookup"><span data-stu-id="f47f6-104">Name Property</span></span>

<span data-ttu-id="f47f6-105">La propriété **Name** est une chaîne utilisée par les clients pour identifier, Rechercher ou annoncer un objet pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f47f6-105">The **Name** property is a string used by clients to identify, find, or announce an object for the user.</span></span> <span data-ttu-id="f47f6-106">Tous les objets prennent en charge la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="f47f6-106">All objects support the **Name** property.</span></span>

<span data-ttu-id="f47f6-107">Par exemple, le texte d’un contrôle bouton est son nom, tandis que le nom d’une zone de liste ou d’un contrôle d’édition est le texte statique qui précède immédiatement le contrôle dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="f47f6-107">For example, the text on a button control is its name, while the name for a list box or edit control is the static text that immediately precedes the control in the tabbing order.</span></span> <span data-ttu-id="f47f6-108">Même les objets graphiques qui n’affichent pas de nom fournissent du texte lorsqu’ils sont interrogés pour la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="f47f6-108">Even graphic objects that do not display a name provide text when queried for the **Name** property.</span></span>

<span data-ttu-id="f47f6-109">La propriété **Name** est récupérée en appelant [**IAccessible :: \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span><span class="sxs-lookup"><span data-stu-id="f47f6-109">The **Name** property is retrieved by calling [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span></span>

## <a name="selecting-names"></a><span data-ttu-id="f47f6-110">Sélection de noms</span><span class="sxs-lookup"><span data-stu-id="f47f6-110">Selecting Names</span></span>

<span data-ttu-id="f47f6-111">Le nom d’un objet doit être intuitif afin que les utilisateurs comprennent la signification ou l’objectif de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f47f6-111">An object's name should be intuitive so that users understand the object's meaning or purpose.</span></span> <span data-ttu-id="f47f6-112">En outre, la propriété **Name** doit être unique par rapport à tous les objets frères dans le parent.</span><span class="sxs-lookup"><span data-stu-id="f47f6-112">Also, the **Name** property should be unique relative to any sibling objects in the parent.</span></span>

<span data-ttu-id="f47f6-113">La navigation dans les tables présente des problèmes particulièrement difficiles pour certains utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f47f6-113">Navigation within tables presents especially difficult problems for some users.</span></span> <span data-ttu-id="f47f6-114">Par conséquent, les développeurs de serveurs doivent faire en sorte que les noms des cellules de tableau soient aussi descriptifs que possible.</span><span class="sxs-lookup"><span data-stu-id="f47f6-114">Therefore, server developers should make table cell names as descriptive as possible.</span></span> <span data-ttu-id="f47f6-115">Par exemple, vous pouvez créer un nom de cellule en combinant les noms de la ligne et de la colonne qu’il occupe, par exemple « a1 ».</span><span class="sxs-lookup"><span data-stu-id="f47f6-115">For example, you could create a cell name by combining the names of the row and column it occupies, such as "A1."</span></span> <span data-ttu-id="f47f6-116">Toutefois, il est généralement préférable d’utiliser des noms plus descriptifs, tels que « Nancy, février » où « Nancy » est la ligne actuelle et « février » est la colonne actuelle.</span><span class="sxs-lookup"><span data-stu-id="f47f6-116">However, it is generally better to use more descriptive names, such as "Nancy, February" where "Nancy" is the current row and "February" is the current column.</span></span>

## <a name="delegating-requests"></a><span data-ttu-id="f47f6-117">Délégation de requêtes</span><span class="sxs-lookup"><span data-stu-id="f47f6-117">Delegating Requests</span></span>

<span data-ttu-id="f47f6-118">Si un objet n’a pas accès à sa propriété **Name** , il délègue les demandes à son parent, s’identifiant lui-même par son ID enfant.</span><span class="sxs-lookup"><span data-stu-id="f47f6-118">If an object does not have access to its **Name** property, it delegates requests to its parent, identifying itself by its child ID.</span></span> <span data-ttu-id="f47f6-119">Par exemple, si un client appelle la propriété **Name** d’un contrôle d’édition, le contrôle d’édition délègue la requête à son parent, qui retourne la valeur du contrôle de texte statique qui étiquette le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="f47f6-119">For example, if a client calls an edit control's **Name** property, the edit control delegates the query to its parent, which returns the value of the static text control that labels the edit control.</span></span>

 

 




