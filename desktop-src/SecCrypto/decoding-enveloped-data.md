---
description: Tâches générales requises pour décoder un message enveloppé.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Décodage des données enveloppées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df9df80b2a4bc1e3c9d6894bc83624908468edb63f7d0283ee3dca1b50a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767807"
---
# <a name="decoding-enveloped-data"></a>Décodage des données enveloppées

Les tâches générales requises pour décoder un message enveloppé sont illustrées dans l’illustration suivante et décrites dans la liste qui suit.

![décodage des données enveloppées](images/decemsg.png)

La séquence d’événements pour décoder les données enveloppées à l’aide de la gestion de clés de transport de clé, comme illustré dans l’illustration précédente, est la suivante :

-   Un pointeur vers le message [*enveloppé numériquement*](../secgloss/d-gly.md) est récupéré.
-   Un [*magasin de certificats*](../secgloss/c-gly.md) est ouvert.
-   À partir du message, l’ID de destinataire (mon ID) est récupéré.
-   L’ID de destinataire est utilisé pour récupérer le certificat.
-   La [*clé privée*](../secgloss/p-gly.md) associée à ce certificat est récupérée.
-   La clé privée est utilisée pour déchiffrer la clé [*symétrique*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)).
-   L’algorithme de chiffrement est récupéré à partir du message.
-   À l’aide de la clé privée et de l’algorithme de chiffrement, les données sont déchiffrées.

La procédure suivante utilise des fonctions de message de bas niveau pour accomplir les tâches que vous venez de répertorier.

**Pour décoder un message enveloppé**

1.  Obtient un pointeur vers l’objet BLOB encodé.
2.  Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), en passant les arguments nécessaires.
3.  Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) une fois, en passant le handle récupéré à l’étape 2 et un pointeur vers les données qui doivent être décodées. Cela entraîne le suivi des actions appropriées sur le message, en fonction du type de message.
4.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant le handle récupéré à l’étape 2 et \_ le \_ paramètre de type CMSG pour vérifier que le message est du type de données enveloppé.
5.  Appelez à nouveau [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant \_ \_ le paramètre de type de contenu interne CMSG \_ \_ pour récupérer le type de données du [*contenu interne*](../secgloss/i-gly.md).
6.  Si le type de données de contenu interne est **Data**, effectuez le déchiffrement et le décodage du contenu. Sinon, exécutez une procédure de décodage appropriée pour le type de données de contenu.
7.  En supposant que le type de contenu interne est « Data », initialisez la structure de données [**CMSG \_ CTRL \_ decrypte \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) , puis appelez [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), en passant CMSG \_ CTRL \_ et l’adresse de la structure. Le contenu sera déchiffré.
8.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant \_ le paramètre de contenu CMSG \_ pour obtenir un pointeur vers l’objet blob de données décodées (chaîne d'**octets** ).
9.  Appelez [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) pour fermer le message.

Le résultat de cette procédure est que le message est décodé et déchiffré et qu’un pointeur est récupéré dans l’objet BLOB de données de contenu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de programme C : encodage d’un message signé et enveloppé](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
