---
description: À compter de Windows XP, le panneau de configuration prend en charge la catégorisation des éléments du panneau de configuration. Les éléments sont inscrits pour apparaître dans une ou plusieurs catégories. Impossible de créer des catégories.
title: Affectation des catégories du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972075"
---
# <a name="assigning-control-panel-categories"></a><span data-ttu-id="fbaf1-105">Affectation des catégories du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="fbaf1-105">Assigning Control Panel Categories</span></span>

<span data-ttu-id="fbaf1-106">À compter de Windows XP, le panneau de configuration prend en charge la catégorisation des éléments du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-106">As of Windows XP, Control Panel supports categorization of Control Panel items.</span></span> <span data-ttu-id="fbaf1-107">Les éléments sont inscrits pour apparaître dans une ou plusieurs catégories.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-107">Items are registered to appear in one or more category.</span></span> <span data-ttu-id="fbaf1-108">Impossible de créer des catégories.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-108">New categories cannot be created.</span></span>

<span data-ttu-id="fbaf1-109">Pour inscrire un élément du panneau de configuration dans une ou plusieurs catégories, ajoutez des valeurs comme expliqué dans la section inscription de l’élément du panneau de configuration de l' [exécutable](registering-control-panel-items.md) ou [inscription](registering-control-panel-items.md) de l’élément du panneau de configuration de l’enregistrement des éléments du panneau de [configuration, le](registering-control-panel-items.md)cas échéant.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-109">To register a Control Panel item in one or more categories, add values as explained in the [Executable Control Panel Item Registration](registering-control-panel-items.md) or [DLL Control Panel Item Registration](registering-control-panel-items.md) section of [Registering Control Panel Items](registering-control-panel-items.md), as appropriate.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fbaf1-110">ID de la catégorie</span><span class="sxs-lookup"><span data-stu-id="fbaf1-110">Category ID</span></span></th>
<th><span data-ttu-id="fbaf1-111">Nom de la catégorie (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="fbaf1-111">Category Name (Windows 7)</span></span></th>
<th><span data-ttu-id="fbaf1-112">Nom de la catégorie (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="fbaf1-112">Category Name (Windows Vista)</span></span></th>
<th><span data-ttu-id="fbaf1-113">Nom de la catégorie (Windows XP)</span><span class="sxs-lookup"><span data-stu-id="fbaf1-113">Category Name (Windows XP)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fbaf1-114">0</span><span class="sxs-lookup"><span data-stu-id="fbaf1-114">0</span></span></td>
<td><span data-ttu-id="fbaf1-115">&quot;Tous les éléments du panneau de configuration&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-115">&quot;All Control Panel Items&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-116">&quot;Options supplémentaires&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-116">&quot;Additional Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fbaf1-117">Tout élément du panneau de configuration qui ne spécifie pas d’ID de catégorie apparaît dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-117">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="fbaf1-118">&quot;Autres options du panneau de configuration&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-118">&quot;Other Control Panel Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fbaf1-119">Tout élément du panneau de configuration qui ne spécifie pas d’ID de catégorie apparaît dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-119">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbaf1-120">1</span><span class="sxs-lookup"><span data-stu-id="fbaf1-120">1</span></span></td>
<td><span data-ttu-id="fbaf1-121">&quot;Apparence et personnalisation&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-121">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-122">&quot;Apparence et personnalisation&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-122">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-123">&quot;Apparence et thèmes&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-123">&quot;Appearance and Themes&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbaf1-124">2</span><span class="sxs-lookup"><span data-stu-id="fbaf1-124">2</span></span></td>
<td><span data-ttu-id="fbaf1-125">&quot;Matériel et audio&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-125">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-126">&quot;Matériel et audio&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-126">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-127">&quot;Imprimantes et autres matériels&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-127">&quot;Printers and Other Hardware&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbaf1-128">3</span><span class="sxs-lookup"><span data-stu-id="fbaf1-128">3</span></span></td>
<td><span data-ttu-id="fbaf1-129">&quot;Réseau et Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-129">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-130">&quot;Réseau et Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-130">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-131">&quot;Connexions réseau et Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-131">&quot;Network and Internet Connections&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbaf1-132">4</span><span class="sxs-lookup"><span data-stu-id="fbaf1-132">4</span></span></td>
<td><span data-ttu-id="fbaf1-133">N'est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-133">No longer used.</span></span> <span data-ttu-id="fbaf1-134">Tout élément qui s’ajoute uniquement à la catégorie 4 apparaît dans la catégorie 2 (matériel et audio).</span><span class="sxs-lookup"><span data-stu-id="fbaf1-134">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="fbaf1-135">N'est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-135">No longer used.</span></span> <span data-ttu-id="fbaf1-136">Tout élément qui s’ajoute uniquement à la catégorie 4 apparaît dans la catégorie 2 (matériel et audio).</span><span class="sxs-lookup"><span data-stu-id="fbaf1-136">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="fbaf1-137">&quot;Sons, voix et périphériques audio&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-137">&quot;Sounds, Speech, and Audio Devices&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbaf1-138">5</span><span class="sxs-lookup"><span data-stu-id="fbaf1-138">5</span></span></td>
<td><span data-ttu-id="fbaf1-139">&quot;Système et sécurité&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-139">&quot;System and Security&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-140">&quot;Système et maintenance&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-140">&quot;System and Maintenance&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-141">&quot;Performances et maintenance&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-141">&quot;Performance and Maintenance&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbaf1-142">6</span><span class="sxs-lookup"><span data-stu-id="fbaf1-142">6</span></span></td>
<td><span data-ttu-id="fbaf1-143">&quot;Horloge, langue et région&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-143">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-144">&quot;Horloge, langue et région&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-144">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-145">&quot;Options de date, d’heure, de langue et régionales&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-145">&quot;Date, Time, Language, and Regional Options&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbaf1-146">7</span><span class="sxs-lookup"><span data-stu-id="fbaf1-146">7</span></span></td>
<td><span data-ttu-id="fbaf1-147">&quot;Options d’ergonomie&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-147">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-148">&quot;Options d’ergonomie&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-148">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-149">&quot;Options d’accessibilité&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-149">&quot;Accessibility Options&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbaf1-150">8</span><span class="sxs-lookup"><span data-stu-id="fbaf1-150">8</span></span></td>
<td><span data-ttu-id="fbaf1-151">&quot;Programmes&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-151">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-152">&quot;Programmes&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-152">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-153">&quot;Ajouter ou supprimer des programmes&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-153">&quot;Add or Remove Programs&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbaf1-154">9</span><span class="sxs-lookup"><span data-stu-id="fbaf1-154">9</span></span></td>
<td><span data-ttu-id="fbaf1-155">&quot;Comptes d’utilisateur&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-155">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fbaf1-156">Lorsque vous n’êtes pas connecté à un domaine, cela s’appelle &quot; comptes d’utilisateur et sécurité de famille &quot; .</span><span class="sxs-lookup"><span data-stu-id="fbaf1-156">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="fbaf1-157">&quot;Comptes d’utilisateur&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-157">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fbaf1-158">Lorsque vous n’êtes pas connecté à un domaine, cela s’appelle &quot; comptes d’utilisateur et sécurité de famille &quot; .</span><span class="sxs-lookup"><span data-stu-id="fbaf1-158">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="fbaf1-159">&quot;Comptes d’utilisateur&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-159">&quot;User Accounts&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbaf1-160">10</span><span class="sxs-lookup"><span data-stu-id="fbaf1-160">10</span></span></td>
<td><span data-ttu-id="fbaf1-161">N'est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-161">No longer used.</span></span> <span data-ttu-id="fbaf1-162">Les éléments inscrits dans cette catégorie s’affichent dans la catégorie 5 (système et sécurité).</span><span class="sxs-lookup"><span data-stu-id="fbaf1-162">Items registered in this category appear in category 5 (System and Security).</span></span></td>
<td><span data-ttu-id="fbaf1-163">&quot;Sécurité&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-163">&quot;Security&quot;</span></span></td>
<td><span data-ttu-id="fbaf1-164">&quot;Centre de sécurité&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-164">&quot;Security Center&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fbaf1-165">Disponible uniquement dans Windows XP Service Pack 2 (SP2) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-165">Available only in Windows XP Service Pack 2 (SP2) or later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbaf1-166">11</span><span class="sxs-lookup"><span data-stu-id="fbaf1-166">11</span></span></td>
<td><span data-ttu-id="fbaf1-167">N'est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-167">No longer used.</span></span> <span data-ttu-id="fbaf1-168">Les éléments inscrits dans cette catégorie s’affichent dans la catégorie 0 (tous les éléments du panneau de configuration).</span><span class="sxs-lookup"><span data-stu-id="fbaf1-168">Items registered in this category appear in category 0 (All Control Panel Items).</span></span></td>
<td><span data-ttu-id="fbaf1-169">&quot;ORDINATEUR portable&quot;</span><span class="sxs-lookup"><span data-stu-id="fbaf1-169">&quot;Mobile PC&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fbaf1-170">Cette catégorie est visible uniquement sur les ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-170">This category is only visible on mobile PCs.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="fbaf1-171">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-171">Not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fbaf1-172">Dans Windows XP, les catégories **Ajouter ou supprimer des programmes** et des **comptes d’utilisateur** fonctionnent différemment des autres catégories dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-172">In Windows XP, the categories **Add or Remove Programs** and **User Accounts** work somewhat differently from other categories in Control Panel.</span></span> <span data-ttu-id="fbaf1-173">Lorsqu’un ou plusieurs éléments sont ajoutés à l’une de ces deux catégories, le lien associé dans le panneau de configuration ouvre une page de catégorie.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-173">When one or more items are added to one of these two categories, the associated link in Control Panel opens a category page.</span></span> <span data-ttu-id="fbaf1-174">Les éléments inscrits s’affichent dans la partie inférieure de la page sous le titre « ou sélectionnent une icône du panneau de configuration ».</span><span class="sxs-lookup"><span data-stu-id="fbaf1-174">The registered items appear in the lower portion of the page under the heading "or Pick a Control Panel icon".</span></span> <span data-ttu-id="fbaf1-175">Quand aucun élément n’est inscrit pour l’une de ces catégories, le lien associé dans le panneau de configuration appelle directement l’élément Windows standard pour cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-175">When no items are registered for one of these categories, the associated link in Control Panel directly invokes the standard Windows item for that category.</span></span> <span data-ttu-id="fbaf1-176">Dans Windows Vista et versions ultérieures, la catégorie **programmes** et **compte d’utilisateur** n’a pas cette propriété.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-176">In Windows Vista and later, the **Programs** category and the **User Accounts** category do not have this property.</span></span>

<span data-ttu-id="fbaf1-177">La catégorie **Security Center** , disponible uniquement dans Windows XP SP2, est également un peu non standard.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-177">The **Security Center** category, available only in Windows XP SP2, is also somewhat non-standard.</span></span> <span data-ttu-id="fbaf1-178">Cliquez sur cette catégorie pour ouvrir la page **Security Center** dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-178">Clicking this category opens the **Security Center** page in a new window.</span></span> <span data-ttu-id="fbaf1-179">Les éléments inscrits pour **Security Center** s’affichent dans la partie inférieure de cette page sous le titre **gérer les paramètres de sécurité pour :**.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-179">Items registered for **Security Center** appear in the lower portion of that page under the heading **Manage security settings for:**.</span></span> <span data-ttu-id="fbaf1-180">Cliquer sur une icône ouvre l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="fbaf1-180">Clicking an icon opens the Control Panel item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbaf1-181">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fbaf1-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbaf1-182">Éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="fbaf1-182">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="fbaf1-183">Conseils sur l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="fbaf1-183">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="fbaf1-184">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="fbaf1-184">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="fbaf1-185">Utilisation de CPLApplet</span><span class="sxs-lookup"><span data-stu-id="fbaf1-185">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="fbaf1-186">Traitement des messages du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="fbaf1-186">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="fbaf1-187">Exécution des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="fbaf1-187">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="fbaf1-188">Extension des éléments du panneau de configuration système</span><span class="sxs-lookup"><span data-stu-id="fbaf1-188">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="fbaf1-189">Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="fbaf1-189">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="fbaf1-190">Accès au panneau de configuration en mode sans échec sous Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbaf1-190">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




