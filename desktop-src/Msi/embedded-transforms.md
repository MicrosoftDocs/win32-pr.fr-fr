---
description: Les transformations incorporées sont stockées dans le fichier. msi du package. Cela garantit aux utilisateurs que la transformation est toujours disponible lorsque le package d’installation est disponible. Les transformations peuvent également être fournies aux utilisateurs en tant que fichiers. MST autonomes.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Transformations incorporées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034642"
---
# <a name="embedded-transforms"></a><span data-ttu-id="4df62-105">Transformations incorporées</span><span class="sxs-lookup"><span data-stu-id="4df62-105">Embedded Transforms</span></span>

<span data-ttu-id="4df62-106">Les transformations incorporées sont stockées dans le fichier. msi du package.</span><span class="sxs-lookup"><span data-stu-id="4df62-106">Embedded transforms are stored inside the .msi file of the package.</span></span> <span data-ttu-id="4df62-107">Cela garantit aux utilisateurs que la transformation est toujours disponible lorsque le package d’installation est disponible.</span><span class="sxs-lookup"><span data-stu-id="4df62-107">This guarantees to users that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="4df62-108">Les transformations peuvent également être fournies aux utilisateurs en tant que fichiers. MST autonomes.</span><span class="sxs-lookup"><span data-stu-id="4df62-108">Alternatively, transforms may be provided to users as standalone .mst files.</span></span>

<span data-ttu-id="4df62-109">Pour ajouter une transformation incorporée à la liste des transformations, ajoutez un signe deux-points ( :) préfixe du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="4df62-109">To add an embedded transform to the transforms list, add a colon (:) prefix to the file name.</span></span> <span data-ttu-id="4df62-110">Étant donné que le programme d’installation peut toujours obtenir la transformation à partir du stockage dans le fichier. msi, les transformations incorporées ne sont pas mises en cache sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4df62-110">Because the installer can always obtain the transform from storage in the .msi file, embedded transforms are not cached on the user's computer.</span></span> <span data-ttu-id="4df62-111">Les transformations incorporées peuvent être utilisées en association avec des transformations [sécurisées](secured-transforms.md) ou des [transformations non sécurisées](unsecured-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="4df62-111">Embedded transforms may be used in combination with [secured transforms](secured-transforms.md) or [unsecured transforms](unsecured-transforms.md).</span></span> <span data-ttu-id="4df62-112">Pour plus d’informations, consultez [application de transformations](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="4df62-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



