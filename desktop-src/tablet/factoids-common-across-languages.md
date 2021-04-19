---
description: Un certain nombre de Factoids décrivent les entrées communes à tous les moduleurs de langage et n’ont pas besoin d’avoir des formats différents pour des langues différentes. Le tableau suivant répertorie les Factoids qui sont communs à tous les langages.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids commun dans plusieurs langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530837"
---
# <a name="factoids-common-across-languages"></a><span data-ttu-id="8cb41-104">Factoids commun dans plusieurs langues</span><span class="sxs-lookup"><span data-stu-id="8cb41-104">Factoids Common Across Languages</span></span>

<span data-ttu-id="8cb41-105">Un certain nombre de Factoids décrivent les entrées communes à tous les moduleurs de langage et n’ont pas besoin d’avoir des formats différents pour des langues différentes.</span><span class="sxs-lookup"><span data-stu-id="8cb41-105">A number of factoids describe input that is common to all language recognizers and need not have different formats for different languages.</span></span> <span data-ttu-id="8cb41-106">Le tableau suivant répertorie les Factoids qui sont communs à tous les langages.</span><span class="sxs-lookup"><span data-stu-id="8cb41-106">The following table lists factoids that are common across all languages.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8cb41-107">Factoid</span><span class="sxs-lookup"><span data-stu-id="8cb41-107">Factoid</span></span></th>
<th><span data-ttu-id="8cb41-108">Définition</span><span class="sxs-lookup"><span data-stu-id="8cb41-108">Definition</span></span></th>
<th><span data-ttu-id="8cb41-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="8cb41-109">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cb41-110"><strong>Caractères</strong></span><span class="sxs-lookup"><span data-stu-id="8cb41-110"><strong>Digit</strong></span></span></td>
<td><span data-ttu-id="8cb41-111">Définit le décalage pour un chiffre unique.</span><span class="sxs-lookup"><span data-stu-id="8cb41-111">Sets bias for a single digit.</span></span> <span data-ttu-id="8cb41-112">Le module de reconnaissance est biaisé pour retourner uniquement des chiffres quand ce Factoid est défini.</span><span class="sxs-lookup"><span data-stu-id="8cb41-112">The recognizer is biased toward returning only single digits when this factoid is set.</span></span><br/></td>
<td><span data-ttu-id="8cb41-113">0-9</span><span class="sxs-lookup"><span data-stu-id="8cb41-113">0-9</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cb41-114"><strong>E-mail</strong></span><span class="sxs-lookup"><span data-stu-id="8cb41-114"><strong>Email</strong></span></span></td>
<td><span data-ttu-id="8cb41-115">Définit le décalage pour une adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="8cb41-115">Sets bias for an email address.</span></span><br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cb41-116"><strong>Web</strong></span><span class="sxs-lookup"><span data-stu-id="8cb41-116"><strong>Web</strong></span></span></td>
<td><span data-ttu-id="8cb41-117">Définit le décalage pour différents formats d’URL.</span><span class="sxs-lookup"><span data-stu-id="8cb41-117">Sets bias for various URL formats.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8cb41-118">Les paramètres par défaut pour le module de reconnaissance incluent le Factoid <strong>Web</strong> .</span><span class="sxs-lookup"><span data-stu-id="8cb41-118">The default settings for the recognizer include the <strong>Web</strong> factoid.</span></span> <span data-ttu-id="8cb41-119">Pour cette raison, vous ne pouvez pas remarquer une différence importante entre le Factoid <strong>Web</strong> et le paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="8cb41-119">Because of this, you may not notice a large difference between the <strong>Web</strong> factoid and the default setting.</span></span> <span data-ttu-id="8cb41-120">Toutefois, le Factoid <strong>Web</strong> permet d’éliminer les espaces entre les mots d’une URL.</span><span class="sxs-lookup"><span data-stu-id="8cb41-120">However, the <strong>Web</strong> factoid does help eliminate spaces between words in a URL.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="8cb41-121">http : \\ Microsoft.net</span><span class="sxs-lookup"><span data-stu-id="8cb41-121">http:\\microsoft.net</span></span><br/> https://microsoft.us/<br/> <span data-ttu-id="8cb41-122">https : \\ www.Microsoft.au </span><span class="sxs-lookup"><span data-stu-id="8cb41-122">https:\\www.microsoft.au</span></span>\<br/> https://microsoft.com<br/> <span data-ttu-id="8cb41-123">www.microsoft_world. com</span><span class="sxs-lookup"><span data-stu-id="8cb41-123">www.microsoft_world.com</span></span><br/> <span data-ttu-id="8cb41-124">www.microsoft.us </span><span class="sxs-lookup"><span data-stu-id="8cb41-124">www.microsoft.us</span></span>\<br/> <span data-ttu-id="8cb41-125">http : \\www.microsoft.com\myfile.htm</span><span class="sxs-lookup"><span data-stu-id="8cb41-125">http:\\www.microsoft.com\myfile.htm</span></span><br/> <span data-ttu-id="8cb41-126">http : \\www.microsoft.com\myfile.html</span><span class="sxs-lookup"><span data-stu-id="8cb41-126">http:\\www.microsoft.com\myfile.html</span></span><br/> <span data-ttu-id="8cb41-127">http : \\ www. Microsoft. com\myfile.asp</span><span class="sxs-lookup"><span data-stu-id="8cb41-127">http:\\www.microsoft.com\myfile.asp</span></span><br/> <span data-ttu-id="8cb41-128">http : \\ www.Microsoft.uk</span><span class="sxs-lookup"><span data-stu-id="8cb41-128">http:\\www.microsoft.uk</span></span><br/> <span data-ttu-id="8cb41-129">http : \\ www.Microsoft.info</span><span class="sxs-lookup"><span data-stu-id="8cb41-129">http:\\www.microsoft.info</span></span><br/> <span data-ttu-id="8cb41-130">www.microsoft.biz</span><span class="sxs-lookup"><span data-stu-id="8cb41-130">www.microsoft.biz</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cb41-131"><strong>Par défaut</strong></span><span class="sxs-lookup"><span data-stu-id="8cb41-131"><strong>Default</strong></span></span></td>
<td><span data-ttu-id="8cb41-132">Retourne le module de reconnaissance à ses paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="8cb41-132">Returns the recognizer to its default settings.</span></span><br/></td>
<td><span data-ttu-id="8cb41-133">Le paramètre par défaut pour Factoids pour les langues occidentales comprend le dictionnaire système, le dictionnaire de l’utilisateur, les différents signes de ponctuation et le <strong>Web</strong> et le <strong>numéro</strong> Factoids.</span><span class="sxs-lookup"><span data-stu-id="8cb41-133">The default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the <strong>Web</strong> and <strong>Number</strong> factoids.</span></span><br/> <span data-ttu-id="8cb41-134">Le paramètre par défaut pour Factoids pour les langues d’Extrême-Orient comprend tous les caractères pris en charge par le module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="8cb41-134">The default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cb41-135"><strong>Aucun</strong></span><span class="sxs-lookup"><span data-stu-id="8cb41-135"><strong>None</strong></span></span></td>
<td><span data-ttu-id="8cb41-136">Désactive tous les Factoids, les dictionnaires et le modèle de langue.</span><span class="sxs-lookup"><span data-stu-id="8cb41-136">Disables all factoids, dictionaries, and the language model.</span></span><br/></td>
<td><span data-ttu-id="8cb41-137">Ce Factoid doit être utilisé uniquement lorsque vous ne voulez pas que le module de reconnaissance utilise des règles grammaticales ou des dictionnaires, y compris le dictionnaire système.</span><span class="sxs-lookup"><span data-stu-id="8cb41-137">This factoid should be used only when you do not want the recognizer to use any grammar rules or dictionaries, including the system dictionary.</span></span> <span data-ttu-id="8cb41-138">Ce Factoid est utile pour l’entrée de chaînes aléatoires, telles que les codes de produit.</span><span class="sxs-lookup"><span data-stu-id="8cb41-138">This factoid is useful for input of random strings such as product codes.</span></span> <span data-ttu-id="8cb41-139">N’utilisez pas l’indicateur de forçage avec ce Factoid.</span><span class="sxs-lookup"><span data-stu-id="8cb41-139">Do not use the Coerce flag with this factoid.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




