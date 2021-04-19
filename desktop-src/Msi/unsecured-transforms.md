---
description: Les transformations qui n’ont pas été sécurisées, comme décrit dans transformations sécurisées, sont des transformations non sécurisées par défaut.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Transformations non sécurisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545160"
---
# <a name="unsecured-transforms"></a><span data-ttu-id="ef202-103">Transformations non sécurisées</span><span class="sxs-lookup"><span data-stu-id="ef202-103">Unsecured Transforms</span></span>

<span data-ttu-id="ef202-104">Les transformations qui n’ont pas été sécurisées, comme décrit dans [transformations sécurisées](secured-transforms.md) , sont des transformations non sécurisées par défaut.</span><span class="sxs-lookup"><span data-stu-id="ef202-104">Transforms that have not been secured as described in [Secured Transforms](secured-transforms.md) are unsecured transforms by default.</span></span>

<span data-ttu-id="ef202-105">Pour appliquer une transformation non sécurisée lors de l’installation d’un package, transmettez les noms des fichiers de transformation dans la chaîne de la propriété [**TRANSformations**](transforms.md) ou de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ef202-105">To apply an unsecured transform when installing a package, pass the transform file names in the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="ef202-106">Ne commencez pas la chaîne par les caractères @ ou \| , ou définissez la [stratégie TransformsSecure](transformssecure-policy.md) ou la propriété [**TransformsSecure**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="ef202-106">Do not begin the string with the @ or \| characters or set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="ef202-107">Notez que vous ne pouvez pas combiner des transformations sécurisées et des transformations [sécurisées](secured-transforms.md) dans la même liste de transformations.</span><span class="sxs-lookup"><span data-stu-id="ef202-107">Note that you cannot combine unsecured transforms and [secured transforms](secured-transforms.md) in the same transforms list.</span></span>

<span data-ttu-id="ef202-108">Si le package est installé ou publié dans le [contexte d’installation](installation-context.md)par utilisateur et qu’il comporte des transformations non sécurisées, le programme d’installation enregistre la source de transformation dans le dossier Application Data du profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef202-108">If the package is installed or advertised in the per-user [installation context](installation-context.md), and has unsecured transforms, the installer saves the transform source in the Application Data folder in the user's profile.</span></span> <span data-ttu-id="ef202-109">Cela permet à un utilisateur de gérer la personnalisation d’un produit tout en se déplaçant d’un ordinateur à l’autre.</span><span class="sxs-lookup"><span data-stu-id="ef202-109">This enables a user to maintain their customization of a product while moving between computers.</span></span>

<span data-ttu-id="ef202-110">Si le package est installé ou publié dans le [contexte d’installation](installation-context.md)par ordinateur et utilise des transformations non sécurisées, le programme d’installation enregistre la source de transformation dans le dossier% windir% \\ installer.</span><span class="sxs-lookup"><span data-stu-id="ef202-110">If the package is installed or advertised in the per-machine [installation context](installation-context.md), and uses unsecured transforms, the installer saves the transform source in the %windir%\\Installer folder.</span></span>

<span data-ttu-id="ef202-111">Lors de la première installation du package, le programme d’installation commence par Rechercher la transformation à la source fournie par la propriété [**TRANSformations**](transforms.md) ou la chaîne de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ef202-111">During a first-time installation of the package, the installer first searches for the transform at the source supplied by the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="ef202-112">Si cette source n’est pas disponible, le programme d’installation recherche la transformation à la source du package à côté du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="ef202-112">If this source is unavailable, the installer then searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="ef202-113">Pendant une [installation de maintenance](maintenance-installation.md), le programme d’installation recherche la transformation à l’emplacement du cache.</span><span class="sxs-lookup"><span data-stu-id="ef202-113">During a [maintenance installation](maintenance-installation.md), the installer searches for the transform at the cache location.</span></span> <span data-ttu-id="ef202-114">Si la copie mise en cache de la transformation devient indisponible, le programme d’installation recherche la transformation à la source du package à côté du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="ef202-114">If the cached copy of the transform becomes unavailable, the installer searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="ef202-115">Pour plus d’informations, consultez [application de transformations](applying-transforms.md) et [résilience source](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="ef202-115">For more information, see [Applying Transforms](applying-transforms.md) and [Source Resiliency](source-resiliency.md).</span></span>

 

 



