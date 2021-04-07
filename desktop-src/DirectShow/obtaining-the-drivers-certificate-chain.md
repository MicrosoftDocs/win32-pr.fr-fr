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
# <a name="obtaining-the-drivers-certificate-chain"></a>Obtention de la chaîne de certificats des pilotes

Pour utiliser le protocole COPP (Certified Output Protection Protocol), l’application doit d’abord créer un graphique DirectShow qui comprend le filtre de rendu de mixage vidéo (VMR-7 ou VMR-9). Le filtre de convertisseur vidéo plus ancien ne prend pas en charge COPP. Avant d’appeler des méthodes COPP, l’application doit générer un graphique de lecture vidéo et connecter le décodeur à la broche d’entrée du filtre VMR. Il n’est pas nécessaire de lire le fichier vidéo.

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

 

 



