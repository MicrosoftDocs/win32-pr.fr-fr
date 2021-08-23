---
description: Obtention de la chaîne de certificats des pilotes
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Obtention de la chaîne de certificats des pilotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2641c27c3d24ab45a87b16e8c805228c316d9f89428cd29abbaff347b5aae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684559"
---
# <a name="obtaining-the-drivers-certificate-chain"></a>Obtention de la chaîne de certificats des pilotes

pour utiliser le protocole COPP (certified Output Protection Protocol), l’application doit d’abord créer un DirectShow graphique qui comprend le filtre de rendu de mixage vidéo (vmr-7 ou vmr-9). Le filtre de convertisseur vidéo plus ancien ne prend pas en charge COPP. Avant d’appeler des méthodes COPP, l’application doit générer un graphique de lecture vidéo et connecter le décodeur à la broche d’entrée du filtre VMR. Il n’est pas nécessaire de lire le fichier vidéo.

Une fois le graphique créé, interrogez VMR pour obtenir l’interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) , puis appelez [**IAMCertifiedOutputProtection :: KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Cette méthode retourne un nombre aléatoire 128 bits typé en tant que GUID, ainsi qu’un pointeur vers un tableau d’octets qui contient la chaîne de certificats XML du pilote au format UTF-8. Le code suivant montre comment récupérer la chaîne de certificats.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



