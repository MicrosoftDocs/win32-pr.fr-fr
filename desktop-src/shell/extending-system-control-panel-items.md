---
description: Certains des éléments système trouvés dans le panneau de configuration sont extensibles. Pour installer une extension du panneau de configuration, inscrivez votre extension de Shell comme suit, où nom est le nom prédéfini de l’élément système (voir le tableau ci-dessous).
title: Extension des éléments du panneau de configuration système
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991157"
---
# <a name="extending-system-control-panel-items"></a><span data-ttu-id="75178-104">Extension des éléments du panneau de configuration système</span><span class="sxs-lookup"><span data-stu-id="75178-104">Extending System Control Panel Items</span></span>

<span data-ttu-id="75178-105">Certains des éléments système trouvés dans le panneau de configuration sont extensibles.</span><span class="sxs-lookup"><span data-stu-id="75178-105">Some of the system items found in the Control Panel are extensible.</span></span> <span data-ttu-id="75178-106">Pour installer une extension du panneau de configuration, inscrivez votre extension de Shell comme suit, où *nom* est le nom prédéfini de l’élément système (voir le tableau ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="75178-106">To install a Control Panel extension, register your Shell extension as follows, where *name* is the predefined name of the system item (see table below).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

<span data-ttu-id="75178-107">Cela est similaire à la façon dont vous inscrivez une extension pour un objet Shell prédéfini.</span><span class="sxs-lookup"><span data-stu-id="75178-107">This is similar to the way you would register an extension for a predefined Shell object.</span></span> <span data-ttu-id="75178-108">Étant donné que les seules extensions d’environnement prises en charge par les éléments du panneau de configuration sont des feuilles de propriétés, l’inscription doit se trouver sous la \\ sous-clé shellex **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="75178-108">Because the only Shell extensions supported by Control Panel items are property sheets, the registration must be under the **shellex**\\**PropertySheetHandlers** subkey.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75178-109">Élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="75178-109">Control Panel item</span></span></th>
<th><span data-ttu-id="75178-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="75178-110"><em>name</em></span></span></th>
<th><span data-ttu-id="75178-111">Notes</span><span class="sxs-lookup"><span data-stu-id="75178-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75178-112">Afficher</span><span class="sxs-lookup"><span data-stu-id="75178-112">Display</span></span></td>
<td><span data-ttu-id="75178-113">Bureau</span><span class="sxs-lookup"><span data-stu-id="75178-113">Desk</span></span></td>
<td><span data-ttu-id="75178-114">Prend également en charge le remplacement de la page du <strong>Bureau</strong> .</span><span class="sxs-lookup"><span data-stu-id="75178-114">Also supports replacement of the <strong>Desktop</strong> page.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="75178-115">Cela n’est plus pris en charge sous Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="75178-115">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75178-116">Paramètres d’affichage avancés</span><span class="sxs-lookup"><span data-stu-id="75178-116">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="75178-117">Appareil</span><span class="sxs-lookup"><span data-stu-id="75178-117">Device</span></span></td>
<td><span data-ttu-id="75178-118">Propriétés avancées spécifiques au non-hardisme.</span><span class="sxs-lookup"><span data-stu-id="75178-118">Nonhardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="75178-119">Cela n’est plus pris en charge sous Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="75178-119">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75178-120">Paramètres d’affichage avancés</span><span class="sxs-lookup"><span data-stu-id="75178-120">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="75178-121">Afficher</span><span class="sxs-lookup"><span data-stu-id="75178-121">Display</span></span></td>
<td><span data-ttu-id="75178-122">Propriétés avancées spécifiques au matériel.</span><span class="sxs-lookup"><span data-stu-id="75178-122">Hardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="75178-123">Cela n’est plus pris en charge sous Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="75178-123">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75178-124">Options Internet</span><span class="sxs-lookup"><span data-stu-id="75178-124">Internet Options</span></span></td>
<td><span data-ttu-id="75178-125">Internet</span><span class="sxs-lookup"><span data-stu-id="75178-125">Internet</span></span></td>
<td><span data-ttu-id="75178-126">Le nombre maximal de pages d’extension est 18.</span><span class="sxs-lookup"><span data-stu-id="75178-126">The maximum number of extension pages is 18.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75178-127">Clavier</span><span class="sxs-lookup"><span data-stu-id="75178-127">Keyboard</span></span></td>
<td><span data-ttu-id="75178-128">Clavier</span><span class="sxs-lookup"><span data-stu-id="75178-128">Keyboard</span></span></td>
<td><span data-ttu-id="75178-129">Le nombre maximal de pages d’extension est de 30.</span><span class="sxs-lookup"><span data-stu-id="75178-129">The maximum number of extension pages is 30.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75178-130">Souris</span><span class="sxs-lookup"><span data-stu-id="75178-130">Mouse</span></span></td>
<td><span data-ttu-id="75178-131">Souris</span><span class="sxs-lookup"><span data-stu-id="75178-131">Mouse</span></span></td>
<td><span data-ttu-id="75178-132">Prend également en charge le remplacement des pages standard.</span><span class="sxs-lookup"><span data-stu-id="75178-132">Also supports replacement of standard pages.</span></span> <span data-ttu-id="75178-133">Le nombre maximal de pages d’extension est de 8.</span><span class="sxs-lookup"><span data-stu-id="75178-133">The maximum number of extension pages is 8.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75178-134">Options d’alimentation</span><span class="sxs-lookup"><span data-stu-id="75178-134">Power Options</span></span></td>
<td><span data-ttu-id="75178-135">Power</span><span class="sxs-lookup"><span data-stu-id="75178-135">Power</span></span></td>
<td><span data-ttu-id="75178-136">Le nombre maximal de pages, y compris les pages standard, est 18.</span><span class="sxs-lookup"><span data-stu-id="75178-136">The maximum number of pages, including standard pages, is 18.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75178-137">Système</span><span class="sxs-lookup"><span data-stu-id="75178-137">System</span></span></td>
<td><span data-ttu-id="75178-138">Système</span><span class="sxs-lookup"><span data-stu-id="75178-138">System</span></span></td>
<td><span data-ttu-id="75178-139">Le nombre maximal de pages d’extension est de 8.</span><span class="sxs-lookup"><span data-stu-id="75178-139">The maximum number of extension pages is 8.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="75178-140">Cela n’est plus pris en charge sous Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="75178-140">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="75178-141">L’élément **Ajout/suppression de programmes** du panneau de configuration de Windows XP n’est pas une feuille de propriétés et ne peut donc pas être étendu par les méthodes présentées ici.</span><span class="sxs-lookup"><span data-stu-id="75178-141">The **Add or Remove Programs** item in the Windows XP Control Panel is not a property sheet and therefore cannot be extended by the methods discussed here.</span></span> <span data-ttu-id="75178-142">Au lieu de cela, son contenu est obtenu à partir des éditeurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="75178-142">Instead, its content is obtained from application publishers.</span></span> <span data-ttu-id="75178-143">Pour plus d’informations sur l’ajout de contenu à l' **Ajout ou** à la suppression de programmes, consultez [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)et [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span><span class="sxs-lookup"><span data-stu-id="75178-143">For more information on adding content to **Add or Remove Programs**, see [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps), and [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75178-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75178-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75178-145">Éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="75178-145">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="75178-146">Conseils sur l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="75178-146">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="75178-147">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="75178-147">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="75178-148">Utilisation de CPLApplet</span><span class="sxs-lookup"><span data-stu-id="75178-148">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="75178-149">Traitement des messages du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="75178-149">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="75178-150">Exécution des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="75178-150">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="75178-151">Affectation des catégories du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="75178-151">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="75178-152">Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="75178-152">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="75178-153">Accès au panneau de configuration en mode sans échec sous Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75178-153">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




