---
description: Utilisation du protocole COPP (Certified Output Protection Protocol)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Utilisation du protocole COPP (Certified Output Protection Protocol)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533965"
---
# <a name="using-certified-output-protection-protocol-copp"></a><span data-ttu-id="fa408-103">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="fa408-103">Using Certified Output Protection Protocol (COPP)</span></span>

<span data-ttu-id="fa408-104">Le protocole COPP (Certified Output Protection Protocol) permet à une application de protéger un flux vidéo lorsqu’il passe de la carte graphique au périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fa408-104">Certified Output Protection Protocol (COPP) enables an application to protect a video stream as it travels from the graphics adapter to the display device.</span></span> <span data-ttu-id="fa408-105">Une application peut utiliser COPP pour découvrir le type de connecteur physique attaché au périphérique d’affichage, ainsi que les types de protection de sortie disponibles.</span><span class="sxs-lookup"><span data-stu-id="fa408-105">An application can use COPP to discover what kind of physical connector is attached to the display device, and what types of output protection are available.</span></span> <span data-ttu-id="fa408-106">Les mécanismes de protection sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fa408-106">Protection mechanisms include the following:</span></span>

-   <span data-ttu-id="fa408-107">High-Bandwidth protection du contenu numérique (HDCP)</span><span class="sxs-lookup"><span data-stu-id="fa408-107">High-Bandwidth Digital Content Protection (HDCP)</span></span>
-   <span data-ttu-id="fa408-108">Système de gestion de la génération de copie — analogique (CGMS-A)</span><span class="sxs-lookup"><span data-stu-id="fa408-108">Copy Generation Management System — Analog (CGMS-A)</span></span>
-   <span data-ttu-id="fa408-109">Protection contre la copie analogique (ACP)</span><span class="sxs-lookup"><span data-stu-id="fa408-109">Analog Copy Protection (ACP)</span></span>

<span data-ttu-id="fa408-110">Si la carte graphique prend en charge l’un de ces mécanismes, l’application peut utiliser COPP pour définir le niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="fa408-110">If the graphics adapter supports one of these mechanisms, the application can use COPP to set the protection level.</span></span>

<span data-ttu-id="fa408-111">COPP définit un protocole qui est utilisé pour établir un canal de communication sécurisé avec le pilote Graphics.</span><span class="sxs-lookup"><span data-stu-id="fa408-111">COPP defines a protocol that is used to establish a secure communications channel with the graphics driver.</span></span> <span data-ttu-id="fa408-112">Il utilise des codes d’authentification de message (Mac) pour vérifier l’intégrité des commandes COPP transmises entre l’application et le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fa408-112">It uses Message Authentication Codes (MACs) to verify the integrity of the COPP commands that are passed between the application and the display driver.</span></span> <span data-ttu-id="fa408-113">L’application utilise COPP en appelant des méthodes sur l’interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) du filtre de convertisseur de mixage vidéo DIRECTSHOW (VMR-7 ou VMR-9).</span><span class="sxs-lookup"><span data-stu-id="fa408-113">The application uses COPP by calling methods on the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface of the DirectShow Video Mixing Renderer filter (VMR-7 or VMR-9).</span></span>

<span data-ttu-id="fa408-114">COPP ne définit rien sur les stratégies de droits numériques qui peuvent s’appliquer au contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="fa408-114">COPP does not define anything about the digital rights policies that might apply to digital media content.</span></span> <span data-ttu-id="fa408-115">En outre, COPP n’implémente aucun système de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="fa408-115">Also, COPP itself does not implement any output protection systems.</span></span> <span data-ttu-id="fa408-116">Le protocole COPP permet simplement de définir et d’interroger des niveaux de protection sur la carte graphique, à l’aide des systèmes de protection fournis par l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="fa408-116">The COPP protocol simply provides a way to set and query protection levels on the graphics adapter, using the protection systems provided by the adapter.</span></span>

<span data-ttu-id="fa408-117">Cette section suppose que vous êtes familiarisé avec les technologies suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa408-117">This section assumes that you are familiar with the following technologies:</span></span>

-   <span data-ttu-id="fa408-118">DirectShow</span><span class="sxs-lookup"><span data-stu-id="fa408-118">DirectShow</span></span>
-   <span data-ttu-id="fa408-119">Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="fa408-119">Windows Media Format SDK</span></span>
-   <span data-ttu-id="fa408-120">XML</span><span class="sxs-lookup"><span data-stu-id="fa408-120">XML</span></span>
-   <span data-ttu-id="fa408-121">Chiffrement à clé publique et chiffrement symétrique</span><span class="sxs-lookup"><span data-stu-id="fa408-121">Public-key cryptography and symmetric cryptography</span></span>

<span data-ttu-id="fa408-122">Les exemples de code de cette section utilisent le CryptoAPI de Microsoft pour effectuer des opérations de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fa408-122">The code examples in this section use Microsoft's CryptoAPI to perform cryptographic operations.</span></span> <span data-ttu-id="fa408-123">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa408-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="fa408-124">Vue d’ensemble de COPP</span><span class="sxs-lookup"><span data-stu-id="fa408-124">Overview of COPP</span></span>](overview-of-copp.md)
-   [<span data-ttu-id="fa408-125">Obtention de la chaîne de certificats du pilote</span><span class="sxs-lookup"><span data-stu-id="fa408-125">Obtaining the Driver's Certificate Chain</span></span>](obtaining-the-drivers-certificate-chain.md)
-   [<span data-ttu-id="fa408-126">Validation de la chaîne de certificats</span><span class="sxs-lookup"><span data-stu-id="fa408-126">Validating the Certificate Chain</span></span>](validating-the-certificate-chain.md)
-   [<span data-ttu-id="fa408-127">Listes de révocation de certificats</span><span class="sxs-lookup"><span data-stu-id="fa408-127">Certificate Revocation Lists</span></span>](certificate-revocation-lists.md)
-   [<span data-ttu-id="fa408-128">Importation de la clé publique du pilote</span><span class="sxs-lookup"><span data-stu-id="fa408-128">Importing the Driver's Public Key</span></span>](importing-the-drivers-public-key.md)
-   [<span data-ttu-id="fa408-129">Lancement d’une session COPP</span><span class="sxs-lookup"><span data-stu-id="fa408-129">Initiating a COPP Session</span></span>](initiating-a-copp-session.md)
-   [<span data-ttu-id="fa408-130">Envoi de demandes d’État COPP</span><span class="sxs-lookup"><span data-stu-id="fa408-130">Sending COPP Status Requests</span></span>](sending-copp-status-requests.md)
-   [<span data-ttu-id="fa408-131">Envoi de commandes COPP</span><span class="sxs-lookup"><span data-stu-id="fa408-131">Sending COPP Commands</span></span>](sending-copp-commands.md)
-   [<span data-ttu-id="fa408-132">Tester si un pilote graphique prend en charge COPP</span><span class="sxs-lookup"><span data-stu-id="fa408-132">Testing Whether a Graphics Driver Supports COPP</span></span>](testing-whether-a-graphics-driver-supports-copp.md)
-   [<span data-ttu-id="fa408-133">Informations de référence sur les requêtes COPP</span><span class="sxs-lookup"><span data-stu-id="fa408-133">COPP Query Reference</span></span>](copp-query-reference.md)
-   [<span data-ttu-id="fa408-134">Informations de référence sur les commandes COPP</span><span class="sxs-lookup"><span data-stu-id="fa408-134">COPP Command Reference</span></span>](copp-command-reference.md)

## <a name="related-topics"></a><span data-ttu-id="fa408-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa408-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa408-136">Utilisation du convertisseur de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="fa408-136">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



