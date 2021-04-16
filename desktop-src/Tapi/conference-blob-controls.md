---
description: Le diagramme suivant illustre les principaux objets impliqués dans les contrôles blob de conférence TAPI 3. Les interfaces affichées sont des liens hypertexte vers les pages de référence appropriées.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Contrôles blob de conférence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527225"
---
# <a name="conference-blob-controls"></a><span data-ttu-id="1603e-104">Contrôles blob de conférence</span><span class="sxs-lookup"><span data-stu-id="1603e-104">Conference Blob Controls</span></span>

<span data-ttu-id="1603e-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1603e-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1603e-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1603e-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1603e-107">Le diagramme suivant illustre les principaux objets impliqués dans les contrôles blob de conférence TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="1603e-107">The following diagram illustrates the main objects involved in TAPI 3 conference blob controls.</span></span> <span data-ttu-id="1603e-108">Les interfaces affichées sont des liens hypertexte vers les pages de référence appropriées.</span><span class="sxs-lookup"><span data-stu-id="1603e-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![interfaces et contrôles d’objet blob de conférence](images/rendblob.png)

<span data-ttu-id="1603e-110">L’objet blob de conférence contient des informations spécifiques au fournisseur sur un objet de conférence.</span><span class="sxs-lookup"><span data-stu-id="1603e-110">The conference blob contains provider-specific information on a conference object.</span></span> <span data-ttu-id="1603e-111">Un pointeur vers l’objet blob d’interface [**ITConferenceBlob**](itconferenceblob.md) est obtenu en exécutant QueryInterface sur [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span><span class="sxs-lookup"><span data-stu-id="1603e-111">A pointer to the [**ITConferenceBlob**](itconferenceblob.md) interface blob is obtained by doing a QueryInterface on [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span></span> <span data-ttu-id="1603e-112">L’interface **ITConferenceBlob** fournit des méthodes pour la manipulation de base d’un objet blob de conférence générique.</span><span class="sxs-lookup"><span data-stu-id="1603e-112">The **ITConferenceBlob** interface provides methods for basic manipulation of a generic conference blob.</span></span> <span data-ttu-id="1603e-113">Une application utilisant des objets BLOB de conférence non-SDP doit implémenter ses propres méthodes pour la manipulation détaillée.</span><span class="sxs-lookup"><span data-stu-id="1603e-113">An application using non-SDP conference blobs must implement its own methods for detail manipulation.</span></span>

<span data-ttu-id="1603e-114">Rendezvous fournit l’interface [**ITSdp**](itsdp.md) pour manipuler les objets BLOB de conférence SDP.</span><span class="sxs-lookup"><span data-stu-id="1603e-114">Rendezvous provides the [**ITSdp**](itsdp.md) interface for manipulating SDP conference blobs.</span></span> <span data-ttu-id="1603e-115">Le SDP est un protocole permettant de décrire les sessions multimédias et leurs informations de planification associées.</span><span class="sxs-lookup"><span data-stu-id="1603e-115">The SDP is a protocol for describing multimedia sessions and their related scheduling information.</span></span> <span data-ttu-id="1603e-116">Pour plus d’informations sur le protocole SDP, localisez la norme IETF (Internet Engineering Task Force) RFC 2327 intitulée « SDP : session Description Protocol ».</span><span class="sxs-lookup"><span data-stu-id="1603e-116">For additional information on the SDP protocol, locate Internet Engineering Task Force (IETF) RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="1603e-117">Si l’interface **ITSDP** existe pour un objet blob de conférence donné, vous pouvez obtenir un pointeur vers celle-ci en exécutant **QueryInterface** sur [**ITConferenceBlob**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="1603e-117">If the **ITSDP** interface exists for a given conference blob, you can obtain a pointer to it by doing a **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

<span data-ttu-id="1603e-118">Pour les objets BLOB de conférence SDP, les interfaces [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md)et [**ITMedia**](itmedia.md) permettent un contrôle détaillé du temps de conférence SDP et des caractéristiques du support.</span><span class="sxs-lookup"><span data-stu-id="1603e-118">For SDP conference blobs, the [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md), and [**ITMedia**](itmedia.md) interfaces allow detailed control of SDP conference time and media characteristics.</span></span>

 

 



