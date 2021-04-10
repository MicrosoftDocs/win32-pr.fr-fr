---
description: Le fragment de code suivant montre comment demander et définir une adresse de multidiffusion pour une conférence.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Acquisition d’une adresse de multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112614"
---
# <a name="acquiring-a-multicast-address"></a><span data-ttu-id="ef178-103">Acquisition d’une adresse de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="ef178-103">Acquiring a Multicast Address</span></span>

<span data-ttu-id="ef178-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ef178-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ef178-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="ef178-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ef178-106">Le fragment de code suivant montre comment demander et définir une adresse de multidiffusion pour une conférence.</span><span class="sxs-lookup"><span data-stu-id="ef178-106">The following code fragment illustrates how to request and set a multicast address for a conference.</span></span>

<span data-ttu-id="ef178-107">Par souci de simplicité, ce fragment montre l’affectation d’une adresse de multidiffusion à un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="ef178-107">For the sake of simplicity, this fragment shows the assignment of one multicast address to one media item.</span></span> <span data-ttu-id="ef178-108">En réalité, la sélection d’une étendue, la demande d’adresse de multidiffusion et l’attribution sont effectuées pour chaque élément multimédia impliqué dans la Conférence.</span><span class="sxs-lookup"><span data-stu-id="ef178-108">In actuality, the selection of a scope, the multicast address request, and the assignment will be performed for every media item involved in the conference.</span></span>

<span data-ttu-id="ef178-109">Ce fragment part du principe que la [connexion à un serveur ils](connecting-to-an-ils-server.md) a déjà été effectuée.</span><span class="sxs-lookup"><span data-stu-id="ef178-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span> <span data-ttu-id="ef178-110">Les opérations présentées ici sont effectuées dans la section « modifier les paramètres si nécessaire » de la rubrique [création d’une annonce de conférence](creating-a-conference-announcement.md).</span><span class="sxs-lookup"><span data-stu-id="ef178-110">The operations shown here would be performed in the "Modify the settings if necessary" section of [Creating a Conference Announcement](creating-a-conference-announcement.md).</span></span>


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a><span data-ttu-id="ef178-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef178-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef178-112">Interfaces COM de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="ef178-112">Multicast COM Interfaces</span></span>](multicast-com-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ef178-113">**IMcastAddressAllocation**</span><span class="sxs-lookup"><span data-stu-id="ef178-113">**IMcastAddressAllocation**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[<span data-ttu-id="ef178-114">**IMcastScope**</span><span class="sxs-lookup"><span data-stu-id="ef178-114">**IMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[<span data-ttu-id="ef178-115">**IMcastLeaseInfo**</span><span class="sxs-lookup"><span data-stu-id="ef178-115">**IMcastLeaseInfo**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[<span data-ttu-id="ef178-116">**IEnumMcastScope**</span><span class="sxs-lookup"><span data-stu-id="ef178-116">**IEnumMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[<span data-ttu-id="ef178-117">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="ef178-117">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="ef178-118">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="ef178-118">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="ef178-119">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="ef178-119">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="ef178-120">**IEnumBstr**</span><span class="sxs-lookup"><span data-stu-id="ef178-120">**IEnumBstr**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[<span data-ttu-id="ef178-121">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="ef178-121">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="ef178-122">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="ef178-122">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 



