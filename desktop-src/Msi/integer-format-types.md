---
description: Les types de format entier des données configurables peuvent être utilisés dans des champs de base de données de type texte ou entier. L’attribut msmConfigItemNonNullable est implicite dans ce format de données et n’a pas besoin d’être défini. NULL n’est jamais une valeur valide pour ce type.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Types de format d’entier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757035"
---
# <a name="integer-format-types"></a><span data-ttu-id="d760d-105">Types de format d’entier</span><span class="sxs-lookup"><span data-stu-id="d760d-105">Integer Format Types</span></span>

<span data-ttu-id="d760d-106">Les types de format entier des données configurables peuvent être utilisés dans des champs de base de données de type texte ou entier.</span><span class="sxs-lookup"><span data-stu-id="d760d-106">The Integer Format Types of configurable data may be used in either text or integer database fields.</span></span> <span data-ttu-id="d760d-107">L’attribut msmConfigItemNonNullable est implicite dans ce format de données et n’a pas besoin d’être défini.</span><span class="sxs-lookup"><span data-stu-id="d760d-107">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="d760d-108">NULL n’est jamais une valeur valide pour ce type.</span><span class="sxs-lookup"><span data-stu-id="d760d-108">Null is never a valid value for this type.</span></span>

<span data-ttu-id="d760d-109">Le type de format entier suivant existe.</span><span class="sxs-lookup"><span data-stu-id="d760d-109">The following Integer Format type exists.</span></span>

[<span data-ttu-id="d760d-110">Type d’entier arbitraire</span><span class="sxs-lookup"><span data-stu-id="d760d-110">Arbitrary Integer Type</span></span>](arbitrary-integer-type.md)

<span data-ttu-id="d760d-111">Les éléments configurables du type de format entier sont utilisés dans les colonnes de type texte ou entier et peuvent en général être remplacés par n’importe quel entier positif ou négatif.</span><span class="sxs-lookup"><span data-stu-id="d760d-111">Configurable items of the Integer Format Type are used in either text or integer columns and in general could be replaced by any positive or negative integer.</span></span> <span data-ttu-id="d760d-112">Toutefois, certains éléments configurables peuvent également avoir des restrictions sémantiques caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="d760d-112">However, particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="d760d-113">Par exemple, un élément configurable particulier qui doit être un entier compris entre 0 et 100 a une restriction sémantique supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d760d-113">For example, a particular configurable item required to be an integer between 0 and 100 has and additional semantic restriction.</span></span> <span data-ttu-id="d760d-114">Ces restrictions ne sont pas appliquées par Mergemod.dll et par conséquent, les auteurs de module doivent être préparés à gérer toute chaîne conforme au type de format entier spécifié.</span><span class="sxs-lookup"><span data-stu-id="d760d-114">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Integer Format type.</span></span>

 

 



