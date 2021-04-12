---
description: Les fonctions de redirection de l’appareil redirigent les périphériques MS-DOS standard, les lettres de lecteur et les ports LPT. Cela permet aux applications qui s’exécutent sur le système d’utiliser les appareils et d’accéder au réseau de manière totalement transparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Fonctions Device-Redirecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201248"
---
# <a name="device-redirecting-functions"></a><span data-ttu-id="ab739-104">Fonctions Device-Redirecting</span><span class="sxs-lookup"><span data-stu-id="ab739-104">Device-Redirecting Functions</span></span>

<span data-ttu-id="ab739-105">Les fonctions de redirection de l’appareil redirigent les périphériques MS-DOS standard, les lettres de lecteur et les ports LPT.</span><span class="sxs-lookup"><span data-stu-id="ab739-105">The device-redirecting functions redirect standard MS-DOS devices, drive letters and LPT ports.</span></span> <span data-ttu-id="ab739-106">Cela permet aux applications qui s’exécutent sur le système d’utiliser les appareils et d’accéder au réseau de manière totalement transparente.</span><span class="sxs-lookup"><span data-stu-id="ab739-106">This enables applications running on the system to use the devices and access the network in a totally transparent manner.</span></span>



| <span data-ttu-id="ab739-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="ab739-107">Function</span></span>                                                         | <span data-ttu-id="ab739-108">Description</span><span class="sxs-lookup"><span data-stu-id="ab739-108">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab739-109">**NPAddConnection**</span><span class="sxs-lookup"><span data-stu-id="ab739-109">**NPAddConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | <span data-ttu-id="ab739-110">Redirige ou connecte un appareil local à une ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="ab739-110">Redirects or connects a local device to a network resource.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="ab739-111">**NPAddConnection3**</span><span class="sxs-lookup"><span data-stu-id="ab739-111">**NPAddConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | <span data-ttu-id="ab739-112">Effectue la même action que [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), mais permet à l’utilisateur de spécifier quelle fenêtre doit posséder toutes les boîtes de dialogue et comment la connexion doit être établie.</span><span class="sxs-lookup"><span data-stu-id="ab739-112">Performs the same action as [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), but lets the user specify which window should own any dialog boxes and how the connection should be established.</span></span><br/> |
| [<span data-ttu-id="ab739-113">**NPCancelConnection**</span><span class="sxs-lookup"><span data-stu-id="ab739-113">**NPCancelConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | <span data-ttu-id="ab739-114">Interrompt une connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="ab739-114">Breaks a network connection.</span></span> <span data-ttu-id="ab739-115">Les modifications sont mémorisées si un appareil est déconnecté, sauf si la connexion est une connexion sans appareil.</span><span class="sxs-lookup"><span data-stu-id="ab739-115">The changes are remembered if a device is disconnected unless the connection is a deviceless connection.</span></span><br/>                                                    |
| [<span data-ttu-id="ab739-116">**NPGetConnection**</span><span class="sxs-lookup"><span data-stu-id="ab739-116">**NPGetConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | <span data-ttu-id="ab739-117">Retourne des informations sur une connexion.</span><span class="sxs-lookup"><span data-stu-id="ab739-117">Returns information about a connection.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="ab739-118">**NPGetConnection3**</span><span class="sxs-lookup"><span data-stu-id="ab739-118">**NPGetConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | <span data-ttu-id="ab739-119">Retourne des informations sur une connexion, même si la connexion est actuellement déconnectée.</span><span class="sxs-lookup"><span data-stu-id="ab739-119">Returns information about a connection, even if the connection is currently disconnected.</span></span><br/>                                                                                                |
| [<span data-ttu-id="ab739-120">**NPGetConnectionPerformance**</span><span class="sxs-lookup"><span data-stu-id="ab739-120">**NPGetConnectionPerformance**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | <span data-ttu-id="ab739-121">Retourne les informations de performance relatives à une connexion.</span><span class="sxs-lookup"><span data-stu-id="ab739-121">Returns performance information about a connection.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="ab739-122">**NPGetUniversalName**</span><span class="sxs-lookup"><span data-stu-id="ab739-122">**NPGetUniversalName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | <span data-ttu-id="ab739-123">Retourne le nom universel local ou distant, au format spécifié lors de l’appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ab739-123">Returns the remote or local universal name, in the format specified during the function call.</span></span><br/>                                                                                            |



 

 

 




