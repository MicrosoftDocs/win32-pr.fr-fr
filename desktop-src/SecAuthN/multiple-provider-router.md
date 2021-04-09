---
description: Le routeur de fournisseur multiple gère la communication entre le système d’exploitation Windows et les fournisseurs de réseau installés. Il permet à Windows de présenter un réseau intégré à l’utilisateur.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Routeur à plusieurs fournisseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867246"
---
# <a name="multiple-provider-router"></a><span data-ttu-id="33101-104">Routeur à plusieurs fournisseurs</span><span class="sxs-lookup"><span data-stu-id="33101-104">Multiple Provider Router</span></span>

<span data-ttu-id="33101-105">Le [*routeur de fournisseur multiple*](../secgloss/m-gly.md) gère la communication entre le système d’exploitation Windows et les fournisseurs de réseau installés.</span><span class="sxs-lookup"><span data-stu-id="33101-105">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication between the Windows operating system and the installed network providers.</span></span> <span data-ttu-id="33101-106">Il permet à Windows de présenter un réseau intégré à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="33101-106">It enables Windows to present an integrated network to the user.</span></span>

<span data-ttu-id="33101-107">Au démarrage de MPR, il vérifie le registre pour déterminer quels fournisseurs de réseau sont installés sur le système et l’ordre dans lequel ils doivent être recycles.</span><span class="sxs-lookup"><span data-stu-id="33101-107">When the MPR starts, it checks the registry to determine which network providers are installed on the system and the order they should be cycled through.</span></span> <span data-ttu-id="33101-108">Il charge toutes les dll de fournisseur réseau inscrites et les utilise pour traiter les appels WNet suivants effectués par l’interface utilisateur ou d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="33101-108">It loads all registered network provider DLLs and uses them to process subsequent WNet calls made by the user interface or other applications.</span></span>

<span data-ttu-id="33101-109">Pour plus d’informations sur les fonctions WNet, consultez [mise en réseau Windows](../wnet/windows-networking-wnet-.md).</span><span class="sxs-lookup"><span data-stu-id="33101-109">For more information about WNet functions, see [Windows Networking](../wnet/windows-networking-wnet-.md).</span></span>

 

 
