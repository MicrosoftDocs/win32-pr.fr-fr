---
description: Plusieurs fonctions ajoutent un contexte de certificat ou un lien vers un contexte vers un \[ Kit de développement logiciel (SDK) de plateforme de magasin \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Utilisation de certificats dans les magasins de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320041"
---
# <a name="working-with-certificates-in-certificate-stores"></a>Utilisation de certificats dans les magasins de certificats

Plusieurs fonctions ajoutent un contexte de certificat ou un lien vers un contexte dans un magasin.

Pour les certificats déjà sous forme de contexte de certificat :

-   [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [**CertAddCRLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [**CertAddCTLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

Pour les certificats qui sont au format codé, mais pas les contextes de certificat complet :

-   [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [**CertAddEncodedCRLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

Les fonctions suivantes suppriment un certificat, une liste de révocation de certificats ou une liste CTL d’un magasin en décrémentant son décompte de références d’une unité. Si le nombre de références est alors égal à zéro, la mémoire utilisée pour stocker le certificat, la liste de révocation de certificats ou la liste CTL est libérée.

-   [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [**CertDeleteCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



