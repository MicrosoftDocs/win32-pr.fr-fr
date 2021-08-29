---
description: Lorsqu’un document ou un texte doit être protégé par un seul utilisateur ou que le document doit être partagé entre un petit groupe de personnes qui ont toutes accès au même mot de passe secret, le chiffrement/déchiffrement simple peut être effectué.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Chiffrement et déchiffrement de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250212864ed7cdd9bcd0c7778ae0d0b9209169f5ab36e4fa25e8a336e8da79aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874469"
---
# <a name="encrypting-and-decrypting-data"></a>Chiffrement et déchiffrement de données

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Lorsqu’un document ou un texte doit être protégé par un seul utilisateur ou que le document doit être partagé entre un petit groupe de personnes qui ont toutes accès au même mot de passe secret, le chiffrement/déchiffrement simple peut être effectué. CAPICOM ne prend pas en charge le \# type de contenu PKCS 7 EncryptedData, mais utilise une structure ASN non standard pour EncryptedData. Par conséquent, seul CAPICOM peut déchiffrer un objet CAPICOM EncryptedData.

Les sections suivantes présentent des exemples de tâches de chiffrement et de déchiffrement :

-   [Chiffrement d’un message dans CAPICOM](encrypting-a-message-in-capicom.md)
-   [Déchiffrement d’un message dans CAPICOM](decrypting-a-message-in-capicom.md)

 

 



