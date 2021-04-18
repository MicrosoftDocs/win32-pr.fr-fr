---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 2c796d5c-1556-4348-83e2-23e93780ebc1
title: Référencement des paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815ec7cd412e158a73e2b760f9f6080d7b0326a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106527052"
---
# <a name="referencing-parameters"></a><span data-ttu-id="11350-104">Référencement des paramètres</span><span class="sxs-lookup"><span data-stu-id="11350-104">Referencing Parameters</span></span>

<span data-ttu-id="11350-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="11350-105">This topic is not current.</span></span> <span data-ttu-id="11350-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="11350-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11350-107">L’option Personnaliser la taille du média est un exemple concret d’une option qui comprend un élément ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="11350-107">A concrete example of an Option that includes a ParameterRef element is the custom media size Option.</span></span> <span data-ttu-id="11350-108">Notez qu’il fait référence à deux paramètres : PageMediaSizeMediaSizeWidth et PageMediaSizeMediaSizeHeight.</span><span class="sxs-lookup"><span data-stu-id="11350-108">Note that it references two parameters: PageMediaSizeMediaSizeWidth and PageMediaSizeMediaSizeHeight.</span></span> <span data-ttu-id="11350-109">Chaque instance ParameterRef fait référence à une instance ParameterDef qui est définie ailleurs dans le document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="11350-109">Each ParameterRef instance refers to a ParameterDef instance that is defined elsewhere in the PrintCapabilities document.</span></span> <span data-ttu-id="11350-110">Pour plus d’informations sur l’élément ParameterDef, consultez [ParameterDef](parameterdef.md).</span><span class="sxs-lookup"><span data-stu-id="11350-110">For information about the ParameterDef element, see [ParameterDef](parameterdef.md).</span></span> <span data-ttu-id="11350-111">Pour obtenir des informations conceptuelles sur la définition des paramètres, consultez [ParameterDef et ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span><span class="sxs-lookup"><span data-stu-id="11350-111">For conceptual information about defining parameters, see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

``` syntax
<!--Example of ParamterRef usage within a Feature-->
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
</psf:Option>
```

<span data-ttu-id="11350-112">La simple création d’une option paramétrable n’est pas suffisante pour s’assurer que l’option sera gérée et traitée correctement.</span><span class="sxs-lookup"><span data-stu-id="11350-112">Merely creating a parameterized Option is not sufficient to ensure that the Option will be handled and processed correctly.</span></span> <span data-ttu-id="11350-113">Le fournisseur et les clients PrintCapabilities/PrintTicket doivent fournir une prise en charge supplémentaire pour implémenter correctement des instances d’option paramétrées.</span><span class="sxs-lookup"><span data-stu-id="11350-113">The PrintCapabilities/PrintTicket provider and clients must provide additional support to properly implement parameterized Option instances.</span></span> <span data-ttu-id="11350-114">Les comportements requis sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="11350-114">The required behaviors are described in the following sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11350-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11350-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11350-116">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="11350-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



