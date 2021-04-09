---
description: Les transformations sécurisées sont parfois nécessaires pour des raisons de sécurité.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Transformations sécurisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869041"
---
# <a name="secured-transforms"></a><span data-ttu-id="f0fe8-103">Transformations sécurisées</span><span class="sxs-lookup"><span data-stu-id="f0fe8-103">Secured Transforms</span></span>

<span data-ttu-id="f0fe8-104">Les transformations sécurisées sont parfois nécessaires pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-104">Secured transforms are sometimes necessary for security reasons.</span></span> <span data-ttu-id="f0fe8-105">Les transformations sécurisées sont stockées localement sur l’ordinateur de l’utilisateur dans un emplacement où l’utilisateur n’a pas d’accès en écriture sur un système de fichiers sécurisé.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-105">Secured transforms are stored locally on the user's computer in a location where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="f0fe8-106">Ces transformations sont mises en cache à cet emplacement lors de l’installation ou de la publication du package.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-106">Such transforms are cached in this location during the installation or advertisement of the package.</span></span> <span data-ttu-id="f0fe8-107">Seuls les administrateurs et le système local ont accès en écriture à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-107">Only administrators and local system have write access to this location.</span></span> <span data-ttu-id="f0fe8-108">Un utilisateur non-administrateur ne peut pas modifier le fichier de transformation.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-108">A non-admin user would not be able to modify the transform file.</span></span> <span data-ttu-id="f0fe8-109">Lors des installations ultérieures d’installation à la [demande](installation-on-demand.md) ou de [maintenance](maintenance-installation.md) du package, le programme d’installation utilise les transformations mises en cache.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-109">During subsequent [installation-on-demand](installation-on-demand.md) or [maintenance installations](maintenance-installation.md) of the package, the installer uses the cached transforms.</span></span>

<span data-ttu-id="f0fe8-110">Pour spécifier un stockage de transformation sécurisé, définissez la [stratégie TransformsSecure](transformssecure-policy.md), définissez la propriété [**TransformsSecure**](transformssecure.md) ou transmettez le \| symbole @ ou dans la liste transformations.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-110">To specify secured transform storage, set the [TransformsSecure policy](transformssecure-policy.md), set the [**TRANSFORMSSECURE**](transformssecure.md) property, or pass the @ or \| symbol in the transforms list.</span></span> <span data-ttu-id="f0fe8-111">Notez que vous ne pouvez pas inclure des transformations sécurisées et non sécurisées dans la même liste de transformations.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-111">Note that you cannot include secured and unsecured transforms in the same transforms list.</span></span> <span data-ttu-id="f0fe8-112">Consultez [application de transformations](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="f0fe8-112">See [Applying Transforms](applying-transforms.md).</span></span>

<span data-ttu-id="f0fe8-113">La suppression du produit par un utilisateur supprime toutes les transformations sécurisées pour ce produit de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-113">The removal of the product by any user removes all secured transforms for that product from the user's computer.</span></span>

<span data-ttu-id="f0fe8-114">Si le programme d’installation détecte qu’une transformation sécurisée n’est pas disponible localement, il tente de restaurer le cache de transformation à partir d’une source.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-114">If the installer finds that a secured transform is not locally available, it then attempts to restore the transform cache from a source.</span></span> <span data-ttu-id="f0fe8-115">Les transformations sécurisées peuvent être sécurisées au niveau source ou sécurisé-complet :</span><span class="sxs-lookup"><span data-stu-id="f0fe8-115">Secure transforms can be secure-at-source or secure-full-path:</span></span>

-   <span data-ttu-id="f0fe8-116">Les [transformations sécurisées à la source](secure-at-source-transforms.md) qui manquent dans le cache de transformation local sont restaurées à partir de la racine de la source du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-116">[Secure-at-source transforms](secure-at-source-transforms.md) that are missing from the local transform cache are restored from the root of the source of the .msi file.</span></span>
-   <span data-ttu-id="f0fe8-117">Les [transformations sécurisées de chemin d’accès complet](secure-full-path-transforms.md) qui manquent dans le cache de transformation local sont restaurées à partir du chemin d’accès complet d’origine spécifié par la liste des transformations.</span><span class="sxs-lookup"><span data-stu-id="f0fe8-117">[Secure-full-path transforms](secure-full-path-transforms.md) that are missing from the local transform cache are restored from the original full path specified by the transforms list.</span></span>

 

 



