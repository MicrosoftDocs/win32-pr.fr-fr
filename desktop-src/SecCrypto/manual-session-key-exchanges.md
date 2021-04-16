---
description: Montre comment envoyer un message chiffré.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Échange de clés de session manuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556695"
---
# <a name="manual-session-key-exchanges"></a>Échange de clés de session manuelle

> [!Note]  
> La procédure décrite dans cette section suppose que les utilisateurs (ou les clients CryptoAPI) possèdent déjà leur propre ensemble de [*paires de clés publiques/privées*](../secgloss/p-gly.md) et ont également obtenu les [*clés publiques*](../secgloss/p-gly.md)de l’autre.

 

L’illustration suivante montre comment utiliser cette procédure pour envoyer un message chiffré.

![envoi d’un message chiffré](images/capi04.png)

Cette approche est vulnérable à au moins une forme d’attaque courante. Une personne malveillante peut acquérir des copies d’un ou de plusieurs messages chiffrés et de clés chiffrées. Ensuite, plus tard, l’écouteur peut envoyer l’un de ces messages au récepteur et le destinataire n’aura aucun moyen de savoir que le message ne provient pas directement de l’expéditeur d’origine. Ce risque peut être réduit en horodateurant tous les messages ou en utilisant des numéros de série.

Le moyen le plus simple d’envoyer des messages chiffrés à un autre utilisateur consiste à envoyer le message chiffré à l’aide d’une clé de session aléatoire avec la clé de session chiffrée avec la clé [*publique d’échange de clé*](../secgloss/k-gly.md)du récepteur.

Voici les étapes à suivre pour envoyer une clé de session chiffrée.

**Pour envoyer une clé de session chiffrée**

1.  Créez une [*clé de session*](../secgloss/s-gly.md) aléatoire à l’aide de la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .
2.  Chiffrez le message à l’aide de la clé de session. Cette procédure est décrite dans [chiffrement et déchiffrement des données](data-encryption-and-decryption.md).
3.  Exportez la clé de session dans un [*objet blob de clé*](../secgloss/k-gly.md) avec la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , en spécifiant que la clé doit être chiffrée avec la clé publique d’échange de clé de l’utilisateur de destination.
4.  Envoyez le message chiffré et l’objet BLOB de clé chiffrée à l’utilisateur de destination.
5.  L’utilisateur de destination importe l’objet BLOB de clé dans son CSP à l’aide de la fonction [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) . Cette opération déchiffre automatiquement la clé de session, à condition que la clé publique d’échange de clé de l’utilisateur de destination ait été spécifiée à l’étape 3.
6.  L’utilisateur de destination peut ensuite déchiffrer le message à l’aide de la clé de session, en suivant la procédure décrite dans [chiffrement et déchiffrement des données](data-encryption-and-decryption.md).

 

 
