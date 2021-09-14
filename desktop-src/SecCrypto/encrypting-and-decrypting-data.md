---
description: Lorsqu’un document ou un texte doit être protégé par un seul utilisateur ou que le document doit être partagé entre un petit groupe de personnes qui ont toutes accès au même mot de passe secret, le chiffrement/déchiffrement simple peut être effectué.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Chiffrement et déchiffrement de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416424"
---
# <a name="encrypting-and-decrypting-data"></a>Chiffrement et déchiffrement de données

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Lorsqu’un document ou un texte doit être protégé par un seul utilisateur ou que le document doit être partagé entre un petit groupe de personnes qui ont toutes accès au même mot de passe secret, le chiffrement/déchiffrement simple peut être effectué. CAPICOM ne prend pas en charge le \# type de contenu PKCS 7 EncryptedData, mais utilise une structure ASN non standard pour EncryptedData. Par conséquent, seul CAPICOM peut déchiffrer un objet CAPICOM EncryptedData.

Les sections suivantes présentent des exemples de tâches de chiffrement et de déchiffrement :

-   [Chiffrement d’un message dans CAPICOM](encrypting-a-message-in-capicom.md)
-   [Déchiffrement d’un message dans CAPICOM](decrypting-a-message-in-capicom.md)

 

 



