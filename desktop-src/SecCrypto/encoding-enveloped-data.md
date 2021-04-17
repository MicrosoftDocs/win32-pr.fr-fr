---
description: La syntaxe de message de chiffrement peut être utilisée pour encoder des messages enveloppés.
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: Encodage de données enveloppées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dc20fc7483ba1ef364d8b59824d26bd14d458d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563106"
---
# <a name="encoding-enveloped-data"></a>Encodage de données enveloppées

Les données enveloppées se composent d’un contenu chiffré de tout type et de clés de session de chiffrement de contenu chiffrées pour un ou plusieurs destinataires. Les messages enveloppés conservent le contenu du message secret et autorisent uniquement les personnes ou les entités spécifiées à récupérer le contenu.

La syntaxe de message de chiffrement (CMS) peut être utilisée pour encoder des messages enveloppés. CMS prend en charge trois techniques de gestion de clés : le transport de clé, l’accord de clé et les clés de chiffrement de clé symétrique (KEK) précédemment distribuées. Les KEK symétriques précédemment distribués sont également appelées distribution de clé de liste de diffusion.

Dans chacune de ces trois techniques, une clé de session unique est générée pour chiffrer le message enveloppé. Les problèmes de gestion de clés concernent la façon dont la clé de session est chiffrée par l’expéditeur et déchiffrée par un destinataire. Un seul message chiffré peut être distribué à de nombreux destinataires à l’aide d’une combinaison des techniques de gestion de clés.

La gestion des clés de transport de clé utilise la clé publique du récepteur prévu pour chiffrer la clé de session. Le récepteur déchiffre la clé de session à l’aide de la clé privée associée à la clé publique qui a été utilisée pour chiffrer. Le récepteur utilise ensuite la clé de session déchiffrée pour déchiffrer les données enveloppées. Lorsque le transport de clé est utilisé, le destinataire n’a pas confirmé les informations sur l’identité de l’expéditeur.

Dans la gestion d’un accord de clé, une clé privée temporaire Diffie-Hellman éphémère est générée et utilisée pour chiffrer la clé de session. La clé publique correspondant à la clé privée éphémère est incluse dans le cadre des informations de destinataire du message. Le destinataire déchiffre la clé de session à l’aide de la clé éphémère reçue et utilise cette clé de session déchiffrée pour déchiffrer le message enveloppé. À l’aide de l’accord de clé éphémère conjointement avec la clé privée du destinataire, le destinataire du message a confirmé des informations sur l’identité de l’expéditeur.

Pour la gestion des clés à l’aide de [*clés symétriques*](../secgloss/s-gly.md)précédemment distribuées, chaque message inclut la clé de chiffrement de contenu qui a été chiffrée avec une clé de chiffrement de clé précédemment distribuée. Les destinataires utilisent la clé de chiffrement de clé précédemment distribuée pour déchiffrer la clé de chiffrement de contenu, puis utiliser la clé de chiffrement de contenu déchiffrée pour déchiffrer le message enveloppé.

L’illustration suivante montre une séquence CMS d’événements type pour l’encodage des données enveloppées.

![encodage de données enveloppées](images/envelmsg.png)

-   Un pointeur vers le message de [*texte en clair*](../secgloss/p-gly.md) est récupéré.
-   Une clé symétrique ([*session*](../secgloss/s-gly.md)) est générée.
-   La [*clé symétrique*](../secgloss/s-gly.md) et l’algorithme de chiffrement spécifié sont utilisés pour chiffrer les données du message.
-   Un [*magasin de certificats*](../secgloss/c-gly.md) est ouvert.
-   Le certificat du destinataire est récupéré à partir du magasin.
-   La [*clé publique*](../secgloss/p-gly.md) est récupérée à partir du certificat du destinataire.
-   À l’aide de la clé publique du destinataire, la clé symétrique est chiffrée.
-   À partir du certificat du destinataire, l’ID du destinataire est récupéré.
-   Les informations suivantes sont incluses dans le message enveloppé numériquement : l’algorithme de chiffrement des données, les données chiffrées, la clé symétrique chiffrée et la structure d’informations du destinataire.

Pour utiliser les fonctions de message de bas niveau pour accomplir les tâches courantes qui viennent d’être listées, utilisez la procédure suivante.

**Pour encoder un message enveloppé**

1.  Créez ou récupérez le contenu.
2.  Obtenir un fournisseur de services de chiffrement.
3.  Obtenir un certificat de destinataire.
4.  Initialisez la structure d' [**\_ \_ \_ informations d’encodage enveloppée CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) .
5.  Appelez [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) pour connaître la taille de l’objet blob de message encodé. Allouez de la mémoire pour celui-ci.
6.  Appelez [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), en passant CMSG \_ envelopped pour *dwMsgType* et un pointeur vers [**CMSG \_ informations de \_ codage \_ enveloppé**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) pour *pvMsgEncodeInfo*. À la suite de cet appel, vous obtiendrez un handle pour le message ouvert.
7.  Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), en passant le handle récupéré à l’étape 6 et un pointeur vers les données qui doivent être chiffrées, enveloppées et encodées. Cette fonction peut être appelée autant de fois que nécessaire pour terminer le processus d’encodage.
8.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant le handle récupéré à l’étape 6 et les types de paramètres appropriés pour accéder aux données encodées souhaitées. Par exemple, transmettez \_ le paramètre de contenu CMSG \_ pour obtenir un pointeur vers l’intégralité du \# message PKCS 7.

    Si le résultat de cet encodage doit être utilisé en tant que [*données internes*](../secgloss/i-gly.md) pour un autre message encodé, tel qu’un message enveloppé, le \_ \_ paramètre param CMSG Bare Content \_ doit être passé. Pour obtenir un exemple, consultez [autre code pour l’encodage d’un message enveloppé](alternate-code-for-encoding-an-enveloped-message.md).

9.  Fermez le message en appelant [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Le résultat de cette procédure est un message encodé qui contient les données chiffrées, la [*clé symétrique*](../secgloss/s-gly.md) qui est chiffrée avec les clés publiques du destinataire et les structures de données d’informations de destinataire. La combinaison du contenu chiffré et d’une clé symétrique chiffrée pour un destinataire est une [*enveloppe numérique*](../secgloss/d-gly.md) pour ce destinataire. N’importe quel type de contenu peut être enveloppé pour plusieurs destinataires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de programme C : encodage d’un message signé et enveloppé](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
