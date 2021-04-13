---
title: Barre de titre (référence des éléments d’interface utilisateur MSAA)
description: La barre de titre en haut d’une fenêtre affiche une icône et une ligne de texte définies par l’application.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381423"
---
# <a name="title-bar-msaa-ui-element-reference"></a><span data-ttu-id="8faab-103">Barre de titre (référence des éléments d’interface utilisateur MSAA)</span><span class="sxs-lookup"><span data-stu-id="8faab-103">Title Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="8faab-104">Cette rubrique décrit les objets de **barre de titre** à des fins de référence d’élément d’interface utilisateur MSAA.</span><span class="sxs-lookup"><span data-stu-id="8faab-104">This topic describes **Title Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="8faab-105">La procédure de création d’objets de **barre de titre** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici.</span><span class="sxs-lookup"><span data-stu-id="8faab-105">How to create **Title Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="8faab-106">Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="8faab-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="8faab-107">La barre de titre en haut d’une fenêtre affiche une icône et une ligne de texte définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="8faab-107">The title bar at the top of a window displays an application-defined icon and line of text.</span></span> <span data-ttu-id="8faab-108">Le texte spécifie le nom de l’application et indique l’objectif de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8faab-108">The text specifies the name of the application and indicates the purpose of the window.</span></span> <span data-ttu-id="8faab-109">La barre de titre permet également à l’utilisateur de déplacer la fenêtre à l’aide d’une souris ou d’un autre dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="8faab-109">The title bar also makes it possible for the user to move the window using a mouse or other pointing device.</span></span>

<span data-ttu-id="8faab-110">Les barres de titre contiennent au moins trois petits boutons qui permettent de réduire, d’agrandir ou de restaurer et de fermer la fenêtre associée à la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8faab-110">Title bars contain at least three small buttons that minimize, maximize or restore, and close the window associated with the title bar.</span></span> <span data-ttu-id="8faab-111">Les barres de titre contiennent également un bouton d’aide contextuelle.</span><span class="sxs-lookup"><span data-stu-id="8faab-111">Title bars also contain a context-sensitive Help button.</span></span> <span data-ttu-id="8faab-112">Les applications qui s’exécutent dans la version Far-East du système d’exploitation Windows peuvent également contenir des boutons de l’éditeur de méthode d’entrée (IME).</span><span class="sxs-lookup"><span data-stu-id="8faab-112">Applications running in the Far-East version of the Windows operating system may also contain Input Method Editor (IME) buttons.</span></span> <span data-ttu-id="8faab-113">Microsoft Active Accessibility expose ces boutons en tant qu’éléments enfants de la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8faab-113">Microsoft Active Accessibility exposes these buttons as child elements of the title bar.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="8faab-114">Méthodes IAccessible</span><span class="sxs-lookup"><span data-stu-id="8faab-114">IAccessible Methods</span></span>

<span data-ttu-id="8faab-115">Les barres de titre prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="8faab-115">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="8faab-116">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="8faab-116">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="8faab-117">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="8faab-117">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="8faab-118">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="8faab-118">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="8faab-119">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="8faab-119">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="8faab-120">Propriétés IAccessible</span><span class="sxs-lookup"><span data-stu-id="8faab-120">IAccessible Properties</span></span>

<span data-ttu-id="8faab-121">Les barres de titre prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :</span><span class="sxs-lookup"><span data-stu-id="8faab-121">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8faab-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="8faab-122">Property</span></span></th>
<th><span data-ttu-id="8faab-123">Commentaires</span><span class="sxs-lookup"><span data-stu-id="8faab-123">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8faab-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="8faab-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="8faab-125">La propriété <strong>ChildCount</strong> est cinq.</span><span class="sxs-lookup"><span data-stu-id="8faab-125">The <strong>ChildCount</strong> property is five.</span></span> <span data-ttu-id="8faab-126">La propriété <strong>ChildCount</strong> comprend l’éditeur IME et les boutons d’aide contextuelle, même lorsqu’ils ne sont pas affichés.</span><span class="sxs-lookup"><span data-stu-id="8faab-126">The <strong>ChildCount</strong> property includes the IME and context-sensitive Help buttons even when they are not displayed.</span></span> <span data-ttu-id="8faab-127">Les boutons qui ne sont pas affichés ont la propriété <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8faab-127">Buttons that are not displayed have the <strong>State</strong> property <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8faab-128"><strong>get_accDescription</strong></span><span class="sxs-lookup"><span data-stu-id="8faab-128"><strong>get_accDescription</strong></span></span></td>
<td><span data-ttu-id="8faab-129">La propriété <strong>Description</strong> de la barre de titre elle-même est : &quot; affiche le nom de la fenêtre et contient des contrôles pour la manipuler. &quot; Les boutons enfants de la barre de titre présentent les descriptions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8faab-129">The <strong>Description</strong> property of the title bar itself is: &quot;Displays the name of the window and contains controls to manipulate it.&quot; The child buttons in the title bar have the following descriptions:</span></span><br/>
<ul>
<li><span data-ttu-id="8faab-130">&quot;Déplace la fenêtre en dehors de</span><span class="sxs-lookup"><span data-stu-id="8faab-130">&quot;Moves the window out of</span></span></li>
<li><span data-ttu-id="8faab-131">&quot;Rend la fenêtre complète</span><span class="sxs-lookup"><span data-stu-id="8faab-131">&quot;Makes the window full</span></span></li>
<li><span data-ttu-id="8faab-132">&quot;Place un réduit ou un</span><span class="sxs-lookup"><span data-stu-id="8faab-132">&quot;Puts a minimized or</span></span></li>
<li><span data-ttu-id="8faab-133">&quot;Ferme la fenêtre&quot;</span><span class="sxs-lookup"><span data-stu-id="8faab-133">&quot;Closes the window&quot;</span></span></li>
<li><span data-ttu-id="8faab-134">&quot;Entrée ou sortie du contexte-</span><span class="sxs-lookup"><span data-stu-id="8faab-134">&quot;Enters or leaves context-</span></span></li>
<li><span data-ttu-id="8faab-135">&quot;Affiche le clavier quand vous appuyez sur&quot;</span><span class="sxs-lookup"><span data-stu-id="8faab-135">&quot;Brings up the keyboard when pressed&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8faab-136"><strong>get_accName</strong></span><span class="sxs-lookup"><span data-stu-id="8faab-136"><strong>get_accName</strong></span></span></td>
<td><span data-ttu-id="8faab-137">La barre de titre elle-même ne prend pas en charge la propriété <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="8faab-137">The title bar itself does not support the <strong>Name</strong> property.</span></span> <span data-ttu-id="8faab-138">Les boutons enfants de la barre de titre portent les noms suivants :</span><span class="sxs-lookup"><span data-stu-id="8faab-138">The child buttons in the title bar have the following names:</span></span>
<ul>
<li><span data-ttu-id="8faab-139">&quot;Réduire&quot;</span><span class="sxs-lookup"><span data-stu-id="8faab-139">&quot;Minimize&quot;</span></span></li>
<li><span data-ttu-id="8faab-140">&quot;Agrandir &quot; ou &quot; restaurer &quot; ,</span><span class="sxs-lookup"><span data-stu-id="8faab-140">&quot;Maximize&quot; or &quot;Restore&quot;,</span></span></li>
<li><span data-ttu-id="8faab-141">&quot;Close&quot;</span><span class="sxs-lookup"><span data-stu-id="8faab-141">&quot;Close&quot;</span></span></li>
<li><span data-ttu-id="8faab-142">&quot;Aide contextuelle&quot;</span><span class="sxs-lookup"><span data-stu-id="8faab-142">&quot;Context help&quot;</span></span></li>
<li><span data-ttu-id="8faab-143">&quot;IME&quot;</span><span class="sxs-lookup"><span data-stu-id="8faab-143">&quot;IME&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8faab-144"><strong>get_accParent</strong></span><span class="sxs-lookup"><span data-stu-id="8faab-144"><strong>get_accParent</strong></span></span></td>
<td><span data-ttu-id="8faab-145">La propriété <strong>parent</strong> de la barre de titre est la fenêtre d’application principale ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) qui a le même nom de classe de fenêtre définie par l’application que la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8faab-145">The <strong>Parent</strong> property of the title bar is the main application window ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) that has the same application-defined window class name as the title bar.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8faab-146"><strong>get_accRole</strong></span><span class="sxs-lookup"><span data-stu-id="8faab-146"><strong>get_accRole</strong></span></span></td>
<td><span data-ttu-id="8faab-147">La propriété de <strong>rôle</strong> est <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8faab-147">The <strong>Role</strong> property is <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span></span> <span data-ttu-id="8faab-148">Les boutons enfants de la barre de titre ont la propriété <strong>Role</strong> <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8faab-148">The child buttons in the title bar have the <strong>Role</strong> property <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8faab-149"><strong>get_accState</strong></span><span class="sxs-lookup"><span data-stu-id="8faab-149"><strong>get_accState</strong></span></span></td>
<td><span data-ttu-id="8faab-150">La propriété <strong>State</strong> pour la barre de titre et les boutons enfants peuvent être une combinaison d’une ou plusieurs des <a href="object-state-constants.md">valeurs</a>suivantes : <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="8faab-150">The <strong>State</strong> property for the title bar and the child buttons can be a combination of one or more of the following <a href="object-state-constants.md">values</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8faab-151"><strong>get_accValue</strong></span><span class="sxs-lookup"><span data-stu-id="8faab-151"><strong>get_accValue</strong></span></span></td>
<td><span data-ttu-id="8faab-152">La propriété <strong>valeur</strong> est une chaîne qui est identique au texte affiché dans la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="8faab-152">The <strong>Value</strong> property is a string that is the same as the text displayed in the title bar.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="8faab-153">Notes</span><span class="sxs-lookup"><span data-stu-id="8faab-153">Notes</span></span>

-   <span data-ttu-id="8faab-154">Bien que la barre de titre d’une application ait la propriété **État** indicateur de l’état du système, elle n’a jamais le [**\_ \_ focus**](object-state-constants.md)sur le système d’état de l’indicateur d' **État** . [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="8faab-154">Although an application's title bar has the **State** property flag [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md), it never has the **State** flag [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md).</span></span> <span data-ttu-id="8faab-155">La définition du focus sur un objet de barre de titre est axée sur la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="8faab-155">Setting focus to a title bar object focuses the application window.</span></span>
-   <span data-ttu-id="8faab-156">Étant donné que l’objet de barre de titre ne prend pas en charge l' [**affichage des \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), les boutons de la barre de titre sont des éléments simples.</span><span class="sxs-lookup"><span data-stu-id="8faab-156">Because the title bar object does not support [**get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), the buttons on the title bar are simple elements.</span></span> <span data-ttu-id="8faab-157">Ils ne prennent pas en charge l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proprement dit.</span><span class="sxs-lookup"><span data-stu-id="8faab-157">They do not support the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface themselves.</span></span> <span data-ttu-id="8faab-158">L’objet barre de titre fournit des informations sur ces boutons enfants.</span><span class="sxs-lookup"><span data-stu-id="8faab-158">The title bar object provides information about these child buttons.</span></span>
-   <span data-ttu-id="8faab-159">Comme les barres de titre n’obtiennent pas le focus et n’ont pas d’action par défaut, les méthodes [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) et [**\_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) ne sont pas prises en charge pour ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="8faab-159">Because title bars do not get focus and have no default action, the [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) and [**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) methods are not supported for this control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8faab-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8faab-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8faab-161">IAccessible, interface</span><span class="sxs-lookup"><span data-stu-id="8faab-161">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





