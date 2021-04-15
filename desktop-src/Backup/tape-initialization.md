---
title: Initialisation de la bande
description: Une application doit utiliser la fonction CreateFile pour créer un handle de périphérique à bandes. Ce descripteur est utilisé dans les opérations suivantes sur la bande de l’appareil.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Sauvegarde d’initialisation de bande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463426"
---
# <a name="tape-initialization"></a><span data-ttu-id="7542a-105">Initialisation de la bande</span><span class="sxs-lookup"><span data-stu-id="7542a-105">Tape Initialization</span></span>

<span data-ttu-id="7542a-106">Une application doit utiliser la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour créer un handle de périphérique à bandes.</span><span class="sxs-lookup"><span data-stu-id="7542a-106">An application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to create a handle of a tape device.</span></span> <span data-ttu-id="7542a-107">Ce descripteur est utilisé dans les opérations suivantes sur la bande de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7542a-107">This handle is used in subsequent operations on the tape in the device.</span></span>

<span data-ttu-id="7542a-108">Avant qu’une application n’écrive sur une bande, la bande doit être mise en forme en fonction des besoins de l’application et des fonctionnalités du lecteur de bande utilisé.</span><span class="sxs-lookup"><span data-stu-id="7542a-108">Before an application writes to a tape, the tape must be formatted according to the needs of the application and the capabilities of the tape drive being used.</span></span> <span data-ttu-id="7542a-109">La fonction [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) reformate une bande, en créant un nombre donné de partitions d’une taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7542a-109">The [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) function reformats a tape, creating on it a given number of partitions of a specified size.</span></span>

<span data-ttu-id="7542a-110">La fonction [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prépare l’accès ou la suppression d’une bande.</span><span class="sxs-lookup"><span data-stu-id="7542a-110">The [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) function prepares a tape to be accessed or removed.</span></span> <span data-ttu-id="7542a-111">Cette fonction peut charger, décharger, verrouiller ou déverrouiller une bande.</span><span class="sxs-lookup"><span data-stu-id="7542a-111">This function can load, unload, lock, or unlock a tape.</span></span> <span data-ttu-id="7542a-112">Cette fonction peut également mettre en marche la bande en la déplaçant à la fin de la bande et en la faisant revenir au début.</span><span class="sxs-lookup"><span data-stu-id="7542a-112">This function can also tension the tape by moving the tape to the end of the tape and back to the beginning.</span></span>

<span data-ttu-id="7542a-113">Pour récupérer et définir des informations sur une bande et un lecteur de bande, une application utilise les fonctions [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)et [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .</span><span class="sxs-lookup"><span data-stu-id="7542a-113">To retrieve and set information about a tape and tape drive, an application uses the [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters), and [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) functions.</span></span>

<span data-ttu-id="7542a-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) récupère des informations qui décrivent une bande ou un lecteur de bande.</span><span class="sxs-lookup"><span data-stu-id="7542a-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) retrieves information that describes a tape or a tape drive.</span></span> <span data-ttu-id="7542a-115">Les informations sur la bande incluent le type, la densité et la taille de bloc de la bande ; le nombre de partitions sur la bande ; la quantité de bande restant ; et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="7542a-115">The tape information includes the tape's type, density, and block size; the number of partitions on the tape; the amount of tape remaining; and so on.</span></span> <span data-ttu-id="7542a-116">Les informations sur le lecteur de bande incluent la taille de bloc par défaut du lecteur, le nombre maximal de partitions et les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7542a-116">The tape drive information includes the drive's default block size, the maximum partition count, and the features that are supported.</span></span>

<span data-ttu-id="7542a-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) définit la taille de bloc de bande ou définit les indicateurs de lecteur de bande qui indiquent si le lecteur prend en charge la correction des erreurs matérielles, la compression des données, le remplissage des données ou une combinaison des trois.</span><span class="sxs-lookup"><span data-stu-id="7542a-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) either sets the tape block size or sets the tape drive flags that indicate whether the drive supports hardware error correction, data compression, data padding, or any combination of the three.</span></span>

<span data-ttu-id="7542a-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indique si le lecteur de bande est prêt à traiter les commandes de bande.</span><span class="sxs-lookup"><span data-stu-id="7542a-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indicates whether the tape drive is ready to process tape commands.</span></span>

 

 