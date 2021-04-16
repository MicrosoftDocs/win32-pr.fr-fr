---
description: Les transformations sécurisées-chemin d’accès complet doivent avoir une source située dans le chemin d’accès complet spécifié dans la propriété transformations.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Sécuriser-transformations de chemin d’accès complet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530303"
---
# <a name="secure-full-path-transforms"></a><span data-ttu-id="8c587-103">Sécuriser-transformations de chemin d’accès complet</span><span class="sxs-lookup"><span data-stu-id="8c587-103">Secure-Full-Path Transforms</span></span>

<span data-ttu-id="8c587-104">Les transformations sécurisées-chemin d’accès complet doivent avoir une source située dans le chemin d’accès complet spécifié dans la propriété [**TRANSformations**](transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="8c587-104">Secure-full-path transforms must have a source located at the full path specified in the [**TRANSFORMS**](transforms.md) property.</span></span> <span data-ttu-id="8c587-105">Lorsque le package est installé ou publié, le programme d’installation enregistre les transformations dans un cache où, sur un système de fichiers sécurisé, l’utilisateur ne dispose pas d’un accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="8c587-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="8c587-106">Si la copie locale de la transformation devient indisponible, elle peut uniquement restaurer le cache à l’aide du chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="8c587-106">If the local copy of the transform becomes unavailable, it may only restore the cache using the specified path.</span></span> <span data-ttu-id="8c587-107">La suppression d’un produit par un utilisateur supprime toutes les transformations sécurisées pour ce produit de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c587-107">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="8c587-108">Pour appliquer des transformations sécurisées-chemins d’accès complets lors de l’installation d’un package, définissez la [stratégie TransformsSecure](transformssecure-policy.md) ou la propriété [**TransformsSecure**](transformssecure.md) ou faites \| passer le premier caractère dans la liste transformer.</span><span class="sxs-lookup"><span data-stu-id="8c587-108">To apply secure-full-paths transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property or make \| the first character passed in the transform list.</span></span> <span data-ttu-id="8c587-109">Les chemins d’accès complets à la source de chaque transformation doivent être passés dans la chaîne transformations.</span><span class="sxs-lookup"><span data-stu-id="8c587-109">The full paths to the source of each transform must be passed in the transforms string.</span></span> <span data-ttu-id="8c587-110">Si des chemins d’accès relatifs se trouvent dans la liste, l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="8c587-110">If any relative paths are in the list, the installation fails.</span></span> <span data-ttu-id="8c587-111">La source de la transformation ne doit pas être localisée avec la source du package.</span><span class="sxs-lookup"><span data-stu-id="8c587-111">The transform source does not have to be located with the source of the package.</span></span>

 

 



