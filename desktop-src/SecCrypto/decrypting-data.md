---
description: Présente les étapes permettant de déchiffrer un message chiffré.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Déchiffrement de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600903d7a3060c83cd7cd0a85e92f96efe4fb0cfa30c2936c5546f71138b6854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875689"
---
# <a name="decrypting-data"></a>Déchiffrement de données

Cette section présente les étapes permettant de déchiffrer un message chiffré.

**Pour déchiffrer un message chiffré**

1.  Obtient un pointeur vers le message enveloppé numériquement.
2.  Ouvrez un magasin de certificats.
3.  À partir du message, récupérez l’identificateur du destinataire (mon ID).
4.  Utilisez l’identificateur de destinataire pour récupérer le certificat.
5.  Obtenir la clé privée du certificat.
6.  Utilisez la clé privée pour déchiffrer la clé symétrique (session).
7.  Récupérez l’algorithme de chiffrement du message.
8.  À l’aide de la clé de session déchiffrée et de l’algorithme de chiffrement, déchiffrez les données.

[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) effectue toutes les tâches de déchiffrement d’un message. Toutefois, l’initialisation des structures et d’autres données est toujours nécessaire.

**Pour déchiffrer des données à l’aide de CryptDecryptMessage**

1.  Obtient un pointeur vers l’objet BLOB chiffré.
2.  Ouvrez un magasin de certificats.
3.  Créez un groupe de magasins de certificats.
4.  Initialisez la structure de la [**\_ para- \_ message \_ de déchiffrement**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) .
5.  Appelez [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour déchiffrer les données contenues dans le message.

[Exemple de programme C : l’utilisation de CryptEncryptMessage et de CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implémente la procédure qui vient d’être présentée. Les commentaires indiquent les éléments de code qui effectuent chaque étape de la procédure. Pour plus d’informations sur la fonction, consultez [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)et pour plus d’informations sur la structure de données, consultez [**\_ crypt Decrypt \_ message \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).

 

 



