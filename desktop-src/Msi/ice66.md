---
description: ICE66 utilise les tables de la base de données pour déterminer le schéma que votre base de données doit utiliser.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753013"
---
# <a name="ice66"></a><span data-ttu-id="659c4-103">ICE66</span><span class="sxs-lookup"><span data-stu-id="659c4-103">ICE66</span></span>

<span data-ttu-id="659c4-104">ICE66 utilise les tables de la base de données pour déterminer le schéma que votre base de données doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="659c4-104">ICE66 uses the tables in the database to determine which schema your database should use.</span></span>

<span data-ttu-id="659c4-105">Certaines fonctionnalités peuvent uniquement être disponibles si le package est installé sur un système avec une version actuelle de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="659c4-105">Some functionality may only be available if the package is installed on a system with a current Windows Installer version.</span></span>

## <a name="result"></a><span data-ttu-id="659c4-106">Résultats</span><span class="sxs-lookup"><span data-stu-id="659c4-106">Result</span></span>

<span data-ttu-id="659c4-107">ICE66 publie un avertissement si votre base de données utilise un schéma incorrect.</span><span class="sxs-lookup"><span data-stu-id="659c4-107">ICE66 posts a warning if your database is using the wrong schema.</span></span>

## <a name="example"></a><span data-ttu-id="659c4-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="659c4-108">Example</span></span>

<span data-ttu-id="659c4-109">ICE66 signale l’avertissement suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="659c4-109">ICE66 reports the following warning for the example shown.</span></span>

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

<span data-ttu-id="659c4-110">Cet avertissement peut être ignoré si vous souhaitez que votre package soit installé à l’aide d’une version actuelle de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="659c4-110">This warning can be ignored if you want your package to be installed using a current Windows Installer version.</span></span> <span data-ttu-id="659c4-111">Par exemple, si vous souhaitez que votre package soit installé uniquement sur la version 2,0 ou ultérieure, remplacez votre schéma de package (PID \_ PageCount) par 200.</span><span class="sxs-lookup"><span data-stu-id="659c4-111">For example, if you want your package to be installable only on version 2.0 or later, change your package schema (PID\_PAGECOUNT) to 200.</span></span>

[<span data-ttu-id="659c4-112">Table IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="659c4-112">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="659c4-113">Composant \_ partagé</span><span class="sxs-lookup"><span data-stu-id="659c4-113">Component\_Shared</span></span> | <span data-ttu-id="659c4-114">Application de composant \_</span><span class="sxs-lookup"><span data-stu-id="659c4-114">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="659c4-115">Composant1</span><span class="sxs-lookup"><span data-stu-id="659c4-115">Component1</span></span>        | <span data-ttu-id="659c4-116">Component2</span><span class="sxs-lookup"><span data-stu-id="659c4-116">Component2</span></span>             |



 

[<span data-ttu-id="659c4-117">Flux d’informations de synthèse</span><span class="sxs-lookup"><span data-stu-id="659c4-117">Summary Information Stream</span></span>](summary-information-stream.md)



| <span data-ttu-id="659c4-118">PIDt</span><span class="sxs-lookup"><span data-stu-id="659c4-118">PIDt</span></span>           | <span data-ttu-id="659c4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="659c4-119">Value</span></span> |
|----------------|-------|
| <span data-ttu-id="659c4-120">PID \_ PageCount</span><span class="sxs-lookup"><span data-stu-id="659c4-120">PID\_PAGECOUNT</span></span> | <span data-ttu-id="659c4-121">100</span><span class="sxs-lookup"><span data-stu-id="659c4-121">100</span></span>   |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="659c4-122">Table utilisée lors de l’exécution :</span><span class="sxs-lookup"><span data-stu-id="659c4-122">Table used during execution:</span></span>

[<span data-ttu-id="659c4-123">\_Table colonnes</span><span class="sxs-lookup"><span data-stu-id="659c4-123">\_Columns table</span></span>](-columns-table.md)

## <a name="related-topics"></a><span data-ttu-id="659c4-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="659c4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="659c4-125">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="659c4-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



