---
description: Décrit la procédure d’encodage d’un message signé.
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: Encodage de données signées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4a542fe0890a6ee9d51ebc1a5ee6b98bab4242
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416438"
---
# <a name="encoding-signed-data"></a>Encodage de données signées

Les [*données signées*](../secgloss/s-gly.md) se composent du contenu de tout type et de tous les [*hachages*](../secgloss/h-gly.md) de messages chiffrés du contenu par zéro ou plusieurs signataires. Le hachage résultant peut confirmer que le message d’origine n’a pas été modifié depuis la signature et que certaines personnes ou entités ont signé les données.

L’illustration suivante représente la procédure d’encodage d’un message signé. La liste qui suit l’illustration décrit les étapes.

Un message peut avoir plusieurs signataires, des algorithmes de hachage et des certificats. Bien que l’illustration affiche uniquement les certificats, les [*listes de révocation*](../secgloss/c-gly.md)de certificats et les listes de certificats de [*confiance*](../secgloss/c-gly.md) peuvent utiliser le même processus. Ils rentrent dans l’illustration partout où les certificats sont affichés.

![encodage d’un message signé](images/signmsg2.png)

Le processus général d’encodage des [*données signées*](../secgloss/s-gly.md) est le suivant.

**Pour encoder des données signées**

1.  Les données sont créées (si nécessaire) et un pointeur vers cette dernière est récupéré.
2.  Un [*magasin de certificats*](../secgloss/c-gly.md) s’ouvre et contient le certificat du signataire.
3.  La clé privée du certificat est récupérée. Il existe deux propriétés qui doivent être définies sur le certificat avant de l’utiliser. L’un est utilisé pour lier un certificat à un CSP particulier et, dans ce CSP, à un [*conteneur de clé*](../secgloss/k-gly.md)privée particulier. L’autre est utilisée pour indiquer l’algorithme de hachage à utiliser lors de l’appel d’une opération de [*hachage*](../secgloss/h-gly.md) . Ces derniers ne doivent être définis qu’une seule fois.
4.  La propriété d’un certificat détermine l’algorithme de hachage.
5.  Un hachage des données est créé en envoyant les données via la fonction de hachage.
6.  La signature est créée en chiffrant le hachage à l’aide de la clé privée, obtenue par le biais d’une propriété sur le certificat.
7.  Les données suivantes sont incluses dans le message terminé, signé :
    -   Données d’origine à signer
    -   Algorithmes de hachage
    -   Les signatures
    -   Structures d’informations sur le signataire, qui incluent l’identificateur du signataire (émetteur et numéro de série du certificat)
    -   Certificats du signataire (facultatif)

Cette procédure illustre un cas simple. Les cas plus complexes impliquent des attributs authentifiés inclus dans le message. Lorsque le type de contenu est, à l’exception d’une chaîne d' **octets** , ou qu’il existe au moins un attribut authentifié avec un type de données, deux attributs authentifiés standard sont requis : le type de contenu (données) et le hachage du contenu. Dans ces circonstances, l' [*CryptoAPI*](../secgloss/c-gly.md) fournit automatiquement ces deux attributs requis. Les fonctions de message de bas niveau hachent les attributs authentifiés, chiffrent le hachage avec la clé privée et fournissent ce code comme signature.

Utilisez les fonctions de message de bas niveau pour accomplir les tâches que vous venez de répertorier, à l’aide de la procédure suivante.

**Pour encoder un message signé**

1.  Créez ou récupérez le contenu.
2.  Obtenir un fournisseur de services de chiffrement.
3.  Obtient les certificats de signataire.
4.  Initialisez la structure d' [**\_ informations de \_ codage \_ du signataire CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) .
5.  Initialisez la structure d' [**\_ \_ \_ informations de codage signé CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .
6.  Appelez [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) pour connaître la taille de l’objet blob de message encodé. Allouez de la mémoire pour celui-ci.
7.  Appelez [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), en passant CMSG \_ signed *pour dwMsgType* et un pointeur vers les [**\_ \_ \_ informations de codage signées CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) pour *pvMsgEncodeInfo* afin d’obtenir un handle pour le message ouvert.
8.  Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), en passant le handle récupéré à l’étape 7 et un pointeur vers les données qui doivent être signées et encodées. Cette fonction peut être appelée autant de fois que nécessaire pour terminer le processus d’encodage.
9.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant le handle récupéré à l’étape 7 et les types de paramètres appropriés pour accéder aux données encodées souhaitées. Par exemple, transmettez \_ le paramètre de contenu CMSG \_ pour obtenir un pointeur vers l’intégralité du message [*PKCS \# 7*](../secgloss/p-gly.md) .

    Si le résultat de cet encodage doit être utilisé en tant que [*données internes*](../secgloss/i-gly.md) pour un autre message encodé, tel qu’un message enveloppé, le \_ \_ paramètre param CMSG Bare Content \_ doit être passé. Pour obtenir un exemple qui illustre cela, consultez [autre code pour l’encodage d’un message enveloppé](alternate-code-for-encoding-an-enveloped-message.md).

10. Fermez le message en appelant [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Le résultat de cette procédure est un message encodé qui contient les données d’origine, le hachage chiffré de ces données (signature) et les informations sur le signataire. Il y a également un pointeur vers l’objet BLOB encodé souhaité.

Pour plus d’informations sur le codage C, consultez [exemple de programme c : signature, encodage, décodage et vérification d’un message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
