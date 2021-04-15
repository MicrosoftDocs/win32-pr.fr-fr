---
description: Le préfixe ASN. 1 (Abstract Syntax Notation One) définit les ensembles de règles suivants qui régissent la façon dont les structures de données envoyées entre les ordinateurs sont encodées et décodées.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527003"
---
# <a name="distinguished-encoding-rules"></a>Distinguished Encoding Rules

Le préfixe ASN. 1 (Abstract Syntax Notation One) définit les ensembles de règles suivants qui régissent la façon dont les structures de données envoyées entre les ordinateurs sont encodées et décodées.

-   Règles de codage de base (BER)
-   Règles d’encodage canoniques (CER)
-   Distinguished Encoding Rules (DER)
-   Règles d’encodage compressées (PER)

L’ensemble de règles d’origine a été défini par la spécification BER. CER et DER ont été développés plus tard en tant que sous-ensembles spécialisés de BER. PAR a été développé en réponse à formulées sur la quantité de bande passante requise pour transmettre des données à l’aide de BER ou de ses variantes. PER fournit des économies substantielles.

DER a été créé pour répondre aux exigences de la spécification X. 509 pour un transfert de données sécurisé. L’API d’inscription de certificats utilise DER exclusivement. Pour plus d'informations, consultez les rubriques ci-dessous.

-   [Syntaxe de transfert DER](about-der-transfer-syntax.md)
-   [Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Encodage de demande de certificat](about-certificate-request-encoding.md)
</dt> <dt>

[Présentation de la syntaxe et de l’encodage ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



