---
description: Représentent des attributs en tant que constructions feature/option ou en tant que paramètres. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Représentation des attributs en tant que constructions feature/option ou en tant que paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120054"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="e0cee-105">Représentation des attributs en tant que constructions feature/option ou en tant que paramètres</span><span class="sxs-lookup"><span data-stu-id="e0cee-105">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="e0cee-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e0cee-106">This topic is not current.</span></span> <span data-ttu-id="e0cee-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e0cee-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e0cee-108">L’auteur d’un document PrintCapabilities définit les attributs de l’appareil qui composent la configuration.</span><span class="sxs-lookup"><span data-stu-id="e0cee-108">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="e0cee-109">Dans le document PrintCapabilities, l’auteur peut choisir de représenter un attribut d’appareil en tant que construction fonctionnalité/option ou en tant que construction de paramètre.</span><span class="sxs-lookup"><span data-stu-id="e0cee-109">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="e0cee-110">Si un attribut d’appareil a un nombre relativement faible d’États possibles qui ne sont pas classés dans un modèle évident, une construction fonctionnalité/option est généralement le meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="e0cee-110">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="e0cee-111">Par exemple, si les valeurs autorisées pour l’attribut d’appareil PageMediaSize sont les valeurs letter, Legal, A4ISO, tabloïd et Envelope10, une fonctionnalité/option est le meilleur choix pour la représentation.</span><span class="sxs-lookup"><span data-stu-id="e0cee-111">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="e0cee-112">En raison de la difficulté et de l’ambiguïté associées à l’expression des valeurs autorisées sans énumération explicite, la construction de paramètre n’est pas appropriée pour l’attribut PageMediaSize.</span><span class="sxs-lookup"><span data-stu-id="e0cee-112">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="e0cee-113">Si un attribut d’appareil peut être représenté par une plage d’entiers, la représentation des paramètres est généralement le meilleur choix, en particulier pour les plages qui incluent de nombreuses valeurs.</span><span class="sxs-lookup"><span data-stu-id="e0cee-113">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="e0cee-114">Par exemple, si l’attribut d’appareil CopyCount pour un modèle d’imprimante donné peut être compris entre 1 et 99 999, cet attribut doit être catégorisé comme paramètre, en définissant une instance ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="e0cee-114">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="e0cee-115">Assignez des valeurs aux instances de propriété standard MinValue et MaxValue de l’élément ParameterDef pour définir la plage de valeurs de l’attribut JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="e0cee-115">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="e0cee-116">En raison du grand nombre de valeurs qui doivent être explicitement listées en tant qu’éléments option, la représentation fonctionnalité/option n’est pas appropriée pour l’attribut d’appareil JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="e0cee-116">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0cee-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0cee-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0cee-118">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="e0cee-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



