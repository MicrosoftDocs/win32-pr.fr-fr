---
description: Les contrôles de l’interface TAPI 3 Rendezvous permettent à un programmeur de créer des applications capables de créer et de découvrir des conférences IP multidiffusion multimédias.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conférence de téléphonie IP Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202827"
---
# <a name="rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="eacdc-103">Conférence de téléphonie IP Rendezvous</span><span class="sxs-lookup"><span data-stu-id="eacdc-103">Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="eacdc-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="eacdc-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eacdc-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="eacdc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="eacdc-106">Les contrôles de l’interface TAPI 3 Rendezvous permettent à un programmeur de créer des applications capables de créer et de découvrir des conférences IP multidiffusion multimédias.</span><span class="sxs-lookup"><span data-stu-id="eacdc-106">The TAPI 3 Rendezvous controls enable a programmer to create applications that can create and discover multimedia multicast IP conferences.</span></span>

<span data-ttu-id="eacdc-107">Les composants clés de rendezvous :</span><span class="sxs-lookup"><span data-stu-id="eacdc-107">The key components of Rendezvous:</span></span>

<span data-ttu-id="eacdc-108">Les [contrôles d’annuaire](directory-controls.md) sont une abstraction des listes de conférences sur un serveur ils ou NTDS.</span><span class="sxs-lookup"><span data-stu-id="eacdc-108">[Directory Controls](directory-controls.md) are an abstraction of conference listings on an ILS or NTDS server.</span></span>

<span data-ttu-id="eacdc-109">Les [contrôles blob de conférence](conference-blob-controls.md) représentent des informations spécifiques à la Conférence, telles que l’heure de démarrage et d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="eacdc-109">[Conference Blob Controls](conference-blob-controls.md) represent conference-specific information such as start and stop time.</span></span> <span data-ttu-id="eacdc-110">Des interfaces spéciales sont fournies pour les blobs de protocole SDP.</span><span class="sxs-lookup"><span data-stu-id="eacdc-110">Special interfaces are provided for SDP protocol blobs.</span></span> <span data-ttu-id="eacdc-111">Pour plus d’informations, consultez la RFC 2327 intitulée « SDP : session Description Protocol ».</span><span class="sxs-lookup"><span data-stu-id="eacdc-111">For detailed information, see RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="eacdc-112">Une copie actuelle de cette RFC peut être localisée à l’aide d’un moteur de recherche Internet.</span><span class="sxs-lookup"><span data-stu-id="eacdc-112">A current copy of this RFC can be located using an Internet search engine.</span></span>

<span data-ttu-id="eacdc-113">Les [interfaces COM de multidiffusion](multicast-com-interfaces.md) sont des wrappers com pour les fonctions MADCAP, anciennement connues sous le titre de MDHCP.</span><span class="sxs-lookup"><span data-stu-id="eacdc-113">[Multicast COM Interfaces](multicast-com-interfaces.md) are COM wrappers for the MADCAP functions, formerly know as MDHCP.</span></span> <span data-ttu-id="eacdc-114">Ces interfaces permettent à une application d’obtenir des adresses de multidiffusion à partir d’un serveur d’allocation d’adresses de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="eacdc-114">These interfaces allow an application to get multicast addresses from a multicast address allocation server.</span></span>

<span data-ttu-id="eacdc-115">Les documents suivants fournissent une vue d’ensemble générale et des exemples d’utilisation des contrôles Rendezvous pour la téléphonie et la conférence IP.</span><span class="sxs-lookup"><span data-stu-id="eacdc-115">The following material provides a general overview and some usage examples of the Rendezvous controls for IP telephony and conferencing.</span></span>

 

 



