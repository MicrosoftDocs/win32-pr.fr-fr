---
description: Décrit les étapes à suivre pour chiffrer un message avec les fonctions de chiffrement de base.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Chiffrement de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d2a7fde500397959f0a2352b3f8ddb4fa662209afb251ddceaa8774048f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874452"
---
# <a name="encrypting-data"></a>Chiffrement de données

La procédure suivante décrit les étapes à suivre pour chiffrer un message avec les fonctions de chiffrement de base. Pour chiffrer les messages à l’aide des \# normes PKCS 7, consultez [fonctions de message de bas niveau](cryptography-functions.md) et [fonctions de message simplifiées](cryptography-functions.md).

**Pour chiffrer un message**

1.  Générez une clé de session à l’aide de la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .

    Cet appel génère une clé aléatoire et retourne un descripteur afin que la clé puisse être utilisée pour chiffrer et déchiffrer les données. L’algorithme de chiffrement à utiliser est également spécifié à ce stade. Comme CryptoAPI ne permet pas aux applications d’utiliser des algorithmes de clé publique pour chiffrer les données en bloc, spécifiez un algorithme symétrique tel que RC2 ou RC4 avec l’appel [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .

2.  Vous pouvez également utiliser la fonction [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) pour transformer un mot de passe en une clé adaptée au chiffrement.

    Si une application doit chiffrer le message afin que toute personne disposant d’un mot de passe spécifié puisse déchiffrer les données, utilisez [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) pour transformer le mot de passe en une clé adaptée au chiffrement.

    > [!Note]  
    > Dans ce cas, cette fonction est appelée à la place de la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) et les appels [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) suivants ne sont pas nécessaires.

     

3.  Si nécessaire, définissez des propriétés de chiffrement supplémentaires de la clé à l’aide de la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)

    Une fois la clé générée, les propriétés de chiffrement supplémentaires de la clé peuvent être définies avec la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam). Cette fonction permet aux différentes sections du fichier d’être chiffrées à l’aide de différents sels de clé et fournit un moyen de modifier le mode de chiffrement ou le vecteur d’initialisation de la clé. Ces paramètres peuvent être utilisés pour rendre le chiffrement conforme à une norme de chiffrement de données particulière.

4.  Chiffrez les données dans le fichier avec la fonction [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) .

    La fonction [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) prend la clé de session générée à l’étape précédente et chiffre une mémoire tampon de données.

    > [!Note]  
    > À mesure que les données sont chiffrées, les données peuvent être légèrement développées par l’algorithme de chiffrement. L’application est responsable de la mémorisation de la longueur des données chiffrées afin que la longueur appropriée puisse être spécifiée ultérieurement pour la fonction [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .

     

5.  Si vous le souhaitez, utilisez la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) pour permettre à l’utilisateur actuel de déchiffrer les données à l’avenir.

    Pour permettre à l’utilisateur actuel de déchiffrer les données à l’avenir, la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) est utilisée pour enregistrer la clé de déchiffrement sous une forme chiffrée (un objet blob de clé) qui peut uniquement être déchiffrée avec la clé privée de l’utilisateur. Cette fonction requiert la clé publique d’échange de clés de l’utilisateur à cet effet, qui peut être obtenue à l’aide de la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) . La fonction **CryptExportKey** retourne un objet blob de clé qui doit être stocké par l’application pour être utilisé dans le déchiffrement du fichier

> [!Note]  
> Si l’application possède des certificats (ou des clés publiques) pour d’autres utilisateurs, elle peut permettre à d’autres utilisateurs de déchiffrer le fichier en effectuant des appels [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) pour chaque utilisateur qui doit recevoir l’accès. Les objets BLOB de clé retournés doivent être stockés par l’application, comme à l’étape 5.

 

## <a name="creating-an-encrypted-message"></a>Création d’un message chiffré

Les fonctions de message simplifiées facilitent le chiffrement et le déchiffrement des données. L’illustration suivante représente les tâches individuelles qui doivent être accomplies pour chiffrer un message. Les étapes sont décrites dans la liste suivante.

![chiffrement d’un message](images/encmsg.png)

**Pour chiffrer un message**

1.  Obtient un pointeur vers le message de texte en clair.
2.  Générez une clé symétrique (session).
3.  À l’aide de la clé symétrique et de l’algorithme de chiffrement spécifié, chiffrez les données du message.
4.  Ouvrez un magasin de certificats.
5.  Obtient le certificat du destinataire.
6.  Récupération de la clé publique à partir du certificat du destinataire.
7.  À l’aide de la clé publique du destinataire, chiffrez la clé symétrique.
8.  Obtient l’identificateur du destinataire à partir du certificat du destinataire.
9.  Incluez ce qui suit dans le message enveloppé numériquement : l’algorithme de chiffrement des données, les données chiffrées, la clé symétrique chiffrée et l’identificateur du destinataire.

 

 



