---
title: Prise en charge de l’exemple alloué par l’utilisateur
description: Prise en charge de l’exemple alloué par l’utilisateur
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Media Format SDK, exemple de prise en charge de l’utilisateur alloué par l’utilisateur
- ASF (Advanced Systems Format), prise en charge des exemples alloués par l’utilisateur
- ASF (format de systèmes avancés), prise en charge des exemples alloués par l’utilisateur
- prise en charge de l’exemple alloué par l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028969"
---
# <a name="user-allocated-sample-support"></a><span data-ttu-id="c8441-107">Prise en charge de l’exemple alloué par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8441-107">User Allocated Sample Support</span></span>

<span data-ttu-id="c8441-108">Dans des circonstances normales, l’objet lecteur et l’objet lecteur synchrone créent un nouvel objet buffer pour chaque exemple fourni à votre application.</span><span class="sxs-lookup"><span data-stu-id="c8441-108">Under normal circumstances, both the reader object and the synchronous reader object create a new buffer object for each sample delivered to your application.</span></span> <span data-ttu-id="c8441-109">Cela est dû au fait que l’objet de lecture n’a aucun moyen de savoir ce que fait votre application avec les exemples après l’avoir extraite.</span><span class="sxs-lookup"><span data-stu-id="c8441-109">This is because the reading object has no way of knowing what your application does with the samples after it gets them.</span></span> <span data-ttu-id="c8441-110">Même si de nombreuses applications lisent uniquement les exemples pour les rendre immédiatement, certaines applications peuvent avoir besoin de gérer des échantillons pendant une longue période.</span><span class="sxs-lookup"><span data-stu-id="c8441-110">Even though many applications read samples only to render them immediately, some applications may need to maintain samples for a long time.</span></span> <span data-ttu-id="c8441-111">Par conséquent, l’objet de lecture ne peut pas réutiliser les mémoires tampons qu’il alloue. elle les remet à votre application, qui les contrôle ensuite.</span><span class="sxs-lookup"><span data-stu-id="c8441-111">The reading object cannot, therefore, reuse any of the buffers it allocates; it delivers them to your application, which then has control over them.</span></span>

<span data-ttu-id="c8441-112">Le problème de cette approche est qu’un fichier peut contenir un nombre énorme d’exemples.</span><span class="sxs-lookup"><span data-stu-id="c8441-112">The problem with this approach is that a file can contain an immense number of samples.</span></span> <span data-ttu-id="c8441-113">Si chacune d’entre elles requiert la création d’un nouvel objet de mémoire tampon, l’allocation et la libération de la mémoire est beaucoup plus longue.</span><span class="sxs-lookup"><span data-stu-id="c8441-113">If each one of them requires a new buffer object to be created, a lot of processor time is wasted allocating and releasing memory.</span></span> <span data-ttu-id="c8441-114">Dans les applications sensibles au temps, telles que les lecteurs multimédias, cette surcharge peut être très préjudiciable aux performances.</span><span class="sxs-lookup"><span data-stu-id="c8441-114">In time-sensitive applications such as media players, this overhead can be very detrimental to performance.</span></span>

<span data-ttu-id="c8441-115">Pour atténuer les problèmes de performances des exemples alloués par lecteur, le lecteur et le lecteur synchrone prennent en charge les exemples alloués par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8441-115">To alleviate the performance issues of reader-allocated samples, both the reader and the synchronous reader support user-allocated samples.</span></span> <span data-ttu-id="c8441-116">Pour utiliser des exemples alloués par votre application, l’objet de lecture effectue des appels à un exemple de méthode de rappel d’allocation que vous implémentez.</span><span class="sxs-lookup"><span data-stu-id="c8441-116">To use samples allocated by your application, the reading object makes calls to a sample allocation callback method that you implement.</span></span> <span data-ttu-id="c8441-117">La logique utilisée par le rappel pour fournir des tampons à l’objet de lecture dépend entièrement de vous.</span><span class="sxs-lookup"><span data-stu-id="c8441-117">The logic used by the callback to deliver buffers to the reading object is entirely up to you.</span></span> <span data-ttu-id="c8441-118">Vous pouvez utiliser un pool de mémoires tampons pour le fichier entier ou utiliser plusieurs pools de mémoires tampons, un pour chaque sortie ou flux, ou tout autre schéma qui fonctionne pour votre application.</span><span class="sxs-lookup"><span data-stu-id="c8441-118">You can use a pool of buffers for the entire file or use multiple pools of buffers, one for each output or stream, or any other scheme that works for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8441-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8441-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8441-120">**Allocation de tampons pour la lecture de fichiers**</span><span class="sxs-lookup"><span data-stu-id="c8441-120">**Allocating Buffers for File Reading**</span></span>](allocating-buffers-for-file-reading.md)
</dt> <dt>

[<span data-ttu-id="c8441-121">**Fonctionnalités de lecture de fichier**</span><span class="sxs-lookup"><span data-stu-id="c8441-121">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




