---
description: ICEM14 valide la colonne valeur de la table ModuleSubstitution.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114331"
---
# <a name="icem14"></a><span data-ttu-id="1fdca-103">ICEM14</span><span class="sxs-lookup"><span data-stu-id="1fdca-103">ICEM14</span></span>

<span data-ttu-id="1fdca-104">ICEM14 valide la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="1fdca-104">ICEM14 validates the Value Column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="1fdca-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="1fdca-105">Result</span></span>

<span data-ttu-id="1fdca-106">ICEM14 publie les erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1fdca-106">ICEM14 posts the following errors.</span></span>



| <span data-ttu-id="1fdca-107">Error</span><span class="sxs-lookup"><span data-stu-id="1fdca-107">Error</span></span>                                                                                                                                                         | <span data-ttu-id="1fdca-108">Signification</span><span class="sxs-lookup"><span data-stu-id="1fdca-108">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fdca-109">Chaîne de remplacement dans la colonne ModuleSubstitution. Value de la ligne \[ 1 \] . \[ 2 \] . \[ 3 \] est introuvable dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1fdca-109">The replacement string in ModuleSubstitution.Value column in row \[1\].\[2\].\[3\] is not found in ModuleConfiguration table.</span></span>                                 | <span data-ttu-id="1fdca-110">\[1 \] . \[ 2 \] . \[ 3 \] fait référence à une clé primaire *table. Row. colonne* pour une ligne de la table ModuleSubstitution.</span><span class="sxs-lookup"><span data-stu-id="1fdca-110">\[1\].\[2\].\[3\] refers to a *table.row.column* primary key for a row in the ModuleSubstitution table.</span></span> <span data-ttu-id="1fdca-111">Le modèle de mise en forme dans le champ valeur de cette ligne ne correspond pas à une ligne d’attributs configurables dans la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1fdca-111">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                            |
| <span data-ttu-id="1fdca-112">Dans la table ModuleSubstitution de la ligne \[ 1 \] . \[ 2 \] . \[ 3 \] , un élément configurable est indiqué dans la table'% s'.</span><span class="sxs-lookup"><span data-stu-id="1fdca-112">In ModuleSubstitution table in row \[1\].\[2\].\[3\], a configurable item is indicated in the table '%s'.</span></span> <span data-ttu-id="1fdca-113">La table'% s’ne doit pas contenir d’éléments configurables.</span><span class="sxs-lookup"><span data-stu-id="1fdca-113">The table '%s' must not contain configurable items.</span></span> | <span data-ttu-id="1fdca-114">L’une des tables suivantes est indiquée dans la colonne table de la table ModuleSubstitution : [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md)ou [ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1fdca-114">One of the following tables is listed in the Table column of the ModuleSubstitution table: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md), or [ModuleSignature](modulesignature-table.md).</span></span> <span data-ttu-id="1fdca-115">Ces tables ne peuvent pas contenir de champs configurables.</span><span class="sxs-lookup"><span data-stu-id="1fdca-115">These tables cannot contain configurable fields.</span></span> |
| <span data-ttu-id="1fdca-116">Dans la table ModuleSubstitution de la ligne \[ 1 \] . \[ 2 \] . \[ 3 \] , une chaîne de remplacement vide est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1fdca-116">In ModuleSubstitution table in row \[1\].\[2\].\[3\], an empty replacement string is specified.</span></span>                                                               | <span data-ttu-id="1fdca-117">Le modèle de mise en forme dans le champ valeur de cette ligne ne correspond pas à une ligne d’attributs configurables dans la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1fdca-117">The formatting template in the Value field of this row does not correspond to a row of configurable attributes in the [ModuleConfiguration Table](moduleconfiguration-table.md).</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="1fdca-118">ICEM14 publie l’avertissement suivant.</span><span class="sxs-lookup"><span data-stu-id="1fdca-118">ICEM14 posts the following warning.</span></span>



| <span data-ttu-id="1fdca-119">Avertissement</span><span class="sxs-lookup"><span data-stu-id="1fdca-119">Warning</span></span>                                                                  | <span data-ttu-id="1fdca-120">Signification</span><span class="sxs-lookup"><span data-stu-id="1fdca-120">Meaning</span></span>                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="1fdca-121">La table ModuleSubstitution existe mais la table ModuleConfiguration est manquante</span><span class="sxs-lookup"><span data-stu-id="1fdca-121">ModuleSubstitution table exists but ModuleConfiguration table is missing</span></span> | <span data-ttu-id="1fdca-122">La table ModuleConfiguration est absente.</span><span class="sxs-lookup"><span data-stu-id="1fdca-122">The ModuleConfiguration table is absent.</span></span> |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="1fdca-123">Table utilisée pendant l’exécution</span><span class="sxs-lookup"><span data-stu-id="1fdca-123">Table Used During Execution</span></span>

[<span data-ttu-id="1fdca-124">Table ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="1fdca-124">ModuleSubstitution table</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="1fdca-125">Table ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fdca-125">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)

## <a name="related-topics"></a><span data-ttu-id="1fdca-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fdca-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fdca-127">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="1fdca-127">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



