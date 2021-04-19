---
description: La plateforme Tablet PC prend en charge un certain nombre de Factoids qui sont utilisés pour augmenter la précision de la reconnaissance.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factoids pris en charge à partir de la version 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532302"
---
# <a name="supported-factoids-from-version-1"></a><span data-ttu-id="d475b-103">Factoids pris en charge à partir de la version 1</span><span class="sxs-lookup"><span data-stu-id="d475b-103">Supported Factoids from Version 1</span></span>

<span data-ttu-id="d475b-104">\[Notez que la description suivante du Factoids pris en charge dans la version 1 du kit de développement logiciel (SDK) de Microsoft Windows XP Tablet PC Edition est toujours prise en charge par les module de reconnaissance, mais il est recommandé que tout nouveau développement (pour les logiciels de reconnaissance du script latin) utilise les valeurs définies dans l’énumération [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) .\]</span><span class="sxs-lookup"><span data-stu-id="d475b-104">\[Note the following description of the factoids supported in version 1 of the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) are still supported by recognizers, but it is recommended that all new development (for recognizers of Latin script) use the values defined in the [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration.\]</span></span>

<span data-ttu-id="d475b-105">La plateforme Tablet PC prend en charge un certain nombre de Factoids qui sont utilisés pour augmenter la précision de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="d475b-105">The Tablet PC Platform supports a number of factoids that are used to increase recognition accuracy.</span></span> <span data-ttu-id="d475b-106">Lors de l’utilisation de Factoids, il est important que l’entrée attendue corresponde exactement à la définition du Factoid.</span><span class="sxs-lookup"><span data-stu-id="d475b-106">When using factoids, it is important that the expected input exactly match the definition of the factoid.</span></span> <span data-ttu-id="d475b-107">Si l’entrée ne correspond pas à la définition du Factoid, la précision de la reconnaissance en souffre.</span><span class="sxs-lookup"><span data-stu-id="d475b-107">If the input does not match the definition of the factoid, recognition accuracy suffers.</span></span> <span data-ttu-id="d475b-108">Par exemple, si le **nombre** Factoid est défini et que l’utilisateur entre des lettres, la précision de la reconnaissance pour les lettres est médiocre.</span><span class="sxs-lookup"><span data-stu-id="d475b-108">For example, if the **Number** factoid is set and the user enters letters, the recognition accuracy for letters is poor.</span></span>

<span data-ttu-id="d475b-109">Certaines Factoids, telles que la **messagerie électronique** et les **chiffres**, sont presque identiques d’un langage à l’autre.</span><span class="sxs-lookup"><span data-stu-id="d475b-109">Certain factoids, such as **Email** and **Digit**, are almost identical across languages.</span></span> <span data-ttu-id="d475b-110">D’autres Factoids, tels que **Telephone** et **PostalCode**, varient selon la langue.</span><span class="sxs-lookup"><span data-stu-id="d475b-110">Other factoids, such as **Telephone** and **PostalCode**, vary by language.</span></span> <span data-ttu-id="d475b-111">Examinez le format de chaque Factoid pour la langue que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="d475b-111">Examine the format of each factoid for the language that you are using.</span></span> <span data-ttu-id="d475b-112">Vous trouverez une liste de formats pour chaque Factoid dans chaque langue dans les tableaux des rubriques qui suivent cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d475b-112">A list of formats for each factoid in each language can be found in the tables in the topics following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="d475b-113">Il existe une distinction subtile mais importante entre Factoids pour les langues occidentales et Factoids pour les langues d’Extrême-Orient.</span><span class="sxs-lookup"><span data-stu-id="d475b-113">There is a subtle but important distinction between factoids for western languages and factoids for East Asian languages.</span></span> <span data-ttu-id="d475b-114">Les Factoids pour les langues occidentales sont implémentées à l’aide d’expressions qui décrivent le résultat souhaité.</span><span class="sxs-lookup"><span data-stu-id="d475b-114">Factoids for western languages are implemented by using expressions that describe the desired result.</span></span> <span data-ttu-id="d475b-115">Le module de reconnaissance est ensuite biaisé pour produire des résultats qui correspondent à cette expression.</span><span class="sxs-lookup"><span data-stu-id="d475b-115">The recognizer is then biased to produce results that match this expression.</span></span> <span data-ttu-id="d475b-116">Factoids pour les langues d’Extrême-Orient sont implémentées en spécifiant une plage acceptable de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="d475b-116">Factoids for East Asian languages are implemented by specifying an acceptable range of Unicode characters.</span></span> <span data-ttu-id="d475b-117">Par exemple, la **Date** Factoid pour les langues d’Asie orientale accepte uniquement les caractères Unicode dans une certaine plage.</span><span class="sxs-lookup"><span data-stu-id="d475b-117">For example, the **Date** factoid for East Asian languages accepts only Unicode characters within a certain range.</span></span>

 

<span data-ttu-id="d475b-118">Factoids pour les langues occidentales inclut Factoids pour l’anglais (Royaume-Uni), l’anglais (États-Unis), le français, l’allemand et l’espagnol.</span><span class="sxs-lookup"><span data-stu-id="d475b-118">Factoids for western languages include factoids for English (United Kingdom), English (United States), French, German, and Spanish.</span></span> <span data-ttu-id="d475b-119">Factoids pour les langues d’Extrême-Orient incluent Factoids pour le chinois (simplifié), le chinois (traditionnel), le japonais et le coréen.</span><span class="sxs-lookup"><span data-stu-id="d475b-119">Factoids for East Asian languages include factoids for Chinese (Simplified), Chinese (Traditional), Japanese, and Korean.</span></span>

<span data-ttu-id="d475b-120">Les sections suivantes présentent les formats pris en charge pour chaque Factoid dans chaque langue :</span><span class="sxs-lookup"><span data-stu-id="d475b-120">The following sections show the formats supported for each factoid in each language:</span></span>

-   [<span data-ttu-id="d475b-121">Factoids commun dans plusieurs langues</span><span class="sxs-lookup"><span data-stu-id="d475b-121">Factoids Common Across Languages</span></span>](factoids-common-across-languages.md)
-   [<span data-ttu-id="d475b-122">Factoids pour les langues occidentales</span><span class="sxs-lookup"><span data-stu-id="d475b-122">Factoids for Western Languages</span></span>](factoids-for-western-languages.md)
-   [<span data-ttu-id="d475b-123">Factoids pour les langues d’Extrême-Orient</span><span class="sxs-lookup"><span data-stu-id="d475b-123">Factoids for East Asian Languages</span></span>](factoids-for-east-asian-languages.md)

<span data-ttu-id="d475b-124">Si vous prévoyez une entrée différente des formats énumérés dans les tableaux de ces sections, n’utilisez pas de Factoid.</span><span class="sxs-lookup"><span data-stu-id="d475b-124">If you expect input that is different from the formats listed in the tables in these sections, do not use a factoid.</span></span> <span data-ttu-id="d475b-125">En outre, les Factoids sont intégrés dans le module de reconnaissance pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="d475b-125">In addition, factoids are built into the recognizer for each language.</span></span> <span data-ttu-id="d475b-126">Vous ne pouvez pas utiliser Factoids dans une langue avec un module de reconnaissance d’une autre langue.</span><span class="sxs-lookup"><span data-stu-id="d475b-126">You cannot use factoids from one language with a recognizer from another language.</span></span> <span data-ttu-id="d475b-127">Par exemple, vous ne pouvez pas utiliser le Factoid **téléphonique** français avec un module de reconnaissance japonais.</span><span class="sxs-lookup"><span data-stu-id="d475b-127">For example, you cannot use the French **Telephone** factoid with a Japanese recognizer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d475b-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d475b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d475b-129">**Constantes Factoid**</span><span class="sxs-lookup"><span data-stu-id="d475b-129">**Factoid Constants**</span></span>](factoid-constants.md)
</dt> <dt>

<span data-ttu-id="d475b-130">[Classe Microsoft. Ink. Factoid](/previous-versions/ms583657(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="d475b-130">[Microsoft.Ink.Factoid Class](/previous-versions/ms583657(v=vs.100))</span></span>
</dt> </dl>

 

 
