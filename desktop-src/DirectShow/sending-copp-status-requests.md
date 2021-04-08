---
description: Envoi de demandes d’État COPP
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Envoi de demandes d’État COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745413"
---
# <a name="sending-copp-status-requests"></a><span data-ttu-id="8b84f-103">Envoi de demandes d’État COPP</span><span class="sxs-lookup"><span data-stu-id="8b84f-103">Sending COPP Status Requests</span></span>

<span data-ttu-id="8b84f-104">Pour envoyer une demande d’État COPP (Certified Output Protection Protocol), remplissez une structure [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) avec les données de la demande.</span><span class="sxs-lookup"><span data-stu-id="8b84f-104">To send a Certified Output Protection Protocol (COPP) status request, fill in an [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure with the request data.</span></span> <span data-ttu-id="8b84f-105">Les membres de la structure sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="8b84f-105">The structure members are:</span></span>

-   <span data-ttu-id="8b84f-106">**rApp**.</span><span class="sxs-lookup"><span data-stu-id="8b84f-106">**rApp**.</span></span> <span data-ttu-id="8b84f-107">Nombre aléatoire 128 bits, typé en tant que GUID.</span><span class="sxs-lookup"><span data-stu-id="8b84f-107">A 128-bit random number, typed as a GUID.</span></span> <span data-ttu-id="8b84f-108">Le même numéro est retourné dans la réponse du pilote.</span><span class="sxs-lookup"><span data-stu-id="8b84f-108">The same number is returned in the driver's response.</span></span> <span data-ttu-id="8b84f-109">Vous devez allouer le nombre aléatoire sur le tas, puis le copier dans la structure.</span><span class="sxs-lookup"><span data-stu-id="8b84f-109">You should allocate the random number on the heap and then copy it into structure.</span></span> <span data-ttu-id="8b84f-110">Cela permet de protéger les attaques lorsque l’attaquant modifie le contenu de la structure [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .</span><span class="sxs-lookup"><span data-stu-id="8b84f-110">This guards against attacks where the attacker modifies the contents of the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure.</span></span>
-   <span data-ttu-id="8b84f-111">**guidStatusRequestID**.</span><span class="sxs-lookup"><span data-stu-id="8b84f-111">**guidStatusRequestID**.</span></span> <span data-ttu-id="8b84f-112">GUID qui identifie la demande.</span><span class="sxs-lookup"><span data-stu-id="8b84f-112">A GUID that identifies the request.</span></span> <span data-ttu-id="8b84f-113">Consultez [référence de requête Copp](copp-query-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8b84f-113">See [COPP Query Reference](copp-query-reference.md).</span></span>
-   <span data-ttu-id="8b84f-114">**dwSequence**.</span><span class="sxs-lookup"><span data-stu-id="8b84f-114">**dwSequence**.</span></span> <span data-ttu-id="8b84f-115">Numéro de séquence d’État.</span><span class="sxs-lookup"><span data-stu-id="8b84f-115">The status sequence number.</span></span> <span data-ttu-id="8b84f-116">Incrémentez cette valeur après chaque demande d’État.</span><span class="sxs-lookup"><span data-stu-id="8b84f-116">Increment this value after each status request.</span></span> <span data-ttu-id="8b84f-117">(Dans la section [lancement d’une session Copp](initiating-a-copp-session.md), cette valeur est affichée en tant que *uStatusSeq* dans les exemples de code.)</span><span class="sxs-lookup"><span data-stu-id="8b84f-117">(In the section [Initiating a COPP Session](initiating-a-copp-session.md), this value is shown as *uStatusSeq* in the code examples.)</span></span>
-   <span data-ttu-id="8b84f-118">**cbSizeData**.</span><span class="sxs-lookup"><span data-stu-id="8b84f-118">**cbSizeData**.</span></span> <span data-ttu-id="8b84f-119">Taille, en octets, de toutes les données supplémentaires nécessaires pour la demande.</span><span class="sxs-lookup"><span data-stu-id="8b84f-119">The size, in bytes, of any additional data needed for the request.</span></span>
-   <span data-ttu-id="8b84f-120">**StatusData**.</span><span class="sxs-lookup"><span data-stu-id="8b84f-120">**StatusData**.</span></span> <span data-ttu-id="8b84f-121">Données pour la demande d’État.</span><span class="sxs-lookup"><span data-stu-id="8b84f-121">Data for the status request.</span></span>

<span data-ttu-id="8b84f-122">Transmettez la structure [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) à la méthode [**IAMCertifiedOutputProtection ::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) .</span><span class="sxs-lookup"><span data-stu-id="8b84f-122">Pass the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure to the [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) method.</span></span> <span data-ttu-id="8b84f-123">Par exemple, le code suivant envoie une demande d’État qui interroge les mécanismes de protection disponibles :</span><span class="sxs-lookup"><span data-stu-id="8b84f-123">For example, the following code sends a status request that queries which protection mechanisms are available:</span></span>


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



<span data-ttu-id="8b84f-124">La réponse est écrite dans le membre **COPPStatus** de la structure [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) .</span><span class="sxs-lookup"><span data-stu-id="8b84f-124">The response is written into the **COPPStatus** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure.</span></span> <span data-ttu-id="8b84f-125">La taille des données valides dans la réponse est donnée dans le membre **cbSizeData** .</span><span class="sxs-lookup"><span data-stu-id="8b84f-125">The size of the valid data in the response is given in the **cbSizeData** member.</span></span> <span data-ttu-id="8b84f-126">Pour garantir l’intégrité du message, le pilote calcule un code d’authentification de message (MAC) à l’aide de l’algorithme OMAC 1 et retourne cette valeur dans le membre **macKDI** de la structure.</span><span class="sxs-lookup"><span data-stu-id="8b84f-126">To ensure the integrity of the message, the driver computes a message authentication code (MAC) using the OMAC 1 algorithm, and returns this value in the structure's **macKDI** member.</span></span> <span data-ttu-id="8b84f-127">L’application doit vérifier cette valeur comme suit :</span><span class="sxs-lookup"><span data-stu-id="8b84f-127">The application should verify this value as follows:</span></span>

1.  <span data-ttu-id="8b84f-128">Calculez la balise OMAC pour le bloc de données qui apparaît après le membre **macKDI** de la structure [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (en d’autres termes, **cbSizeData** plus **COPPStatus**).</span><span class="sxs-lookup"><span data-stu-id="8b84f-128">Calculate the OMAC tag for the block of data that appears after the **macKDI** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure (in other words, **cbSizeData** plus **COPPStatus**).</span></span>
2.  <span data-ttu-id="8b84f-129">Comparez cette balise à la valeur dans **macKDI**, à l’aide d’un **memcmp** simple.</span><span class="sxs-lookup"><span data-stu-id="8b84f-129">Compare this tag with the value in **macKDI**, using a straight **memcmp**.</span></span>

<span data-ttu-id="8b84f-130">L’algorithme OMAC 1 est décrit en détail dans [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) .</span><span class="sxs-lookup"><span data-stu-id="8b84f-130">The OMAC 1 algorithm is described in detail at [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html).</span></span> <span data-ttu-id="8b84f-131">COPP utilise les paramètres OMAC-1 suivants :</span><span class="sxs-lookup"><span data-stu-id="8b84f-131">COPP uses the following OMAC-1 parameters:</span></span>

-   <span data-ttu-id="8b84f-132">E = AES</span><span class="sxs-lookup"><span data-stu-id="8b84f-132">E = AES</span></span>
-   <span data-ttu-id="8b84f-133">t = 128 bits</span><span class="sxs-lookup"><span data-stu-id="8b84f-133">t = 128 bits</span></span>

<span data-ttu-id="8b84f-134">Les données retournées par la demande Status commencent toujours par deux éléments :</span><span class="sxs-lookup"><span data-stu-id="8b84f-134">The data returned from the status request always starts with two items:</span></span>

-   <span data-ttu-id="8b84f-135">La même valeur de **rApp** qui a été passée par l’application.</span><span class="sxs-lookup"><span data-stu-id="8b84f-135">The same value of **rApp** that was passed by the application.</span></span> <span data-ttu-id="8b84f-136">Vous devez vérifier que cette valeur correspond à la valeur d’origine stockée sur le tas.</span><span class="sxs-lookup"><span data-stu-id="8b84f-136">You should verify that this value matches the original value stored on the heap.</span></span>
-   <span data-ttu-id="8b84f-137">Valeur [**de \_ StatusFlags Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) qui indique si l’état de protection de sortie a changé.</span><span class="sxs-lookup"><span data-stu-id="8b84f-137">A [**COPP\_StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) value that indicates whether the output protection status has changed.</span></span>

<span data-ttu-id="8b84f-138">Étant donné que la connexion peut être perdue ou reconfigurée, l’application doit régulièrement interroger le pilote pour connaître l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="8b84f-138">Because the connection can be lost or reconfigured, the application should periodically poll the driver for the current status.</span></span> <span data-ttu-id="8b84f-139">Si l' \_ indicateur Copp RenegotiationRequired est défini, l’application doit tenter de réinitialiser le niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="8b84f-139">If the COPP\_RenegotiationRequired flag is set, the application should attempt to reset the protection level.</span></span> <span data-ttu-id="8b84f-140">Si l' \_ indicateur Copp LinkLost est défini, l’application doit arrêter la diffusion du contenu.</span><span class="sxs-lookup"><span data-stu-id="8b84f-140">If the COPP\_LinkLost flag is set, the application should stop playing the content.</span></span> <span data-ttu-id="8b84f-141">Par exemple, l' \_ indicateur Copp LinkLost peut être retourné parce que l’utilisateur a déconnecté le connecteur de sortie.</span><span class="sxs-lookup"><span data-stu-id="8b84f-141">For example, the COPP\_LinkLost flag can be returned because the user disconnected the output connector.</span></span> <span data-ttu-id="8b84f-142">L’application doit libérer l’instance actuelle de VMR, créer une nouvelle instance de VMR et établir une nouvelle session COPP (y compris l’échange de clés et la validation de certificat).</span><span class="sxs-lookup"><span data-stu-id="8b84f-142">The application should release the current instance of the VMR, create a new instance of the VMR, and establish a new COPP session (including key exchange and certificate validation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b84f-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b84f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b84f-144">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="8b84f-144">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



