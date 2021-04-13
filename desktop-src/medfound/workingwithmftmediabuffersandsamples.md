---
description: Utilisation des mémoires tampons et des exemples de médias MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Utilisation des mémoires tampons et des exemples de médias MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321510"
---
# <a name="working-with-mft-media-buffers-and-samples"></a><span data-ttu-id="da35e-103">Utilisation des mémoires tampons et des exemples de médias MFT</span><span class="sxs-lookup"><span data-stu-id="da35e-103">Working with MFT Media Buffers and Samples</span></span>

<span data-ttu-id="da35e-104">Le codec MFTs passe les données multimédias à l’aide des mémoires tampons et des exemples de médias.</span><span class="sxs-lookup"><span data-stu-id="da35e-104">Codec MFTs pass media data back and forth by using media buffers and samples.</span></span>

<span data-ttu-id="da35e-105">Une mémoire tampon de média est un objet COM qui gère un bloc de mémoire, généralement pour contenir des données multimédias.</span><span class="sxs-lookup"><span data-stu-id="da35e-105">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="da35e-106">Lorsque des données sont transmises à ou à partir d’une table MFT, elles sont toujours transmises sous la forme d’une mémoire tampon de média.</span><span class="sxs-lookup"><span data-stu-id="da35e-106">When data is passed to or from an MFT, it is always passed in the form of a media buffer.</span></span>

<span data-ttu-id="da35e-107">Toutes les mémoires tampons de média exposent l’interface **IMFMediaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="da35e-107">All media buffers expose the **IMFMediaBuffer** interface.</span></span> <span data-ttu-id="da35e-108">Cette interface est conçue pour tous les types de données.</span><span class="sxs-lookup"><span data-stu-id="da35e-108">This interface is designed for any type of data.</span></span> <span data-ttu-id="da35e-109">Les mémoires tampons contenant des données vidéo exposent souvent **IMF2DBuffer**.</span><span class="sxs-lookup"><span data-stu-id="da35e-109">Buffers containing video data often also expose **IMF2DBuffer**.</span></span>

<span data-ttu-id="da35e-110">Une mémoire tampon de média a une taille maximale, qui est la quantité de mémoire allouée pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="da35e-110">A media buffer has a maximum size, which is the amount of memory allocated for the buffer.</span></span> <span data-ttu-id="da35e-111">Pour trouver la taille maximale, appelez **IMFMediaBuffer :: GetMaxLength**.</span><span class="sxs-lookup"><span data-stu-id="da35e-111">To find the maximum size, call **IMFMediaBuffer::GetMaxLength**.</span></span> <span data-ttu-id="da35e-112">À tout moment, une mémoire tampon de support a également une longueur actuelle, qui correspond à la quantité de données valides dans la mémoire tampon, allant de zéro octet jusqu’à la taille maximale.</span><span class="sxs-lookup"><span data-stu-id="da35e-112">At any point in time, a media buffer also has a current length, which is the amount of valid data in the buffer, ranging from zero bytes up to the maximum size.</span></span> <span data-ttu-id="da35e-113">Pour connaître la longueur actuelle, appelez **IMFMediaBuffer :: GetCurrentLength**.</span><span class="sxs-lookup"><span data-stu-id="da35e-113">To get the current length, call **IMFMediaBuffer::GetCurrentLength**.</span></span> <span data-ttu-id="da35e-114">Lorsque la mémoire tampon est créée, la longueur actuelle est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="da35e-114">When the buffer is created, the current length is zero.</span></span> <span data-ttu-id="da35e-115">Si vous écrivez des données dans la mémoire tampon, appelez **IMFMediaBuffer :: SetCurrentLength** pour mettre à jour la longueur actuelle.</span><span class="sxs-lookup"><span data-stu-id="da35e-115">If you write data to the buffer, call **IMFMediaBuffer::SetCurrentLength** to update the current length.</span></span>

<span data-ttu-id="da35e-116">Pour accéder à la mémoire dans la mémoire tampon, appelez **IMFMediaBuffer :: Lock**.</span><span class="sxs-lookup"><span data-stu-id="da35e-116">To access the memory in the buffer, call **IMFMediaBuffer::Lock**.</span></span> <span data-ttu-id="da35e-117">Cette méthode retourne un pointeur vers le début du bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="da35e-117">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="da35e-118">Quand vous avez fini d’utiliser le pointeur, appelez **IMFMediaBuffer :: Unlock**.</span><span class="sxs-lookup"><span data-stu-id="da35e-118">When you are done using the pointer, call **IMFMediaBuffer::Unlock**.</span></span> <span data-ttu-id="da35e-119">La méthode **Lock** n’est pas un mécanisme de synchronisation de threads. Cela ne garantit pas que les autres threads ne peuvent pas accéder à la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="da35e-119">The **Lock** method is not a thread synchronization mechanism; it does not guarantee that other threads cannot access the buffer.</span></span> <span data-ttu-id="da35e-120">La méthode **Lock** est utilisée pour s’assurer que l’accès à la mémoire reste valide jusqu’à ce que vous appeliez la méthode **Unlock** .</span><span class="sxs-lookup"><span data-stu-id="da35e-120">The **Lock** method is used to assure that the memory accessed will remain valid until you call the **Unlock** method.</span></span>

<span data-ttu-id="da35e-121">Un exemple d’objet multimédia (dans le contexte du kit de développement logiciel (SDK) Media Foundation) est un objet qui contient une liste triée de zéro ou plusieurs mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="da35e-121">A media sample object (in the context of the Media Foundation SDK) is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="da35e-122">Les exemples de supports exposent l’interface **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="da35e-122">Media samples expose the **IMFSample** interface.</span></span>

<span data-ttu-id="da35e-123">Pour créer un nouvel exemple, appelez la fonction **MFCreateSample** .</span><span class="sxs-lookup"><span data-stu-id="da35e-123">To create a new sample, call the **MFCreateSample** function.</span></span> <span data-ttu-id="da35e-124">Initialement, la liste de mémoires tampons de l’exemple est vide.</span><span class="sxs-lookup"><span data-stu-id="da35e-124">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="da35e-125">Pour ajouter une mémoire tampon à la fin de la liste, appelez **IMFSample :: AddBuffer**.</span><span class="sxs-lookup"><span data-stu-id="da35e-125">To add a buffer to the end of the list, call **IMFSample::AddBuffer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da35e-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da35e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da35e-127">Utilisation du codec DMOs</span><span class="sxs-lookup"><span data-stu-id="da35e-127">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> <dt>

[<span data-ttu-id="da35e-128">Utilisation du codec MFTs</span><span class="sxs-lookup"><span data-stu-id="da35e-128">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



