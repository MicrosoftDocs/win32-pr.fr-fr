---
description: Un fournisseur de temps est implémenté en tant que DLL. Chaque DLL peut prendre en charge plusieurs fournisseurs de temps. Chaque fournisseur est responsable de sa propre configuration et de sa propre synchronisation.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Création d’un fournisseur de temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531226"
---
# <a name="creating-a-time-provider"></a><span data-ttu-id="eaf71-105">Création d’un fournisseur de temps</span><span class="sxs-lookup"><span data-stu-id="eaf71-105">Creating a Time Provider</span></span>

<span data-ttu-id="eaf71-106">Un fournisseur de temps est implémenté en tant que DLL.</span><span class="sxs-lookup"><span data-stu-id="eaf71-106">A time provider is implemented as a DLL.</span></span> <span data-ttu-id="eaf71-107">Chaque DLL peut prendre en charge plusieurs fournisseurs de temps.</span><span class="sxs-lookup"><span data-stu-id="eaf71-107">Each DLL can support multiple time providers.</span></span> <span data-ttu-id="eaf71-108">Chaque fournisseur est responsable de sa propre configuration et de sa propre synchronisation.</span><span class="sxs-lookup"><span data-stu-id="eaf71-108">Each provider is responsible for its own configuration and synchronization.</span></span>

<span data-ttu-id="eaf71-109">Les fournisseurs de temps doivent implémenter les fonctions de rappel suivantes :</span><span class="sxs-lookup"><span data-stu-id="eaf71-109">Time providers must implement the following callback functions:</span></span>

-   [<span data-ttu-id="eaf71-110">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="eaf71-110">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [<span data-ttu-id="eaf71-111">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="eaf71-111">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [<span data-ttu-id="eaf71-112">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="eaf71-112">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

<span data-ttu-id="eaf71-113">Une fois la DLL du fournisseur chargée, le gestionnaire de fournisseurs de temps appelle [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), en passant le nom du fournisseur et les pointeurs aux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="eaf71-113">After it has loaded the provider DLL, the time provider manager calls [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passing the name of the provider and pointers to the following functions:</span></span>

-   [<span data-ttu-id="eaf71-114">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="eaf71-114">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [<span data-ttu-id="eaf71-115">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="eaf71-115">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [<span data-ttu-id="eaf71-116">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="eaf71-116">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

<span data-ttu-id="eaf71-117">Ces fonctions sont utilisées par le fournisseur de temps.</span><span class="sxs-lookup"><span data-stu-id="eaf71-117">These functions are for use by the time provider.</span></span> <span data-ttu-id="eaf71-118">Le fournisseur de temps utilise [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) pour retourner un handle de fournisseur que le gestionnaire de fournisseurs de temps utilise lors de l’envoi de commandes au fournisseur de temps.</span><span class="sxs-lookup"><span data-stu-id="eaf71-118">The time provider uses [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) to return a provider handle that the time provider manager uses when sending commands to the time provider.</span></span> <span data-ttu-id="eaf71-119">La valeur de handle est définie par le fournisseur de temps et est utilisée principalement pour faire la distinction entre les différents fournisseurs implémentés dans la même DLL.</span><span class="sxs-lookup"><span data-stu-id="eaf71-119">The handle value is defined by the time provider and is used primarily to distinguish between different providers implemented in the same DLL.</span></span> <span data-ttu-id="eaf71-120">Le fournisseur de temps peut consigner des événements importants à l’aide de [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span><span class="sxs-lookup"><span data-stu-id="eaf71-120">The time provider can log significant events using [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span></span>

<span data-ttu-id="eaf71-121">Le gestionnaire de fournisseurs de temps utilise [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) pour envoyer des commandes au fournisseur de temps.</span><span class="sxs-lookup"><span data-stu-id="eaf71-121">The time provider manager uses [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) to send commands to the time provider.</span></span> <span data-ttu-id="eaf71-122">Lorsque le fournisseur de temps doit informer le gestionnaire de fournisseurs de temps qu’il dispose d’exemples de temps disponibles, il appelle [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span><span class="sxs-lookup"><span data-stu-id="eaf71-122">When the time provider needs to notify the time provider manager that it has time samples available, it calls [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span></span> <span data-ttu-id="eaf71-123">Le gestionnaire de fournisseurs de temps appelle ensuite **TimeProvCommand** avec la \_ commande TPC getSamples pour récupérer les échantillons d’heure.</span><span class="sxs-lookup"><span data-stu-id="eaf71-123">The time provider manager then calls **TimeProvCommand** with the TPC\_GetSamples command to retrieve the time samples.</span></span> <span data-ttu-id="eaf71-124">Il peut falloir jusqu’à 16 secondes pour que le gestionnaire de fournisseurs de temps demande l’exemple.</span><span class="sxs-lookup"><span data-stu-id="eaf71-124">It can take up to 16 seconds for the time provider manager to request the sample.</span></span> <span data-ttu-id="eaf71-125">Par conséquent, l’application ne doit pas attendre la demande.</span><span class="sxs-lookup"><span data-stu-id="eaf71-125">Therefore, the application should not wait for the request.</span></span>

<span data-ttu-id="eaf71-126">Pour garantir la précision, le fournisseur de temps doit récupérer toutes les informations relatives au temps à l’aide de [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span><span class="sxs-lookup"><span data-stu-id="eaf71-126">To ensure accuracy, the time provider should retrieve all time-related information using [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span></span>

<span data-ttu-id="eaf71-127">Lorsqu’il est temps d’arrêter le fournisseur de temps, le gestionnaire de fournisseurs de temps appelle [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span><span class="sxs-lookup"><span data-stu-id="eaf71-127">When it is time to shut down the time provider, the time provider manager calls [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span></span>

 

 



