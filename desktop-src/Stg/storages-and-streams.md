---
title: Stockages et flux
description: Un objet de stockage est analogue à un répertoire du système de fichiers.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671769"
---
# <a name="storages-and-streams"></a><span data-ttu-id="e47ab-103">Stockages et flux</span><span class="sxs-lookup"><span data-stu-id="e47ab-103">Storages and Streams</span></span>

<span data-ttu-id="e47ab-104">Un objet de stockage est analogue à un répertoire du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e47ab-104">A storage object is analogous to a file system directory.</span></span> <span data-ttu-id="e47ab-105">De même qu’un répertoire peut contenir d’autres répertoires et fichiers, un objet de stockage peut contenir d’autres objets de stockage et objets de flux.</span><span class="sxs-lookup"><span data-stu-id="e47ab-105">Just as a directory can contain other directories and files, a storage object can contain other storage objects and stream objects.</span></span> <span data-ttu-id="e47ab-106">À l’instar d’un répertoire, un objet de stockage effectue le suivi des emplacements et des tailles des objets de stockage et des objets de flux imbriqués sous celui-ci.</span><span class="sxs-lookup"><span data-stu-id="e47ab-106">Also like a directory, a storage object tracks the locations and sizes of the storage objects and stream objects nested beneath it.</span></span>

<span data-ttu-id="e47ab-107">Un objet de flux est analogue à la notion traditionnelle d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="e47ab-107">A stream object is analogous to the traditional notion of a file.</span></span> <span data-ttu-id="e47ab-108">À l’instar d’un fichier, un flux contient des données stockées sous la forme d’une séquence d’octets consécutive.</span><span class="sxs-lookup"><span data-stu-id="e47ab-108">Like a file, a stream contains data stored as a consecutive sequence of bytes.</span></span>

<span data-ttu-id="e47ab-109">Un fichier composé COM se compose d’un objet de stockage racine contenant au moins un objet de flux représentant ses données natives, ainsi qu’un ou plusieurs objets de stockage correspondant à ses objets liés et incorporés.</span><span class="sxs-lookup"><span data-stu-id="e47ab-109">A COM compound file consists of a root storage object containing at least one stream object representing its native data along with one or more storage objects corresponding to its linked and embedded objects.</span></span> <span data-ttu-id="e47ab-110">L’objet de stockage racine est mappé à un nom de fichier dans le système de fichiers dans lequel il se trouve.</span><span class="sxs-lookup"><span data-stu-id="e47ab-110">The root storage object maps to a file name in whatever file system it happens to reside.</span></span> <span data-ttu-id="e47ab-111">Chacun des objets à l’intérieur du document est également représenté par un objet de stockage contenant un ou plusieurs objets de flux, et peut-être également contenir un ou plusieurs objets de stockage.</span><span class="sxs-lookup"><span data-stu-id="e47ab-111">Each of the objects inside the document also is represented by a storage object containing one or more stream objects, and perhaps also containing one or more storage objects.</span></span> <span data-ttu-id="e47ab-112">De cette façon, un document peut se composer d’un nombre illimité d’objets imbriqués.</span><span class="sxs-lookup"><span data-stu-id="e47ab-112">In this way, a document can consist of an unlimited number of nested objects.</span></span> <span data-ttu-id="e47ab-113">Pour plus d’informations, consultez [fichiers composés](compound-files.md).</span><span class="sxs-lookup"><span data-stu-id="e47ab-113">For more information, see [Compound Files](compound-files.md).</span></span>

 

 




