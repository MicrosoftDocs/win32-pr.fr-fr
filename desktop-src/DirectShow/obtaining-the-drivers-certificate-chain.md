---
description: Obtention de la chaîne de certificats des pilotes
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Obtention de la chaîne de certificats des pilotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3f46e395550ca4bcb02396fe09126c1232f2c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845746"
---
# <a name="obtaining-the-drivers-certificate-chain"></a><span data-ttu-id="1ce28-103">Obtention de la chaîne de certificats des pilotes</span><span class="sxs-lookup"><span data-stu-id="1ce28-103">Obtaining the Drivers Certificate Chain</span></span>

<span data-ttu-id="1ce28-104">Pour utiliser le protocole COPP (Certified Output Protection Protocol), l’application doit d’abord créer un graphique DirectShow qui comprend le filtre de rendu de mixage vidéo (VMR-7 ou VMR-9).</span><span class="sxs-lookup"><span data-stu-id="1ce28-104">To use Certified Output Protection Protocol (COPP), the application first must build a DirectShow graph that includes the Video Mixing Render filter (VMR-7 or VMR-9).</span></span> <span data-ttu-id="1ce28-105">Le filtre de convertisseur vidéo plus ancien ne prend pas en charge COPP.</span><span class="sxs-lookup"><span data-stu-id="1ce28-105">The older Video Renderer filter does not support COPP.</span></span> <span data-ttu-id="1ce28-106">Avant d’appeler des méthodes COPP, l’application doit générer un graphique de lecture vidéo et connecter le décodeur à la broche d’entrée du filtre VMR.</span><span class="sxs-lookup"><span data-stu-id="1ce28-106">Before calling any COPP methods, the application must build a video playback graph and connect the decoder to the VMR filter's input pin.</span></span> <span data-ttu-id="1ce28-107">Il n’est pas nécessaire de lire le fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="1ce28-107">It is not necessary to play the video file.</span></span>

<span data-ttu-id="1ce28-108">Une fois le graphique créé, interrogez VMR pour obtenir l’interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) , puis appelez [**IAMCertifiedOutputProtection :: KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="1ce28-108">After building the graph, query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface, and then call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="1ce28-109">Cette méthode retourne un nombre aléatoire 128 bits typé en tant que GUID, ainsi qu’un pointeur vers un tableau d’octets qui contient la chaîne de certificats XML du pilote au format UTF-8.</span><span class="sxs-lookup"><span data-stu-id="1ce28-109">This method returns a 128-bit random number typed as a GUID, along with a pointer to a byte array that contains the driver's XML certificate chain in UTF-8 format.</span></span> <span data-ttu-id="1ce28-110">Le code suivant montre comment récupérer la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="1ce28-110">The following code shows how to get the certificate chain.</span></span>


```C++
GUID guidRandom;
BYTE *pbCertificateChain = NULL;
DWORD cbCertificateChainLen;   // Size of the certificate chain, in bytes.
hr = pCOPP->KeyExchange(&guidRandom, &pbCertificateChain,
         &cbCertificateChainLen);
if (SUCCEEDED(hr))
{
    // TODO: Validate the certificate chain and get the driver's
    // public key. 

    // When you are done, free the buffer that contains the 
    // certificate chain.
    CoTaskMemFree(pbCertificateChain);
}
```



## <a name="related-topics"></a><span data-ttu-id="1ce28-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ce28-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ce28-112">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="1ce28-112">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



