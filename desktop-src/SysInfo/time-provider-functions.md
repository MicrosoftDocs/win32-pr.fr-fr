---
description: Les fonctions suivantes sont utilisées par les fournisseurs de temps.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Fonctions du fournisseur de temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519455"
---
# <a name="time-provider-functions"></a><span data-ttu-id="507c0-103">Fonctions du fournisseur de temps</span><span class="sxs-lookup"><span data-stu-id="507c0-103">Time Provider Functions</span></span>

<span data-ttu-id="507c0-104">Les fonctions suivantes sont utilisées par les fournisseurs de temps.</span><span class="sxs-lookup"><span data-stu-id="507c0-104">The following functions are used by time providers.</span></span>



| <span data-ttu-id="507c0-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="507c0-105">Function</span></span>                                                               | <span data-ttu-id="507c0-106">Description</span><span class="sxs-lookup"><span data-stu-id="507c0-106">Description</span></span>                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="507c0-107">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="507c0-107">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | <span data-ttu-id="507c0-108">Informe le système que de nouveaux exemples sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="507c0-108">Notifies the system that there are new samples available.</span></span>                                              |
| [<span data-ttu-id="507c0-109">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="507c0-109">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | <span data-ttu-id="507c0-110">Récupère les informations sur l’état de l’heure système.</span><span class="sxs-lookup"><span data-stu-id="507c0-110">Retrieves the system time state information.</span></span>                                                           |
| [<span data-ttu-id="507c0-111">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="507c0-111">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | <span data-ttu-id="507c0-112">Journalise un événement de fournisseur de temps dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="507c0-112">Logs a time provider event in the event log.</span></span>                                                           |
| [<span data-ttu-id="507c0-113">**SetProviderStatusFunc**</span><span class="sxs-lookup"><span data-stu-id="507c0-113">**SetProviderStatusFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | <span data-ttu-id="507c0-114">Définit les informations d’État du fournisseur de temps.</span><span class="sxs-lookup"><span data-stu-id="507c0-114">Sets the time provider's status information.</span></span>                                                           |
| [<span data-ttu-id="507c0-115">**SetProviderStatusInfoFreeFunc**</span><span class="sxs-lookup"><span data-stu-id="507c0-115">**SetProviderStatusInfoFreeFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | <span data-ttu-id="507c0-116">Libère une structure [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) .</span><span class="sxs-lookup"><span data-stu-id="507c0-116">Frees a [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) structure.</span></span>                          |
| [<span data-ttu-id="507c0-117">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="507c0-117">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | <span data-ttu-id="507c0-118">Fonction de rappel qui est appelée par le gestionnaire de fournisseurs de temps pour arrêter le fournisseur de temps.</span><span class="sxs-lookup"><span data-stu-id="507c0-118">A callback function that is called by the time provider manager to shut down the time provider.</span></span>        |
| [<span data-ttu-id="507c0-119">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="507c0-119">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | <span data-ttu-id="507c0-120">Fonction de rappel qui est appelée par le gestionnaire du fournisseur de temps pour envoyer des commandes au fournisseur de temps.</span><span class="sxs-lookup"><span data-stu-id="507c0-120">A callback function that is called by the time provider manager to send commands to the time provider.</span></span> |
| [<span data-ttu-id="507c0-121">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="507c0-121">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | <span data-ttu-id="507c0-122">Fonction de rappel qui est appelée par le gestionnaire de fournisseur de temps lors du chargement de la DLL du fournisseur de temps.</span><span class="sxs-lookup"><span data-stu-id="507c0-122">A callback function that is called by the time provider manager when the time provider DLL is loaded.</span></span>  |



 

 

 



