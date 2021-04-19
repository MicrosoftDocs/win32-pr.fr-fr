---
description: Les fournisseurs de services de chiffrement \_ RSA \_ Schannel doivent prendre en charge le \_ hachage CALG SSL3 \_ SHAMD5 qui est compatible avec le fournisseur de services de chiffrement de base Microsoft utilisé dans l’authentification du client SSL 3,0 et TLS 1,0.
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: Type de signature SHA/MD5 RSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106539051"
---
# <a name="shamd5-rsa-signature-type"></a>Type de signature SHA/MD5 RSA

Les fournisseurs de services de chiffrement \_ RSA \_ Schannel doivent prendre en charge le \_ hachage CALG SSL3 \_ SHAMD5 qui est compatible avec le fournisseur de services de chiffrement de base Microsoft utilisé dans l’authentification du client SSL 3,0 et TLS 1,0. [](../secgloss/h-gly.md) Ce hachage est constitué d’une concaténation d’un hachage [*MD5*](../secgloss/m-gly.md) et d’un hachage SHA signé avec une clé privée RSA ou Diffie-Hellman. Un handle vers une valeur de hachage de ce type est créé à l’aide de la fonction [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) ou [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) avec CALG \_ SSL3 \_ SHAMD5 comme paramètre *algid* . Vous pouvez consulter des exemples de fonctions de hachage dans l' [exemple de programme c : création et hachage d’une clé de session](example-c-program-creating-and-hashing-a-session-key.md) et [exemple de programme c : signature d’un hachage et vérification de la signature de hachage](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).

 

 
