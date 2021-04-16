---
description: Les contrôles Rendezvous TAPI 3 fournissent des mécanismes permettant de publier et de découvrir des conférences IP multimédias multiparties. Les éléments suivants décrivent un ensemble de composants COM (Component Object Model) et d’interfaces permettant d’implémenter des conférences.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: À propos de la Conférence de téléphonie IP Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563317"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="11f7a-104">À propos de la Conférence de téléphonie IP Rendezvous</span><span class="sxs-lookup"><span data-stu-id="11f7a-104">About Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="11f7a-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="11f7a-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="11f7a-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="11f7a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="11f7a-107">Les contrôles Rendezvous TAPI 3 fournissent des mécanismes permettant de publier et de découvrir des conférences IP multimédias multiparties.</span><span class="sxs-lookup"><span data-stu-id="11f7a-107">The TAPI 3 Rendezvous controls provide mechanisms to advertise and discover multiparty multimedia IP conferences.</span></span> <span data-ttu-id="11f7a-108">Les éléments suivants décrivent un ensemble de composants COM (Component Object Model) et d’interfaces permettant d’implémenter des conférences.</span><span class="sxs-lookup"><span data-stu-id="11f7a-108">The following describes a set of Component Object Model (COM) components and interfaces to implement conferencing.</span></span>

<span data-ttu-id="11f7a-109">COM est le modèle de codage de base pour TAPI 3, et vous savez qu’il est supposé dans ce document.</span><span class="sxs-lookup"><span data-stu-id="11f7a-109">COM is the basic coding model for TAPI 3, and familiarity with it is assumed throughout this document.</span></span> <span data-ttu-id="11f7a-110">Pour plus d’informations sur COM, consultez le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="11f7a-110">For information on COM, search the Platform Software Development Kit (SDK).</span></span>

## <a name="features"></a><span data-ttu-id="11f7a-111">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="11f7a-111">Features</span></span>

-   <span data-ttu-id="11f7a-112">Fournit l’abstraction d’un répertoire de conférence pour manipuler les annonces de conférences multimédias.</span><span class="sxs-lookup"><span data-stu-id="11f7a-112">Provides the abstraction of a conference directory for manipulating announcements of multimedia conferences</span></span>
-   <span data-ttu-id="11f7a-113">Assure la sécurité par le biais de l’authentification, du chiffrement et d’une couche de contrôle d’accès (ACL) par annonce</span><span class="sxs-lookup"><span data-stu-id="11f7a-113">Provides security through authentication, encryption, and a per-announcement access control layer (ACL)</span></span>
-   <span data-ttu-id="11f7a-114">Fournit un schéma commun pour une annonce de conférence, ce qui permet de rechercher des valeurs d’attribut</span><span class="sxs-lookup"><span data-stu-id="11f7a-114">Provides a common schema for a conference announcement, enabling searches by attribute values</span></span>
-   <span data-ttu-id="11f7a-115">Autorise les extensions via un attribut géré par le fournisseur (objet blob de conférence) dans le schéma</span><span class="sxs-lookup"><span data-stu-id="11f7a-115">Allows extensions through a provider-maintained attribute (conference blob) in the schema</span></span>
-   <span data-ttu-id="11f7a-116">Fournit un wrapper COM pour l’API d’allocation d’adresses multidiffusion (MADCAP)</span><span class="sxs-lookup"><span data-stu-id="11f7a-116">Provides a COM wrapper for the multicast address allocation (MADCAP) API</span></span>

## <a name="architecture"></a><span data-ttu-id="11f7a-117">Architecture</span><span class="sxs-lookup"><span data-stu-id="11f7a-117">Architecture</span></span>

<span data-ttu-id="11f7a-118">Les descriptions et le diagramme suivants illustrent les aspects clés de l’architecture système.</span><span class="sxs-lookup"><span data-stu-id="11f7a-118">The following descriptions and diagram illustrate key aspects of the system architecture.</span></span>

-   <span data-ttu-id="11f7a-119">Le client peut manipuler des conférences stockées sur un répertoire dynamique ILS ou un serveur NTDS à l’aide des contrôles Rendezvous.</span><span class="sxs-lookup"><span data-stu-id="11f7a-119">The client can manipulate conferences stored on an ILS dynamic directory or NTDS server using Rendezvous controls.</span></span> <span data-ttu-id="11f7a-120">Le protocole LDAP (Lightweight Directory Access Protocol) est utilisé pour communiquer avec un serveur ILS.</span><span class="sxs-lookup"><span data-stu-id="11f7a-120">The Lightweight Directory Access Protocol (LDAP) is used to communicate with an ILS server.</span></span>
-   <span data-ttu-id="11f7a-121">Les contrôles Rendezvous fournissent des interfaces COM doubles pour l’écriture de scripts et la programmation.</span><span class="sxs-lookup"><span data-stu-id="11f7a-121">The Rendezvous controls provide dual COM interfaces for scripting and programming.</span></span>
-   <span data-ttu-id="11f7a-122">Un serveur SAP (session Announcement Protocol) ayant un accès direct à Internet écoute les annonces de conférences sur Internet et remplit les serveurs dynamiques ILS avec les informations de conférence.</span><span class="sxs-lookup"><span data-stu-id="11f7a-122">A Session Announcement Protocol (SAP) server with direct access to the Internet listens to conference announcements on the Internet and populates ILS dynamic servers with the conference information.</span></span> <span data-ttu-id="11f7a-123">De même, il annonce également les conférences créées localement dont l’étendue comprend Internet.</span><span class="sxs-lookup"><span data-stu-id="11f7a-123">Similarly, it also announces the locally created conferences whose scope includes the Internet.</span></span> <span data-ttu-id="11f7a-124">(Le serveur SAP n’est pas planifié pour Microsoft Windows 2000.)</span><span class="sxs-lookup"><span data-stu-id="11f7a-124">(The SAP server is not planned for Microsoft Windows 2000.)</span></span>

![architecture du système Rendezvous](images/rend1.png)

 

 



