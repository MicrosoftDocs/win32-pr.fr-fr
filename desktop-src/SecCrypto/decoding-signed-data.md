---
description: Processus de décodage des données signées.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Décodage des données signées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512950"
---
# <a name="decoding-signed-data"></a>Décodage des données signées

Le processus général suivant décode un type de [*données signé*](../secgloss/s-gly.md) .

**Pour décoder un message signé**

1.  Obtient un pointeur vers l’objet BLOB encodé.
2.  Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), en passant les arguments nécessaires.
3.  Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) une fois, en passant le handle récupéré à l’étape 2 et un pointeur vers les données qui doivent être décodées. Cela entraîne le suivi des actions appropriées sur le message, en fonction du type de message.
4.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant le handle récupéré à l’étape 2 et les types de paramètres appropriés pour accéder aux données décodées. Par exemple, transmettez \_ le paramètre de contenu CMSG \_ pour obtenir un pointeur vers le contenu décodé.

Le processus général suivant vérifie la signature d’un message décodé et signé.

**Pour vérifier la signature d’un message décodé, signé**

1.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en transmettant la valeur du paramètre handle du message et CMSG du \_ signataire du signataire \_ \_ \_ pour récupérer [**les \_ informations du certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) du signataire à partir du message.
2.  Appelez [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) pour ouvrir un magasin temporaire qui est initialisé avec les certificats du message.
3.  Appelez [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) pour récupérer les [**\_ informations de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) du signataire à partir des certificats inclus dans le message.
4.  Appelez [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), en transmettant CMSG \_ CTRL \_ verify \_ signature pour vérifier les signatures.
5.  Appelez [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) pour fermer le message.

Le résultat de ces procédures est que la signature est vérifiée et qu’un pointeur est récupéré dans le contenu du message décodé obtenu à l’étape 4 de la procédure de décodage d’un message signé.

Pour plus d’informations sur le codage C, consultez [exemple de programme c : signature, encodage, décodage et vérification d’un message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
