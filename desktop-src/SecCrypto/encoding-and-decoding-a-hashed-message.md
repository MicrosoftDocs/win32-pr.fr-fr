---
description: Décrit les tâches requises pour encoder un message haché.
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: Encodage et décodage d’un message haché
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91d165634c1ae00a59f2c77b1fc5a36b53dbd96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416447"
---
# <a name="encoding-and-decoding-a-hashed-message"></a>Encodage et décodage d’un message haché

Les données hachées se composent d’un contenu de tout type et d’un [*hachage*](../secgloss/h-gly.md) du contenu. Il peut être utilisé lorsqu’il est nécessaire uniquement de confirmer que le contenu du message n’a pas été modifié depuis la création du hachage.

Lors de la création d’un message haché, il peut y avoir plusieurs algorithmes de hachage et plusieurs hachages. L’illustration suivante représente les tâches requises pour encoder un message haché. La procédure est décrite dans le texte qui suit l’illustration.

![création d’un message haché](images/hashmsg.png)

**Pour créer un message haché**

1.  Obtient un pointeur vers les données à hacher.
2.  Sélectionnez l’algorithme de hachage à utiliser.
3.  Placez les données à l’aide d’une fonction de hachage à l’aide de l’algorithme de hachage.
4.  Incluez les données d’origine à hacher, les algorithmes de hachage et les hachages dans le message encodé.

Pour utiliser les fonctions de message de bas niveau pour accomplir les tâches présentées ci-dessous, utilisez la procédure suivante.

**Pour hacher et encoder un message à l’aide de fonctions de message de bas niveau**

1.  Créez ou récupérez le contenu à hacher.
2.  Obtenir un fournisseur de services de chiffrement.
3.  Initialisez la structure d' [**\_ \_ \_ informations de codage hachée CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) .
4.  Appelez [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) pour connaître la taille de l’objet blob de message encodé. Allouez de la mémoire pour celui-ci.
5.  Appelez [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), en transmettant CMSG \_ haché pour le paramètre *dwMsgType* et un pointeur vers les [**\_ \_ \_ informations de codage hachées CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) pour le paramètre *pvMsgEncodeInfo* . À la suite de cet appel, vous obtenez un handle pour le message ouvert.
6.  Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), en passant le handle récupéré à l’étape 5 et un pointeur vers les données à hacher et à encoder. Cette fonction peut être appelée autant de fois que nécessaire pour terminer le processus d’encodage.
7.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant le handle récupéré à l’étape 5 et les types de paramètres appropriés pour accéder aux données encodées souhaitées. Par exemple, transmettez \_ le paramètre de contenu CMSG \_ pour obtenir un pointeur vers l’intégralité du message [*PKCS \# 7*](../secgloss/p-gly.md) .

    Si le résultat de cet encodage doit être utilisé comme [*données internes*](../secgloss/i-gly.md) pour un autre message encodé, tel qu’un message enveloppé, le \_ paramètre CMSG Bare \_ Content \_ doit être passé. Pour obtenir un exemple qui illustre cela, consultez [autre code pour l’encodage d’un message enveloppé](alternate-code-for-encoding-an-enveloped-message.md).

8.  Fermez le message en appelant [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Le résultat de cette procédure est un message encodé qui contient les données d’origine, les algorithmes de hachage et le [*hachage*](../secgloss/h-gly.md) de ces données. Un pointeur vers l' [*objet BLOB*](../secgloss/b-gly.md) de message encodé est obtenu à l’étape 7.

Les deux procédures suivantes décodent puis vérifient les données hachées.

**Pour décoder des données hachées**

1.  Obtient un pointeur vers l’objet BLOB encodé.
2.  Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), en passant les arguments nécessaires.
3.  Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) une fois, en passant le handle récupéré à l’étape 2 et un pointeur vers les données qui doivent être décodées. Cela entraîne le suivi des actions appropriées sur le message, en fonction du type de message.
4.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant le handle récupéré à l’étape 2, et les types de paramètres appropriés pour accéder aux données décodées souhaitées. Par exemple, transmettez \_ le paramètre de contenu CMSG \_ pour obtenir un pointeur vers le contenu décodé.

**Pour vérifier le hachage**

1.  Appelez [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), en passant \_ \_ le hachage CMSG Ctrl Verify \_ pour vérifier les hachages.
2.  Appelez [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) pour fermer le message.

Pour obtenir un exemple de programme, consultez [exemple de programme C : encodage et décodage d’un message haché](example-c-program-encoding-and-decoding-a-hashed-message.md).

 

 
