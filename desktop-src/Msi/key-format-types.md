---
description: Les types de format de clé des données configurables peuvent être utilisés dans les champs de texte pour fournir une clé dans une table de base de données.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Types de format de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514189"
---
# <a name="key-format-types"></a><span data-ttu-id="52753-103">Types de format de clé</span><span class="sxs-lookup"><span data-stu-id="52753-103">Key Format Types</span></span>

<span data-ttu-id="52753-104">Les types de format de clé des données configurables peuvent être utilisés dans les champs de texte pour fournir une clé dans une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="52753-104">The Key Format Types of configurable data may be used in text fields to provide a key into a database table.</span></span> <span data-ttu-id="52753-105">L’attribut msmConfigItemNonNullable est implicite dans ce format de données et n’a pas besoin d’être défini.</span><span class="sxs-lookup"><span data-stu-id="52753-105">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="52753-106">NULL n’est jamais une valeur valide pour ce type.</span><span class="sxs-lookup"><span data-stu-id="52753-106">Null is never a valid value for this type.</span></span> <span data-ttu-id="52753-107">Les réponses à tous les éléments de format de clé doivent être au [format spécial CMSM](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="52753-107">Responses to all Key format items must be in [CMSM Special Format](cmsm-special-format.md).</span></span>

<span data-ttu-id="52753-108">Les types de format de clé suivants existent :</span><span class="sxs-lookup"><span data-stu-id="52753-108">The following Key Format types exist:</span></span>

[<span data-ttu-id="52753-109">Type de répertoire</span><span class="sxs-lookup"><span data-stu-id="52753-109">Directory Type</span></span>](directory-type.md)

[<span data-ttu-id="52753-110">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="52753-110">File Type</span></span>](file-type.md)

[<span data-ttu-id="52753-111">Type de propriété</span><span class="sxs-lookup"><span data-stu-id="52753-111">Property Type</span></span>](property-type.md)

[<span data-ttu-id="52753-112">Type de dialogue</span><span class="sxs-lookup"><span data-stu-id="52753-112">Dialog Type</span></span>](dialog-type.md)

[<span data-ttu-id="52753-113">Type binaire</span><span class="sxs-lookup"><span data-stu-id="52753-113">Binary Type</span></span>](binary-type.md)

[<span data-ttu-id="52753-114">Type d’icône</span><span class="sxs-lookup"><span data-stu-id="52753-114">Icon Type</span></span>](icon-type.md)

<span data-ttu-id="52753-115">Les éléments configurables du type de format de clé sont utilisés dans les colonnes de texte pour fournir une clé de base de données. en général, il est possible de remplacer par n’importe quelle chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="52753-115">Configurable items of the Key Format Type are used in text columns to provide a database key and in general could be replaced by any text string.</span></span> <span data-ttu-id="52753-116">Les types individuels peuvent avoir des restrictions syntaxiques supplémentaires, mais ces restrictions ne sont pas appliquées par Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="52753-116">The individual types may have additional syntactic restrictions, but these restrictions are not enforced by Mergemod.dll.</span></span> <span data-ttu-id="52753-117">Certains éléments configurables peuvent également présenter des restrictions sémantiques caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="52753-117">Particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="52753-118">Par exemple, un élément configurable spécifique peut être une clé de la [table binaire](binary-table.md) vers une ligne contenant une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="52753-118">For example, a particular configurable item may be required to be a key into the [Binary table](binary-table.md) to a row containing a bitmap image.</span></span> <span data-ttu-id="52753-119">Ces restrictions ne sont pas appliquées par Mergemod.dll et par conséquent, les auteurs de module doivent être préparés à gérer toute chaîne conforme au type de format de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="52753-119">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Key Format type.</span></span> <span data-ttu-id="52753-120">Sauf spécification contraire de la signification sémantique ou des attributs, NULL est une réponse valide.</span><span class="sxs-lookup"><span data-stu-id="52753-120">Unless otherwise specified by semantic meaning or attributes, null is a valid response.</span></span>

 

 



