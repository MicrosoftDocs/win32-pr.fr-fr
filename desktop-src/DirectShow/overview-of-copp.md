---
description: Vue d’ensemble de COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Vue d’ensemble de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514311"
---
# <a name="overview-of-copp"></a><span data-ttu-id="2c90f-103">Vue d’ensemble de COPP</span><span class="sxs-lookup"><span data-stu-id="2c90f-103">Overview of COPP</span></span>

<span data-ttu-id="2c90f-104">Voici les étapes de base qu’une application doit effectuer pour utiliser le protocole COPP (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="2c90f-104">Here are the basic steps that an application must perform to use Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="2c90f-105">**Récupérer la chaîne de certificats du pilote**</span><span class="sxs-lookup"><span data-stu-id="2c90f-105">**Get the driver's certificate chain**</span></span>

1.  <span data-ttu-id="2c90f-106">Générez un graphique de lecture DirectShow qui affiche la vidéo à l’aide du convertisseur de mixage vidéo (VMR-7 ou VMR-9) ou du filtre de [**convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="2c90f-106">Build a DirectShow playback graph that renders video using the Video Mixing Renderer (VMR-7 or VMR-9) or the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) filter (EVR).</span></span>
2.  <span data-ttu-id="2c90f-107">Interrogez VMR pour obtenir l’interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) .</span><span class="sxs-lookup"><span data-stu-id="2c90f-107">Query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface.</span></span>
3.  <span data-ttu-id="2c90f-108">Appelez [**IAMCertifiedOutputProtection :: KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="2c90f-108">Call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="2c90f-109">Cette méthode retourne un nombre aléatoire 128 bits du pilote, ainsi qu’une chaîne de certificats qui contient la clé publique RSA 2048 bits du pilote.</span><span class="sxs-lookup"><span data-stu-id="2c90f-109">This method returns a 128-bit random number from the driver, along with a certificate chain that contains the driver's 2048-bit RSA public key.</span></span>

<span data-ttu-id="2c90f-110">**Valider la chaîne de certificats**</span><span class="sxs-lookup"><span data-stu-id="2c90f-110">**Validate the certificate chain**</span></span>

1.  <span data-ttu-id="2c90f-111">Validez la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="2c90f-111">Validate the certificate chain.</span></span> <span data-ttu-id="2c90f-112">Si la chaîne de certificats n’est pas valide, arrêtez.</span><span class="sxs-lookup"><span data-stu-id="2c90f-112">If the certificate chain is not valid, stop.</span></span>
2.  <span data-ttu-id="2c90f-113">Vérifiez la liste de révocation de certificats (CRL).</span><span class="sxs-lookup"><span data-stu-id="2c90f-113">Check the certificate revocation list (CRL).</span></span> <span data-ttu-id="2c90f-114">Si l’un des certificats de la chaîne de certificats apparaît dans la liste de révocation, arrêtez.</span><span class="sxs-lookup"><span data-stu-id="2c90f-114">If any of the certificates in the certificate chain appears in the revocation list, stop.</span></span>
3.  <span data-ttu-id="2c90f-115">Récupération de la clé publique RSA à partir de la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="2c90f-115">Get the RSA public key from the certificate chain.</span></span>

<span data-ttu-id="2c90f-116">**Initialiser la session COPP**</span><span class="sxs-lookup"><span data-stu-id="2c90f-116">**Initialize the COPP Session**</span></span>

1.  <span data-ttu-id="2c90f-117">Générez une clé de session AES 128 bits.</span><span class="sxs-lookup"><span data-stu-id="2c90f-117">Generate a 128-bit AES session key.</span></span> <span data-ttu-id="2c90f-118">Cette clé est utilisée pour signer des données et vérifier que les données signées n’ont pas été falsifiées.</span><span class="sxs-lookup"><span data-stu-id="2c90f-118">This key is used to sign data and to verify that signed data has not been tampered with.</span></span>
2.  <span data-ttu-id="2c90f-119">Générer deux nombres aléatoires 32 bits sécurisés par chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2c90f-119">Generate two cryptographically secure 32-bit random numbers.</span></span> <span data-ttu-id="2c90f-120">Le premier est un numéro de séquence d’État, tandis que le second est un numéro de séquence de commande.</span><span class="sxs-lookup"><span data-stu-id="2c90f-120">The first is a status sequence number, and the second is a command sequence number.</span></span> <span data-ttu-id="2c90f-121">Chaque fois que l’application envoie une commande ou une demande d’État, elle incrémente le numéro de séquence correspondant et y ajoute ce numéro dans la commande COPP ou les données de la requête.</span><span class="sxs-lookup"><span data-stu-id="2c90f-121">Each time the application sends a command or status request, it increments the corresponding sequence number, and includes this number in the COPP command or request data.</span></span>
3.  <span data-ttu-id="2c90f-122">Concaténez le nombre aléatoire 128 bits à partir du pilote Graphics, la clé de session AES, le numéro de séquence d’État et le numéro de séquence de commande.</span><span class="sxs-lookup"><span data-stu-id="2c90f-122">Concatenate the 128-bit random number from the graphics driver, the AES session key, the status sequence number, and the command sequence number.</span></span> <span data-ttu-id="2c90f-123">Chiffrez ce tableau d’octets à l’aide de la clé publique du pilote et transmettez le résultat à [**IAMCertifiedOutputProtection :: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span><span class="sxs-lookup"><span data-stu-id="2c90f-123">Encrypt this byte array using the driver's public key and pass the result to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span></span>

<span data-ttu-id="2c90f-124">**Envoyer des commandes et des requêtes d’État COPP**</span><span class="sxs-lookup"><span data-stu-id="2c90f-124">**Send COPP Commands and Status Requests**</span></span>

1.  <span data-ttu-id="2c90f-125">Interrogez les types de protection disponibles et d’autres informations en appelant [**IAMCertifiedOutputProtection ::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span><span class="sxs-lookup"><span data-stu-id="2c90f-125">Query for the available protection types and other information by calling [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span></span>
2.  <span data-ttu-id="2c90f-126">Définissez les niveaux de protection souhaités en appelant [**IAMCertifiedOutputProtection ::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span><span class="sxs-lookup"><span data-stu-id="2c90f-126">Set the desired protection levels by calling [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span></span>
3.  <span data-ttu-id="2c90f-127">Interrogez régulièrement le niveau de protection local actuel.</span><span class="sxs-lookup"><span data-stu-id="2c90f-127">Periodically query for the current local protection level.</span></span> <span data-ttu-id="2c90f-128">Arrêter la lecture si le niveau de protection local change de façon inattendue ou si un problème est détecté.</span><span class="sxs-lookup"><span data-stu-id="2c90f-128">Stop playback if the local protection level changes unexpectedly or if a problem is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c90f-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c90f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c90f-130">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="2c90f-130">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



