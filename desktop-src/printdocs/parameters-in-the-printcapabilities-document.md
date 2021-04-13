---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Paramètres dans le document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321709"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="58208-104">Paramètres dans le document PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="58208-104">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="58208-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="58208-105">This topic is not current.</span></span> <span data-ttu-id="58208-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="58208-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="58208-107">Comme indiqué dans [éléments de référence de paramètre](parameter-reference-elements.md), les éléments ParameterInit peuvent être référencés à partir d’instances d’option, mais la construction de paramètre a également une utilisation indépendante de ce type d’élément.</span><span class="sxs-lookup"><span data-stu-id="58208-107">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="58208-108">CopyCount est un exemple d’attribut de configuration d’appareil adapté à la représentation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="58208-108">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="58208-109">Les valeurs autorisées pour cet attribut de configuration de périphérique peuvent être définies facilement et de façon concise sans répertorier chacune d’elles de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="58208-109">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="58208-110">Bien qu’il soit possible, bien que fastidieux, de répertorier chaque valeur CopyCount dans sa propre option, certains attributs de configuration de l’appareil ne peuvent pas être représentés à l’aide d’une construction fonctionnalité/option.</span><span class="sxs-lookup"><span data-stu-id="58208-110">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="58208-111">Par exemple, imaginez un appareil qui accepte une chaîne de texte qui est ensuite utilisée pour produire un filigrane virtuel sur chaque page de sortie.</span><span class="sxs-lookup"><span data-stu-id="58208-111">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="58208-112">L’ensemble de toutes les chaînes de texte possibles ne peut pas être facilement énuméré, mais la chaîne de texte peut facilement être décrite à l’aide d’un élément ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="58208-112">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="58208-113">Le document des mots clés du schéma d’impression définit un certain nombre de constructions de paramètres couramment utilisées, mais les fournisseurs PrintCapabilities sont libres de définir des éléments supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="58208-113">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="58208-114">Toutefois, ces constructions de paramètres définies de manière privée ne sont pas portables vers d’autres appareils, en raison du fait qu’un document PrintCapabilities fourni par une autre partie ne définit pas une telle construction de paramètre.</span><span class="sxs-lookup"><span data-stu-id="58208-114">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="58208-115">Que la définition d’un schéma ou d’une définition privée soit définie, l’instance ParameterDef doit être présente dans le document PrintCapabilities avant que le paramètre soit reconnu et utilisé par les clients.</span><span class="sxs-lookup"><span data-stu-id="58208-115">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="58208-116">Ces paramètres sont appelés *paramètres désignés*.</span><span class="sxs-lookup"><span data-stu-id="58208-116">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58208-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58208-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58208-118">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="58208-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



