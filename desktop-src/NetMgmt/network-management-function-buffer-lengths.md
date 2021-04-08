---
title: Longueur de la mémoire tampon des fonctions de gestion de réseau
description: Cette rubrique décrit la configuration requise pour les longueurs de mémoire tampon de fonction lorsqu’elle est utilisée avec les API de gestion de réseau.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840117"
---
# <a name="network-management-function-buffer-lengths"></a><span data-ttu-id="7b5cc-103">Longueur de la mémoire tampon des fonctions de gestion de réseau</span><span class="sxs-lookup"><span data-stu-id="7b5cc-103">Network Management Function Buffer Lengths</span></span>

<span data-ttu-id="7b5cc-104">Cette rubrique décrit la configuration requise pour les longueurs de mémoire tampon de fonction lorsqu’elle est utilisée avec les API de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-104">This topic discusses the requirements for function buffer lengths when used with the network management APIs.</span></span>

<span data-ttu-id="7b5cc-105">Les applications qui spécifient des tailles de mémoire tampon lors de l’appel de fonctions d’énumération de gestion de réseau (et diverses fonctions de récupération de données) doivent spécifier des mémoires tampons suffisamment grandes pour contenir la structure d’informations (ou structures) retournées, ainsi que les chaînes auxquelles leurs membres pointent.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-105">Applications that specify buffer sizes when calling network management enumeration functions (and various data retrieval functions) must specify buffers large enough to hold the returned information structure (or structures) plus the strings to which their members point.</span></span> <span data-ttu-id="7b5cc-106">Si vous ne spécifiez pas de mémoire tampon suffisamment grande pour recevoir toutes les entrées disponibles, la fonction retourne l’erreur \_ plus de \_ données.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-106">If you do not specify a large enough buffer to receive all the available entries, the function returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="7b5cc-107">Les appels d’énumération ne retournent pas d’entrées partielles.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-107">Enumeration calls do not return partial entries.</span></span>

<span data-ttu-id="7b5cc-108">Certaines fonctions de gestion de réseau prennent un paramètre de longueur de données maximal de l’avis, *prefmaxlen*.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-108">Some network management functions take an advisory maximum data-length parameter, *prefmaxlen*.</span></span> <span data-ttu-id="7b5cc-109">Ce paramètre permet à une application de suggérer le nombre d’octets que le serveur doit retourner à partir d’un appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-109">This parameter allows an application to suggest the number of bytes the server should return from a function call.</span></span>

<span data-ttu-id="7b5cc-110">Si vous spécifiez la valeur MAX \_ préférée \_ Length dans le paramètre *prefmaxlen* , les fonctions de gestion de réseau allouent la quantité de mémoire requise pour les données.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-110">If you specify the value MAX\_PREFERRED\_LENGTH in the *prefmaxlen* parameter, the network management functions allocate the amount of memory required for the data.</span></span>

<span data-ttu-id="7b5cc-111">Pour plus d’informations, consultez [mémoires tampons de fonctions de gestion de réseau](network-management-function-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="7b5cc-111">For more information, see [Network Management Function Buffers](network-management-function-buffers.md).</span></span>

 

 




