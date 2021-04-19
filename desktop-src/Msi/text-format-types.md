---
description: Les types de format de texte des données configurables peuvent être des chaînes de texte de n’importe quelle longueur. Les valeurs NULL incorporées ne sont pas autorisées.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Types de format de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539334"
---
# <a name="text-format-types"></a><span data-ttu-id="3277f-104">Types de format de texte</span><span class="sxs-lookup"><span data-stu-id="3277f-104">Text Format Types</span></span>

<span data-ttu-id="3277f-105">Les types de format de texte des données configurables peuvent être des chaînes de texte de n’importe quelle longueur.</span><span class="sxs-lookup"><span data-stu-id="3277f-105">The text format types of configurable data may be text strings of any length.</span></span> <span data-ttu-id="3277f-106">Les valeurs NULL incorporées ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="3277f-106">Embedded nulls are not allowed.</span></span>

<span data-ttu-id="3277f-107">Les types de format de texte suivants existent :</span><span class="sxs-lookup"><span data-stu-id="3277f-107">The following Text Format types exist:</span></span>

[<span data-ttu-id="3277f-108">Texte arbitraire</span><span class="sxs-lookup"><span data-stu-id="3277f-108">Arbitrary Text</span></span>](arbitrary-text-type.md)

[<span data-ttu-id="3277f-109">RTF</span><span class="sxs-lookup"><span data-stu-id="3277f-109">RTF</span></span>](rtf-type.md)

[<span data-ttu-id="3277f-110">Correct</span><span class="sxs-lookup"><span data-stu-id="3277f-110">Formatted</span></span>](formatted-type.md)

[<span data-ttu-id="3277f-111">Enum</span><span class="sxs-lookup"><span data-stu-id="3277f-111">Enum</span></span>](enum-type.md)

[<span data-ttu-id="3277f-112">Type d’identificateur</span><span class="sxs-lookup"><span data-stu-id="3277f-112">Identifier Type</span></span>](identifier-type.md)

<span data-ttu-id="3277f-113">Les éléments configurables du type de format texte sont utilisés dans les champs de base de données non binaires. en général, ils peuvent être remplacés par toute chaîne de n’importe quelle longueur.</span><span class="sxs-lookup"><span data-stu-id="3277f-113">Configurable items of the Text Format Type are used in non-binary database fields and in general could be replaced by any string of any length.</span></span> <span data-ttu-id="3277f-114">Toutefois, certains éléments configurables ont également des restrictions sémantiques.</span><span class="sxs-lookup"><span data-stu-id="3277f-114">However, particular configurable items also have semantic restrictions.</span></span> <span data-ttu-id="3277f-115">Par exemple, un élément configurable qui doit être une clé étrangère dans une table spécifique a des restrictions sémantiques supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3277f-115">For example, a configurable item that is required to be a foreign key into a specific table has additional semantic restrictions.</span></span> <span data-ttu-id="3277f-116">Ces restrictions sémantiques ne sont pas appliquées par Mergemod.dll et par conséquent, les auteurs de module doivent être préparés à gérer toute chaîne conforme au type de format texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="3277f-116">Such semantic restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Text Format type.</span></span>

 

 



