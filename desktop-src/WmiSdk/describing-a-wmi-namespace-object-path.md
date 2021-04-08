---
description: Un chemin d’accès d’objet d’espace de noms décrit l’emplacement d’un espace de noms particulier sur un serveur. Un chemin d’accès à un objet d’espace de noms contient des éléments de serveur et d’espace de noms.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Description d’un chemin d’accès d’objet d’espace de noms WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034310"
---
# <a name="describing-a-wmi-namespace-object-path"></a><span data-ttu-id="02516-104">Description d’un chemin d’accès d’objet d’espace de noms WMI</span><span class="sxs-lookup"><span data-stu-id="02516-104">Describing a WMI Namespace Object Path</span></span>

<span data-ttu-id="02516-105">Un chemin d’accès d’objet d’espace de noms décrit l’emplacement d’un espace de noms particulier sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="02516-105">A namespace object path describes the location of a particular namespace on a server.</span></span> <span data-ttu-id="02516-106">Un chemin d’accès à un objet d’espace de noms contient des éléments de serveur et d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="02516-106">A namespace object path contains server and namespace elements, and is formatted using either forward or backward slashes.</span></span>

<span data-ttu-id="02516-107">L’élément Server spécifie le nom réseau de l’ordinateur qui héberge l’espace de noms, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="02516-107">The server element specifies the network name of the computer that is hosting the namespace, as shown in the following example.</span></span>

``` syntax
\\Server\Namespace
```

<span data-ttu-id="02516-108">\- ou -</span><span class="sxs-lookup"><span data-stu-id="02516-108">\- or -</span></span>

``` syntax
//Server/Namespace
```

<span data-ttu-id="02516-109">Si le serveur est l’ordinateur local, utilisez un point unique au lieu du nom du serveur, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="02516-109">If the server is the local computer, use a single dot instead of the server name, as shown in the following example.</span></span>

``` syntax
\\.\Namespace
```

<span data-ttu-id="02516-110">L’élément namespace spécifie un espace de noms valide.</span><span class="sxs-lookup"><span data-stu-id="02516-110">The namespace element specifies any valid namespace.</span></span> <span data-ttu-id="02516-111">Un espace de noms est représenté par une chaîne hiérarchique contenant des éléments délimités par des barres obliques inverses uniques, telles que \\ cimv2 racine.</span><span class="sxs-lookup"><span data-stu-id="02516-111">A namespace is represented with a hierarchical string containing elements delimited by single backslashes, such as root\\cimv2.</span></span> <span data-ttu-id="02516-112">Vous ne pouvez pas utiliser les barres obliques dans les noms d’espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="02516-112">You cannot use forward slashes within namespace names.</span></span>

 

 



