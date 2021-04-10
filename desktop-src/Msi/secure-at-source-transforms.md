---
description: Les transformations sécurisées à la source doivent avoir une source située à la racine de la source du package.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Transformations sécurisées à la source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869042"
---
# <a name="secure-at-source-transforms"></a><span data-ttu-id="9dc7a-103">Transformations sécurisées à la source</span><span class="sxs-lookup"><span data-stu-id="9dc7a-103">Secure-At-Source Transforms</span></span>

<span data-ttu-id="9dc7a-104">Les transformations sécurisées à la source doivent avoir une source située à la racine de la source du package.</span><span class="sxs-lookup"><span data-stu-id="9dc7a-104">Secure-at-source transforms must have a source located at the root of the source for the package.</span></span> <span data-ttu-id="9dc7a-105">Lorsque le package est installé ou publié, le programme d’installation enregistre les transformations dans un cache où, sur un système de fichiers sécurisé, l’utilisateur ne dispose pas d’un accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="9dc7a-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="9dc7a-106">Si la copie locale de la transformation devient indisponible, le programme d’installation recherche une source pour restaurer le cache.</span><span class="sxs-lookup"><span data-stu-id="9dc7a-106">If the local copy of the transform becomes unavailable, the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="9dc7a-107">La méthode est identique à la recherche d’un fichier. msi dans la liste source.</span><span class="sxs-lookup"><span data-stu-id="9dc7a-107">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="9dc7a-108">Pour plus d’informations, consultez [résilience source](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="9dc7a-108">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="9dc7a-109">La suppression d’un produit par un utilisateur supprime toutes les transformations sécurisées pour ce produit de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9dc7a-109">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="9dc7a-110">Pour appliquer des transformations sécurisées au niveau de la source lors de l’installation d’un package, définissez la [stratégie TransformsSecure](transformssecure-policy.md) ou la propriété [**TransformsSecure**](transformssecure.md) , ou faites de @ le premier caractère transmis dans la liste transformer.</span><span class="sxs-lookup"><span data-stu-id="9dc7a-110">To apply secure-at-source transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property, or make @ the first character passed in the transform list.</span></span> <span data-ttu-id="9dc7a-111">Chaque transformation doit être indiquée par un nom de fichier et doit se trouver à la racine de la source du package.</span><span class="sxs-lookup"><span data-stu-id="9dc7a-111">Each transform must be indicated by a file name and must be located at the root of the source for the package.</span></span> <span data-ttu-id="9dc7a-112">Si l’une des transformations ne se trouve pas à la racine de la source du package, l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="9dc7a-112">If any of the transforms are not located at the root of the package source, the installation fails.</span></span> <span data-ttu-id="9dc7a-113">Pour plus d’informations, consultez [application de transformations](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="9dc7a-113">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



