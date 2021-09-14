---
description: Détaille la procédure d’encodage d’un message général.
ms.assetid: 554cab0d-cfa2-46a7-80d9-f41430eb4b47
title: Procédure d’encodage et de décodage des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49da09c2318fffd3d1c92d6012055172709609a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120846"
---
# <a name="procedure-for-encoding-and-decoding-messages"></a>Procédure d’encodage et de décodage des messages

La procédure d’encodage d’un message général est la suivante.

**Pour encoder un message**

1.  Initialisez les structures de données appropriées pour le type de données souhaité.
2.  Appelez [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), en passant les arguments nécessaires. Lors de l’appel de **CryptMsgOpenToEncode**, si les données qui doivent être fournies à [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) ont déjà été codées en message, transmettez l’identificateur d’objet approprié dans *pszInnerContentObjID* (par exemple, « 1.2.840.113549.1.7.2 » pour szOID \_ RSA \_ SignedData). Si *pszInnerContentObjID* a la **valeur null**, le type de [*contenu interne*](../secgloss/i-gly.md) est supposé ne pas avoir été précédemment encodé et traité correctement.
3.  Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) autant de fois que nécessaire pour terminer le message. Lors du dernier appel, définissez le paramètre *fFinal* sur **true**. (Pour plus d’informations, consultez **CryptMsgUpdate**).
4.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour obtenir un pointeur vers les paramètres souhaités, tels que le contenu. Pour l’encodage de données simples et générales, utilisez \_ \_ le paramètre de contenu CMSG pour *dwParamtype*.
5.  Fermez le message en appelant [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Cette procédure génère un message encodé d’un type spécifié dans les appels de fonction.

La procédure de décodage d’un message général se présente comme suit.

**Pour décoder un message**

1.  Déterminez la longueur nécessaire pour que la mémoire tampon contienne les données encodées à l’aide de [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength).
2.  Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), en passant les arguments nécessaires. Pour assurer la compatibilité avec Internet Explorer version 3,0, le paramètre *dwMsgType* est fourni. Les données signées créées dans Internet Explorer 3,0 ne contiennent pas d’informations d’en-tête. Par conséquent, si un tel message est extrait des signatures de fichier, le type de message doit être passé dans la fonction. Si la valeur zéro est passée dans le paramètre *dwMsgType* , la fonction lira le type de message dans l’en-tête du message. Si l’en-tête est manquant, l’appel de fonction échoue. En cas de réussite, un descripteur du message ouvert est retourné.
3.  Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) une fois. Cela entraîne le suivi des actions appropriées sur le message, en fonction du type de message.
4.  Pour un traitement supplémentaire du message, tel qu’un déchiffrement ou une vérification de signature supplémentaire, appelez [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), en passant l’action souhaitée dans *dwCtrlType*.
5.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour obtenir un pointeur vers les paramètres souhaités, tels que le contenu. Pour décoder des données générales simples, utilisez CMSG \_ Content \_ param pour le paramètre *dwParamtype* .
6.  Appelez [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) pour fermer le message.

Pour obtenir un exemple qui implémente ces étapes, consultez [exemple de programme C : encodage et décodage de données](example-c-program-encoding-and-decoding-data.md). Pour obtenir des procédures et un exemple illustrant le processus d’encodage, de décodage et de vérification de la signature d’un message signé, consultez [exemple de programme C : signature, encodage, décodage et vérification d’un message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
