---
description: Le terme FORMSOF effectue des correspondances à l’aide d’autres formes linguistiques du mot.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Terme FORMSOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512940"
---
# <a name="formsof-term"></a><span data-ttu-id="8474b-103">Terme FORMSOF</span><span class="sxs-lookup"><span data-stu-id="8474b-103">FORMSOF Term</span></span>

<span data-ttu-id="8474b-104">Le terme FORMSOF effectue des correspondances à l’aide d’autres formes linguistiques du mot.</span><span class="sxs-lookup"><span data-stu-id="8474b-104">The FORMSOF term performs matches using other linguistic forms of the word.</span></span> <span data-ttu-id="8474b-105">Voici la syntaxe du terme FORMSOF :</span><span class="sxs-lookup"><span data-stu-id="8474b-105">The following is the FORMSOF term syntax:</span></span>


```
FORMSOF (<generation_type>,<match_words>)
```



<span data-ttu-id="8474b-106">Le type de génération spécifie la manière dont Microsoft Windows Search choisit les autres formes de mots.</span><span class="sxs-lookup"><span data-stu-id="8474b-106">The generation type specifies how Microsoft Windows Search chooses the alternative word forms.</span></span> <span data-ttu-id="8474b-107">La valeur **fléchie** choisit d’autres formes fléchies pour les mots de correspondance.</span><span class="sxs-lookup"><span data-stu-id="8474b-107">The **INFLECTIONAL** value chooses alternative inflection forms for the match words.</span></span> <span data-ttu-id="8474b-108">Si le mot est un verbe, d’autres dizaines sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="8474b-108">If the word is a verb, alternative tenses are used.</span></span> <span data-ttu-id="8474b-109">Si le mot est un substantif, les formes singulières, plurielles et de possession sont utilisées pour détecter les correspondances.</span><span class="sxs-lookup"><span data-stu-id="8474b-109">If the word is a noun, the singular, plural, and possessive forms are used to detect matches.</span></span>

<span data-ttu-id="8474b-110">La valeur de correspondance des \_ mots correspond à un ou plusieurs mots, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="8474b-110">The match\_words value is one or more words, separated by commas.</span></span>

## <a name="examples"></a><span data-ttu-id="8474b-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="8474b-111">Examples</span></span>

<span data-ttu-id="8474b-112">L’exemple suivant recherche des correspondances fléchies pour le mot « Run ».</span><span class="sxs-lookup"><span data-stu-id="8474b-112">The following example searches for inflectional matches for the word "run".</span></span> <span data-ttu-id="8474b-113">Cet exemple correspond à des documents contenant « exécuter », « en cours d’exécution » ou « exécuté ».</span><span class="sxs-lookup"><span data-stu-id="8474b-113">This example matches documents containing "run", "running", or "ran".</span></span>


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a><span data-ttu-id="8474b-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8474b-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8474b-115">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="8474b-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8474b-116">Prédicat FREETEXT</span><span class="sxs-lookup"><span data-stu-id="8474b-116">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="8474b-117">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="8474b-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



