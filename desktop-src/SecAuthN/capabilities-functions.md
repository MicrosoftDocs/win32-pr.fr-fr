---
description: L’API du fournisseur réseau spécifie une fonction de fonctions unique.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Fonctions fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034266"
---
# <a name="capabilities-functions"></a><span data-ttu-id="712ff-103">Fonctions fonctions</span><span class="sxs-lookup"><span data-stu-id="712ff-103">Capabilities Functions</span></span>

<span data-ttu-id="712ff-104">L’API du fournisseur réseau spécifie une fonction de fonctions unique.</span><span class="sxs-lookup"><span data-stu-id="712ff-104">The Network Provider API specifies a single capabilities function.</span></span> <span data-ttu-id="712ff-105">Lorsque le système d’exploitation demande des informations sur les fonctionnalités d’un fournisseur de réseau, le [*routeur de fournisseur multiple*](/windows/desktop/SecGloss/m-gly) (MPR) appelle la fonction [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) de chaque fournisseur réseau dont le réseau est actif.</span><span class="sxs-lookup"><span data-stu-id="712ff-105">When the operating system requests information about a network provider's capabilities, the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function of each network provider whose network is active.</span></span>

<span data-ttu-id="712ff-106">La fonction [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) renvoie un masque de masque indiquant les fonctions de l’API du fournisseur réseau prises en charge par le fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="712ff-106">The [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function returns a bitmask indicating which functions of the Network Provider API the network provider supports.</span></span> <span data-ttu-id="712ff-107">La fonction **NPGetCaps** est la seule fonction qu’un fournisseur réseau doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="712ff-107">The **NPGetCaps** function is the only function that a network provider must implement.</span></span> <span data-ttu-id="712ff-108">Le système d’exploitation appelle cette fonction pour déterminer les autres fonctions de l’API du fournisseur réseau prises en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="712ff-108">The operating system calls this function to determine which other functions of the Network Provider API the provider supports.</span></span>

 

 
