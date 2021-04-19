---
description: Cette section examine une partie d’un exemple d’application qui fonctionne sur le réseau très lentement. Tout au long de cette section, les modifications sont apportées au code initial pour améliorer ses performances.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Amélioration d’une application lente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516872"
---
# <a name="improving-a-slow-application"></a><span data-ttu-id="491a2-104">Amélioration d’une application lente</span><span class="sxs-lookup"><span data-stu-id="491a2-104">Improving a Slow Application</span></span>

<span data-ttu-id="491a2-105">Cette section examine une partie d’un exemple d’application qui fonctionne sur le réseau très lentement.</span><span class="sxs-lookup"><span data-stu-id="491a2-105">This section examines a portion of a sample application that operates over the network very slowly.</span></span> <span data-ttu-id="491a2-106">Tout au long de cette section, les modifications sont apportées au code initial pour améliorer ses performances.</span><span class="sxs-lookup"><span data-stu-id="491a2-106">Throughout this section, modifications are made to the initial code to improve its performance.</span></span>

<span data-ttu-id="491a2-107">L’exemple factice est la partie mise à jour pour un jeu appelé Life.</span><span class="sxs-lookup"><span data-stu-id="491a2-107">The mock sample is the updated portion for a game called Life.</span></span> <span data-ttu-id="491a2-108">L’application est écrite de telle sorte que le client effectue les calculs pour les mises à jour et les envoie au serveur.</span><span class="sxs-lookup"><span data-stu-id="491a2-108">The application is written such that the client performs the calculations for the updates and sends them to the server.</span></span> <span data-ttu-id="491a2-109">Le serveur affiche ensuite le champ vie résultante.</span><span class="sxs-lookup"><span data-stu-id="491a2-109">The server then displays the resulting Life field.</span></span> <span data-ttu-id="491a2-110">La sortie du client est un flux d’octets, regroupés en trois (triples), chaque triplet représentant une seule cellule à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="491a2-110">The output from the client is a stream of bytes, grouped in threes (triplets), each triplet representing one cell update.</span></span> <span data-ttu-id="491a2-111">Les octets de l’triplet représentent respectivement la ligne, la colonne et la valeur de la cellule.</span><span class="sxs-lookup"><span data-stu-id="491a2-111">The bytes in the triplet represent the row, column, and value, respectively, for the cell.</span></span>

<span data-ttu-id="491a2-112">Cet exemple commence comme une application intentionnellement médiocre, qui fournit la ligne de base à partir de laquelle les améliorations des performances peuvent être illustrées.</span><span class="sxs-lookup"><span data-stu-id="491a2-112">This sample begins as an intentionally poor performing application, which provides the baseline from which performance improvements can be illustrated.</span></span> <span data-ttu-id="491a2-113">À partir de là, le code est amélioré trois fois pour résoudre différents problèmes qui affectent les performances.</span><span class="sxs-lookup"><span data-stu-id="491a2-113">From there, the code is improved three times to address various issues that affect performance.</span></span> <span data-ttu-id="491a2-114">Ces exemples doivent être lus dans l’ordre, car chaque itération s’améliore sur la version précédente.</span><span class="sxs-lookup"><span data-stu-id="491a2-114">These samples should be read in order, as each iteration improves on the previous version.</span></span>

<span data-ttu-id="491a2-115">Le code de base, ainsi que les révisions qui améliorent ce code, sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="491a2-115">The baseline code, and the revisions that improve that code, are the following:</span></span>

-   [<span data-ttu-id="491a2-116">Version de référence : une application très médiocre</span><span class="sxs-lookup"><span data-stu-id="491a2-116">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
-   [<span data-ttu-id="491a2-117">Révision 1 : nettoyage évident</span><span class="sxs-lookup"><span data-stu-id="491a2-117">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
-   [<span data-ttu-id="491a2-118">Révision 2 : reconception pour des connexions moins nombreuses</span><span class="sxs-lookup"><span data-stu-id="491a2-118">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
-   [<span data-ttu-id="491a2-119">Révision 3 : envoi de bloc compressé</span><span class="sxs-lookup"><span data-stu-id="491a2-119">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
-   [<span data-ttu-id="491a2-120">Améliorations futures</span><span class="sxs-lookup"><span data-stu-id="491a2-120">Future Improvements</span></span>](future-improvements-2.md)

> [!WARNING]
> <span data-ttu-id="491a2-121">Les premiers exemples de l’application offrent des performances intentionnellement médiocres, afin d’illustrer les améliorations de performances possibles avec les modifications apportées au code.</span><span class="sxs-lookup"><span data-stu-id="491a2-121">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="491a2-122">N’utilisez pas ces exemples de code dans votre application. ils sont fournis à titre d’illustration uniquement.</span><span class="sxs-lookup"><span data-stu-id="491a2-122">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="491a2-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="491a2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="491a2-124">Applications Windows Sockets hautes performances</span><span class="sxs-lookup"><span data-stu-id="491a2-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



