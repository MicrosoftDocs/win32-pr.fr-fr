---
description: Ces étapes vérifient la signature des données signées.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Vérification d’un message signé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7bfdac1b16351d51197a84c15688b0724340af34681312b9cb9865900b8dfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970976"
---
# <a name="verifying-a-signed-message"></a>Vérification d’un message signé

Ces étapes vérifient la signature des données signées. L’illustration suivante représente les tâches individuelles qui doivent être accomplies, comme indiqué dans la liste qui la suit.

![vérification d’un message signé](images/verifmsg.png)

**Pour vérifier la signature d’un message signé**

1.  Obtient un pointeur vers le message signé.
2.  Ouvrez un [*magasin de certificats*](../secgloss/c-gly.md).
3.  À l’aide de l’ID du signataire contenu dans le message, récupérez le certificat de l’expéditeur et recevez un handle de sa [*clé publique*](../secgloss/p-gly.md).

    Comme alternative aux étapes 2 et 3, vous pouvez utiliser le certificat contenu dans le message pour récupérer la clé publique du signataire.

4.  À l’aide de la clé publique du signataire, déchiffrez la signature numérique, en générant le condensé d’origine des données dans le message.
5.  À l’aide de l’algorithme de hachage contenu dans le message, [*Hachez*](../secgloss/h-gly.md) les données contenues dans le message, en générant un nouveau condensé.
6.  Comparez le condensé récupéré à partir du message avec le nouveau condensé que vous venez de créer.
7.  Si les deux résumés correspondent, la signature est vérifiée. Cela signifie que la [*clé privée*](../secgloss/p-gly.md) qui a été utilisée pour signer les données correspond à la clé publique utilisée pour déchiffrer la signature, et que les données n’ont pas changé depuis la signature des données.

    Si les deux résumés ne correspondent pas, cela signifie que la signature n’est pas vérifiée et que les clés privée/publique ne correspondent pas, ou que les données ont été modifiées depuis la signature des données, ou les deux à la fois.

Une seule fonction, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), peut être utilisée pour vérifier une signature, comme indiqué dans la procédure suivante.

**Pour vérifier un message signé**

1.  Obtient un pointeur vers le message signé.
2.  Obtient la taille du message signé.
3.  Obtenir un handle sur un fournisseur de services de chiffrement.
4.  Initialisez la structure du [**\_ \_ message \_ de vérification**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) de chiffrement.
5.  Appelez [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) pour vérifier la signature.

Le code qui implémente cette procédure est inclus dans l' [exemple de programme C : signature d’un message et vérification d’une signature de message](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
