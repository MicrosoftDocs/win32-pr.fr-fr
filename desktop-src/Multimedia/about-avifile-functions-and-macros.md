---
title: À propos des fonctions et macros AVIFile
description: À propos des fonctions et macros AVIFile
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- AVIFileInit fonction)
- AVIFileExit fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029822"
---
# <a name="about-avifile-functions-and-macros"></a><span data-ttu-id="f2670-105">À propos des fonctions et macros AVIFile</span><span class="sxs-lookup"><span data-stu-id="f2670-105">About AVIFile Functions and Macros</span></span>

<span data-ttu-id="f2670-106">Les fonctions et macros AVIFile gèrent les informations dans des fichiers basés sur le temps sous la forme d’un ou de plusieurs *flux de données* au lieu de blocs balisés de données appelés segments.</span><span class="sxs-lookup"><span data-stu-id="f2670-106">The AVIFile functions and macros handle the information in time-based files as one or more *data streams* instead of tagged blocks of data called chunks.</span></span> <span data-ttu-id="f2670-107">Les flux de données font référence aux composants d’un fichier basé sur l’heure.</span><span class="sxs-lookup"><span data-stu-id="f2670-107">Data streams refer to the components of a time-based file.</span></span> <span data-ttu-id="f2670-108">Un fichier AVI peut contenir plusieurs types de données différents, tels qu’une séquence vidéo, une piste audio anglaise et une bande son française.</span><span class="sxs-lookup"><span data-stu-id="f2670-108">An AVI file can contain several different types of data, such as a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="f2670-109">À l’aide de AVIFile, une application peut accéder séparément à chacun de ces composants.</span><span class="sxs-lookup"><span data-stu-id="f2670-109">Using AVIFile, an application can access each of these components separately.</span></span>

> [!Note]  
> <span data-ttu-id="f2670-110">Bien que les fonctions et macros AVIFile fonctionnent avec n’importe quel fichier RIFF, cette vue d’ensemble illustre leur utilisation avec les fichiers AVI uniquement.</span><span class="sxs-lookup"><span data-stu-id="f2670-110">Although the AVIFile functions and macros work with any RIFF file, this overview demonstrates their use with AVI files only.</span></span> <span data-ttu-id="f2670-111">Les fichiers AVI sont généralement des fichiers basés sur le temps utilisés avec les macros et les fonctions AVIFile.</span><span class="sxs-lookup"><span data-stu-id="f2670-111">AVI files are typically the time-based files used with the AVIFile macros and functions.</span></span>

 

<span data-ttu-id="f2670-112">Les fonctions et les macros AVIFile sont contenues dans une bibliothèque de liens dynamiques.</span><span class="sxs-lookup"><span data-stu-id="f2670-112">AVIFile functions and macros are contained in a dynamic-link library.</span></span> <span data-ttu-id="f2670-113">Pour initialiser la bibliothèque, utilisez la fonction [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) .</span><span class="sxs-lookup"><span data-stu-id="f2670-113">To initialize the library, use the [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) function.</span></span> <span data-ttu-id="f2670-114">Après l’initialisation de la bibliothèque, vous pouvez utiliser l’une des fonctions ou macros AVIFile.</span><span class="sxs-lookup"><span data-stu-id="f2670-114">After you initialize the library, you can use any of the AVIFile functions or macros.</span></span> <span data-ttu-id="f2670-115">Pour libérer la bibliothèque, utilisez la fonction [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) .</span><span class="sxs-lookup"><span data-stu-id="f2670-115">To release the library, use the [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) function.</span></span> <span data-ttu-id="f2670-116">AVIFile conserve un décompte de références des applications qui utilisent la bibliothèque, mais pas celles qui l’ont publié.</span><span class="sxs-lookup"><span data-stu-id="f2670-116">AVIFile maintains a reference count of the applications that are using the library, but not those that have released it.</span></span> <span data-ttu-id="f2670-117">Vos applications doivent équilibrer chaque utilisation de **AVIFileInit** avec un appel à **AVIFileExit** pour libérer complètement la bibliothèque une fois que chaque application a terminé de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="f2670-117">Your applications should balance each use of **AVIFileInit** with a call to **AVIFileExit** to completely release the library after each application finishes using it.</span></span>

 

 




