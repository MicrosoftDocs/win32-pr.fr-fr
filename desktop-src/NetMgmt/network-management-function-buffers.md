---
title: Mémoires tampons de fonctions de gestion de réseau
description: La bibliothèque Runtime RPC gère les tampons requis par les fonctions de gestion de réseau de l’extraction de données 32 bits comme suit.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196916"
---
# <a name="network-management-function-buffers"></a><span data-ttu-id="0072f-103">Mémoires tampons de fonctions de gestion de réseau</span><span class="sxs-lookup"><span data-stu-id="0072f-103">Network Management Function Buffers</span></span>

<span data-ttu-id="0072f-104">La bibliothèque Runtime RPC gère les tampons requis par les fonctions de gestion de réseau de l’extraction de données 32 bits comme suit :</span><span class="sxs-lookup"><span data-stu-id="0072f-104">The RPC run-time library handles the buffers required by the 32-bit data retrieval network management functions as follows:</span></span>

-   <span data-ttu-id="0072f-105">**Envoi de données au serveur** (données spécifiées par les \[ \] paramètres in).</span><span class="sxs-lookup"><span data-stu-id="0072f-105">**Sending data to the server** (data specified by \[in\] parameters).</span></span>

    <span data-ttu-id="0072f-106">L’appelant doit allouer et libérer la mémoire tampon pour la structure d’informations (ou structures) appropriée et passer une variable pointeur à la fonction.</span><span class="sxs-lookup"><span data-stu-id="0072f-106">The caller must allocate and deallocate the buffer for the relevant information structure (or structures) and pass a pointer variable to the function.</span></span> <span data-ttu-id="0072f-107">L’appelant n’a pas besoin de spécifier la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0072f-107">The caller does not need to specify the buffer length.</span></span>

    <span data-ttu-id="0072f-108">Exemple : [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span><span class="sxs-lookup"><span data-stu-id="0072f-108">Example: [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span></span>

-   <span data-ttu-id="0072f-109">**Récupération de données à partir du serveur** (données spécifiées par les \[ \] paramètres out).</span><span class="sxs-lookup"><span data-stu-id="0072f-109">**Retrieving data from the server** (data specified by \[out\] parameters).</span></span>

    <span data-ttu-id="0072f-110">Le système alloue la mémoire tampon pour les informations retournées.</span><span class="sxs-lookup"><span data-stu-id="0072f-110">The system allocates the buffer for the returned information.</span></span> <span data-ttu-id="0072f-111">L’appelant doit passer une variable pointeur à la fonction en entrée.</span><span class="sxs-lookup"><span data-stu-id="0072f-111">The caller must pass a pointer variable to the function on input.</span></span> <span data-ttu-id="0072f-112">En cas de retour réussi, le pointeur reçoit l’adresse de la mémoire tampon allouée par le système qui contient les informations retournées.</span><span class="sxs-lookup"><span data-stu-id="0072f-112">On successful return, the pointer receives the address of the system-allocated buffer that contains the returned information.</span></span> <span data-ttu-id="0072f-113">Cela simplifie le code appelant, car l’appelant n’a pas besoin d’estimer la taille de la mémoire tampon, ou de redimensionner la mémoire tampon et de réexécuter la fonction.</span><span class="sxs-lookup"><span data-stu-id="0072f-113">This simplifies the calling code, because the caller does not need to estimate the size of the buffer, or resize the buffer and reissue the function.</span></span>

    <span data-ttu-id="0072f-114">Lorsque l’appelant a terminé de traiter les informations renvoyées, il doit libérer la mémoire allouée par le système en appelant la fonction [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) .</span><span class="sxs-lookup"><span data-stu-id="0072f-114">When the caller has finished processing the returned information, it must free the system-allocated memory by calling the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function.</span></span> <span data-ttu-id="0072f-115">Pour plus d’informations sur la spécification des tailles de mémoire tampon, consultez [Lengths de la mémoire tampon des fonctions de gestion réseau](network-management-function-buffer-lengths.md).</span><span class="sxs-lookup"><span data-stu-id="0072f-115">For more information about specifying buffer sizes, see [Network Management Function Buffer Lengths](network-management-function-buffer-lengths.md).</span></span>

    <span data-ttu-id="0072f-116">Exemple : [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span><span class="sxs-lookup"><span data-stu-id="0072f-116">Example: [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span></span>

 

 




