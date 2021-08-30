---
description: Les fonctions CertAddCertificateLinkToStore, CertAddCRLLinkToStore et CertAddCTLLinkToStore ajoutent des liens vers des contextes existants dans des magasins de certificats, plutôt que d’ajouter des copies de ces contextes.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Liens de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e73c67acd9aaba8efe21bba829b59b5cad9803beacf146a765636c0d65c0ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126993"
---
# <a name="certificate-links"></a>Liens de certificat

Les fonctions [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)et [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) ajoutent des liens vers des contextes existants dans des [*magasins de certificats*](../secgloss/c-gly.md) , plutôt que d’ajouter des copies de ces contextes. L’ajout de liens aux magasins rend le même [*certificat*](../secgloss/c-gly.md)physique, la même [*liste de révocation de certificats*](../secgloss/c-gly.md)ou la liste [*CTL*](../secgloss/c-gly.md) disponible via plusieurs magasins différents. Les modifications apportées aux propriétés étendues d’un [*contexte*](../secgloss/c-gly.md) à partir du magasin du contexte d’origine, ou à partir d’un magasin où un lien vers ce contexte est stocké, sont disponibles dans le magasin qui contient le contexte d’origine et dans tous les autres magasins qui possèdent des liens vers ce contexte.

Pour obtenir un exemple qui utilise [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), consultez [exemple de programme C : opérations du magasin de certificats](example-c-program-certificate-store-operations.md).

![Liens de certificat](images/mancert1.png)

Supposons que les certificats A. 1, A. 2, A. 3 et A. 4 se trouvent à l’origine dans le magasin A, et que les certificats B. 1, B. 2, B. 3 et B. 4 sont à l’origine dans le magasin B.

-   Le diagramme montre un lien ajouté dans le magasin B vers le certificat A. 2 et un lien ajouté dans le magasin A au certificat B. 2.
-   L’original du certificat A. 2 se trouve toujours dans le magasin A. L’original de B. 2 est toujours dans le magasin B.
-   Toutes les modifications apportées aux propriétés étendues du certificat A. 2 ou du certificat B. 2 de l’un ou l’autre magasin A ou magasin B sont disponibles pour les deux magasins.
-   Si une copie du certificat A. 3 a été effectuée et stockée dans le magasin B, toute modification apportée aux propriétés étendues du certificat A. 3 d’origine à partir du magasin A n’est pas visible dans la nouvelle copie du magasin B. Si des modifications ont été apportées aux propriétés étendues de la copie du certificat A. 3 dans le magasin B, ces modifications n’affectent pas le contenu du certificat A. 3 d’origine et ne sont pas visibles à partir du magasin A.

 

 
