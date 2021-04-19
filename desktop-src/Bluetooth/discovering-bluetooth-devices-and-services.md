---
title: Détection des appareils et services Bluetooth
description: Pour faciliter la découverte des appareils et services Bluetooth, Windows mappe le protocole de détection de service Bluetooth (SDP) sur les interfaces d’espace de noms Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tâches, détection des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "106527554"
---
# <a name="discovering-bluetooth-devices-and-services"></a><span data-ttu-id="cfccc-104">Détection des appareils et services Bluetooth</span><span class="sxs-lookup"><span data-stu-id="cfccc-104">Discovering Bluetooth Devices and Services</span></span>

<span data-ttu-id="cfccc-105">Pour faciliter la découverte des appareils et services Bluetooth, Windows mappe le protocole de détection de service Bluetooth (SDP) sur les interfaces d’espace de noms Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="cfccc-105">To facilitate the discovery of Bluetooth devices and services, Windows maps the Bluetooth Service Discovery Protocol (SDP) onto the Windows Sockets namespace interfaces.</span></span> <span data-ttu-id="cfccc-106">Les fonctions principales utilisées pour ce mappage sont les fonctions [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)et [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) .</span><span class="sxs-lookup"><span data-stu-id="cfccc-106">The primary functions used for this mapping are the [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) functions.</span></span> <span data-ttu-id="cfccc-107">La structure [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) est également utilisée conjointement avec ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="cfccc-107">The [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure is also used in conjunction with these functions.</span></span>

<span data-ttu-id="cfccc-108">Étant donné que certains concepts et paramètres du SDP Bluetooth ne sont pas nécessairement mappés directement dans la structure [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) , vous devez faire attention à la façon dont les membres sont créés et utilisés.</span><span class="sxs-lookup"><span data-stu-id="cfccc-108">Because certain concepts and parameters from the Bluetooth SDP do not necessarily map directly into the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure, attention must be paid to how its members are created and used.</span></span> <span data-ttu-id="cfccc-109">Pour de nombreuses opérations Bluetooth complexes, telles que la création d’enregistrements SDP, le membre **lpBlob** du **WSAQUERYSET** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cfccc-109">For many complex Bluetooth operations, such as the creation of SDP records, the **lpBlob** member of the **WSAQUERYSET** is used.</span></span> <span data-ttu-id="cfccc-110">Lorsqu’une telle considération particulière est nécessaire, elle est spécifiquement décrite, par exemple dans les pages de référence telles que [**Bluetooth et WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), entre autres.</span><span class="sxs-lookup"><span data-stu-id="cfccc-110">When such special consideration is necessary, it is specifically described, such as in reference pages like [**Bluetooth and WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and others.</span></span>

<span data-ttu-id="cfccc-111">Il est important de comprendre que l’inscription SDP est distincte du contrôle Socket.</span><span class="sxs-lookup"><span data-stu-id="cfccc-111">It is important to understand that SDP registration is separate from socket control.</span></span> <span data-ttu-id="cfccc-112">Quand une application serveur est préparée à accepter la connexion cliente, elle doit appeler la fonction [**WSASetService**](bluetooth-and-wsasetservice.md) pour inscrire un enregistrement SDP Bluetooth qui correspond à ce service.</span><span class="sxs-lookup"><span data-stu-id="cfccc-112">When a server application is prepared to accept client connection, it should call the [**WSASetService**](bluetooth-and-wsasetservice.md) function to register a Bluetooth SDP record that corresponds to that service.</span></span> <span data-ttu-id="cfccc-113">Cette application Bluetooth doit rappeler la fonction **WSASetService** avant de fermer, pour annuler l’inscription de l’enregistrement SDP Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="cfccc-113">That Bluetooth application must call the **WSASetService** function again before closing, to deregister the Bluetooth SDP record.</span></span>

<span data-ttu-id="cfccc-114">Lorsque vous utilisez les fonctions de mappage décrites sur cette page, l' \_ espace de noms NS BTH est assigné.</span><span class="sxs-lookup"><span data-stu-id="cfccc-114">When using the mapping functions described on this page, the NS\_BTH namespace is assigned.</span></span>

<span data-ttu-id="cfccc-115">Pour plus d’informations sur la découverte des appareils et des services, consultez les pages de référence suivantes :</span><span class="sxs-lookup"><span data-stu-id="cfccc-115">For further information about discovering devices and services, consult the following reference pages:</span></span>

-   [<span data-ttu-id="cfccc-116">**Bluetooth et WSASetService**</span><span class="sxs-lookup"><span data-stu-id="cfccc-116">**Bluetooth and WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
-   [<span data-ttu-id="cfccc-117">**Bluetooth et WSALookupServiceBegin pour la consultation des appareils**</span><span class="sxs-lookup"><span data-stu-id="cfccc-117">**Bluetooth and WSALookupServiceBegin for Device Inquiry**</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [<span data-ttu-id="cfccc-118">**Bluetooth et WSALookupServiceBegin pour la détection de service**</span><span class="sxs-lookup"><span data-stu-id="cfccc-118">**Bluetooth and WSALookupServiceBegin for Service Discovery**</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [<span data-ttu-id="cfccc-119">**Bluetooth et WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="cfccc-119">**Bluetooth and WSALookupServiceNext**</span></span>](bluetooth-and-wsalookupservicenext.md)
-   [<span data-ttu-id="cfccc-120">**Bluetooth et WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="cfccc-120">**Bluetooth and WSALookupServiceEnd**</span></span>](bluetooth-and-wsalookupserviceend.md)
-   [<span data-ttu-id="cfccc-121">**Bluetooth et objet BLOB**</span><span class="sxs-lookup"><span data-stu-id="cfccc-121">**Bluetooth and BLOB**</span></span>](bluetooth-and-blob.md)
-   [<span data-ttu-id="cfccc-122">**Bluetooth et WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="cfccc-122">**Bluetooth and WSAQUERYSET**</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)

<span data-ttu-id="cfccc-123">Vous pouvez également télécharger l' [exemple de connexion Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) pour obtenir un exemple complet.</span><span class="sxs-lookup"><span data-stu-id="cfccc-123">You can also download the [Bluetooth connection sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) for a complete example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfccc-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cfccc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfccc-125">Programmation Bluetooth avec Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="cfccc-125">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[<span data-ttu-id="cfccc-126">Exemple de connexion Bluetooth</span><span class="sxs-lookup"><span data-stu-id="cfccc-126">Bluetooth connection sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




