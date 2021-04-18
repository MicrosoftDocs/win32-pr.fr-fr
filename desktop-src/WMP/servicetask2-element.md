---
title: Élément ServiceTask2
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’élément ServiceTask2 représente le deuxième volet des tâches du magasin en ligne.
ms.assetid: f920ef25-efca-47c8-bcbc-2cb34593e879
keywords:
- Élément ServiceTask2 lecteur Windows Media
topic_type:
- apiref
api_name:
- ServiceTask2 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36052dabc1be7f2925f5185239faa602b8633fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540081"
---
# <a name="servicetask2-element"></a><span data-ttu-id="71a39-106">Élément ServiceTask2</span><span class="sxs-lookup"><span data-stu-id="71a39-106">ServiceTask2 Element</span></span>

> [!Note]  
> <span data-ttu-id="71a39-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="71a39-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="71a39-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="71a39-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="71a39-109">L’élément **ServiceTask2** représente le deuxième volet des tâches du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="71a39-109">The **ServiceTask2** element represents the second online store task pane.</span></span>

``` syntax
<ServiceTask2
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="71a39-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="71a39-110">Attributes</span></span>



| <span data-ttu-id="71a39-111">Terme</span><span class="sxs-lookup"><span data-stu-id="71a39-111">Term</span></span>                                                                                                                             | <span data-ttu-id="71a39-112">Description</span><span class="sxs-lookup"><span data-stu-id="71a39-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="71a39-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="71a39-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="71a39-114">URL de la page Web affichée par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="71a39-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="71a39-115">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="71a39-115">Parent/Child Elements</span></span>



| <span data-ttu-id="71a39-116">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="71a39-116">Hierarchy</span></span>       | <span data-ttu-id="71a39-117">Élément</span><span class="sxs-lookup"><span data-stu-id="71a39-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="71a39-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="71a39-118">Parent elements</span></span> | <span data-ttu-id="71a39-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="71a39-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="71a39-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="71a39-120">Child elements</span></span>  | <span data-ttu-id="71a39-121">**ButtonText**, **ButtonTip**</span><span class="sxs-lookup"><span data-stu-id="71a39-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="71a39-122">Notes</span><span class="sxs-lookup"><span data-stu-id="71a39-122">Remarks</span></span>

<span data-ttu-id="71a39-123">**ServiceTask1** est considéré comme le volet principal des tâches pour engager des activités commerciales.</span><span class="sxs-lookup"><span data-stu-id="71a39-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="71a39-124">Il s’agit du volet des tâches qui s’affiche lorsque l’utilisateur choisit d’acheter de la musique.</span><span class="sxs-lookup"><span data-stu-id="71a39-124">It is the task pane that displays when the user chooses to purchase music.</span></span> <span data-ttu-id="71a39-125">Utilisez **ServiceTask2** pour les autres activités du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="71a39-125">Use **ServiceTask2** for other online store activity.</span></span>

> [!Note]  
> <span data-ttu-id="71a39-126">Le lecteur Windows Media 10 comporte trois volets de tâches où un magasin en ligne peut afficher ses pages Web.</span><span class="sxs-lookup"><span data-stu-id="71a39-126">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="71a39-127">Le magasin en ligne peut choisir d’utiliser un, deux ou les trois volets de tâches.</span><span class="sxs-lookup"><span data-stu-id="71a39-127">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="71a39-128">Le lecteur Windows Media 11 n’a qu’un seul volet de tâches, que l’utilisateur peut afficher en cliquant sur l’onglet **magasins en ligne** . le lecteur Windows Media 11 ignore les éléments **ServiceTask2** et **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="71a39-128">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="71a39-129">Les volets des tâches magasins en ligne partagent une seule instance de navigateur.</span><span class="sxs-lookup"><span data-stu-id="71a39-129">Online stores task panes share a single browser instance.</span></span> <span data-ttu-id="71a39-130">Cela signifie que vous ne devez pas écrire de code de script dans votre page Web que vous prévoyez de continuer à exécuter quand l’utilisateur quitte la tâche de service actuelle.</span><span class="sxs-lookup"><span data-stu-id="71a39-130">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="71a39-131">Lorsque l’utilisateur bascule les volets de tâches, le lecteur Windows Media stocke les cookies d’URL et de session.</span><span class="sxs-lookup"><span data-stu-id="71a39-131">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="71a39-132">Lorsque l’utilisateur revient au volet de tâches, le lecteur restaure l’URL et les cookies.</span><span class="sxs-lookup"><span data-stu-id="71a39-132">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="71a39-133">Si l’utilisateur choisit d’utiliser un autre magasin en ligne, l’URL et les données de session sont effacées.</span><span class="sxs-lookup"><span data-stu-id="71a39-133">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="71a39-134">Le tableau suivant détaille les paramètres envoyés avec la demande d’URL.</span><span class="sxs-lookup"><span data-stu-id="71a39-134">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="71a39-135">D’autres peuvent être présents à des fins de compatibilité héritée.</span><span class="sxs-lookup"><span data-stu-id="71a39-135">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="71a39-136">Nom</span><span class="sxs-lookup"><span data-stu-id="71a39-136">Name</span></span>         | <span data-ttu-id="71a39-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="71a39-137">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a39-138">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="71a39-138">*geoid*</span></span>      | <span data-ttu-id="71a39-139">ID d’emplacement géographique Windows.</span><span class="sxs-lookup"><span data-stu-id="71a39-139">Windows geographical location ID.</span></span> <span data-ttu-id="71a39-140">L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="71a39-140">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="71a39-141">*locale*</span><span class="sxs-lookup"><span data-stu-id="71a39-141">*locale*</span></span>     | <span data-ttu-id="71a39-142">ID de paramètres régionaux du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="71a39-142">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="71a39-143">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="71a39-143">*userlocale*</span></span> | <span data-ttu-id="71a39-144">ID de paramètres régionaux Windows.</span><span class="sxs-lookup"><span data-stu-id="71a39-144">Windows locale ID.</span></span> <span data-ttu-id="71a39-145">Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="71a39-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="71a39-146">*version*</span><span class="sxs-lookup"><span data-stu-id="71a39-146">*version*</span></span>    | <span data-ttu-id="71a39-147">Numéro de version du lecteur Windows Media en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="71a39-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="71a39-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71a39-148">Requirements</span></span>



| <span data-ttu-id="71a39-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71a39-149">Requirement</span></span> | <span data-ttu-id="71a39-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="71a39-150">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="71a39-151">Version</span><span class="sxs-lookup"><span data-stu-id="71a39-151">Version</span></span><br/> | <span data-ttu-id="71a39-152">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="71a39-152">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71a39-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71a39-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a39-154">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="71a39-154">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="71a39-155">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="71a39-155">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="71a39-156">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="71a39-156">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





