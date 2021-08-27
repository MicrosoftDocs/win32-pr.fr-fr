---
description: Les données contenues dans un certificat, une liste de révocation de certificats (CRL) ou un contexte de liste de certificats de confiance (CTL), y compris les extensions, sont en lecture seule et ne peuvent pas être modifiées.
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: Propriétés étendues du certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37eaf192d4c236a4f12898ece2bded86d467404c5eceedd98f1deb976b8857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127089"
---
# <a name="certificate-extended-properties"></a>Propriétés étendues du certificat

Les données contenues dans un [*certificat*](../secgloss/c-gly.md), une [*liste de révocation de certificats*](../secgloss/c-gly.md) (CRL) ou un [*contexte*](../secgloss/c-gly.md)de liste de [*certificats de confiance*](../secgloss/c-gly.md) (CTL), y compris les extensions, sont en lecture seule et ne peuvent pas être modifiées. Toutefois, sur les plateformes Microsoft, les certificats CryptoAPI ont également des propriétés étendues dynamiques qui peuvent être ajoutées et modifiées.

> [!Note]  
> Les propriétés étendues sont associées à un certificat et ne font pas partie d’un certificat émis par une [*autorité de certification*](../secgloss/c-gly.md) (ca). Les propriétés étendues ne sont pas disponibles sur un certificat lorsqu’il est utilisé sur une plateforme non-Microsoft.

 

Ces propriétés incluent des données qui :

-   Se rapporte à la clé privée à utiliser avec le certificat.
-   Indique le type de hachage à effectuer sur le certificat.
-   Fournit des informations définies par l’utilisateur associées au certificat.

Sur les plateformes Microsoft, les valeurs de ces propriétés sont jointes et déplacées avec le certificat. Les propriétés prédéfinies actuellement identifiées par des ID de propriété incluent les propriétés suivantes :

-   Ces propriétés lient un certificat à un CSP particulier et, dans ce CSP, à une clé privée particulière :
    -   \_ \_ \_ ID prop du handle \_ de clé de certificat \_
    -   ID de la clé de certificat \_ \_ Prov \_ info \_ prop \_
    -   \_ID de \_ prop du contexte de clé du certificat \_ \_
-   Ces propriétés indiquent l’algorithme de hachage à utiliser lors de l’exécution d’une opération de hachage :
    -   \_ID de \_ la \_ prop hash SHA1 \_ du certificat
    -   \_ID de \_ la \_ prop Hash MD5 \_ du certificat

Pour obtenir la liste complète des propriétés de certificat étendues actuellement définies et des descriptions de la signification et de l’utilisation de chaque propriété, consultez [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[**CertGetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[**CertSetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
