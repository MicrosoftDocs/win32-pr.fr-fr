---
description: Schannel retourne les messages d’erreur suivants lorsque l’alerte correspondante est reçue des protocoles TLS (Transport Layer Security) ou SSL (Secure Sockets Layer) (SSL).
ms.assetid: 0a6ac61d-a00c-4fc8-a995-d25d17e405df
title: Codes d’erreur Schannel pour les alertes TLS et SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9fdba202e63d212fc85f0c02eb5ac9dc20db047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951883"
---
# <a name="schannel-error-codes-for-tls-and-ssl-alerts"></a>Codes d’erreur Schannel pour les alertes TLS et SSL

[*Schannel*](../secgloss/s-gly.md) retourne les messages d’erreur suivants lorsque l’alerte correspondante est reçue des protocoles TLS ( [*Transport Layer Security*](../secgloss/t-gly.md) ) ou [*SSL (Secure Sockets Layer)*](../secgloss/s-gly.md) (SSL). Les messages d’erreur sont définis dans Winerror. h.



| Alerte TLS ou SSL                                           | Code d’erreur Schannel                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| \_Message d’alerte SSL3 \_ inattendu \_<br/> 10<br/>  | s \_ E \_ \_ message illégal<br/> 0x80090326<br/>             |
| Alerte TLS1- \_ \_ Mac d’enregistrement incorrect \_ \_<br/> 20<br/>     | s \_ \_ message électronique \_ modifié<br/> 0x8009030F<br/>             |
| \_Échec du \_ déchiffrement d’alerte TLS1 \_<br/> 21<br/>   | \_échec de \_ déchiffrement s E \_<br/> 0x80090330<br/>             |
| \_Dépassement d' \_ enregistrement d’alerte TLS1 \_<br/> 22<br/>     | s \_ E \_ \_ message illégal<br/> 0x80090326<br/>             |
| Échec de la \_ DÉcompression d’alerte SSL3 \_ \_<br/> 30<br/>  | s \_ \_ message électronique \_ modifié<br/> 0x8009030F<br/>             |
| \_Échec de \_ négociation d’alerte SSL3 \_<br/> 40<br/>   | s \_ E \_ \_ message illégal<br/> 0x80090326<br/>             |
| \_Alerte TLS1 \_ certificat incorrect \_<br/> 42<br/>     | s \_ \_ certificat E \_ inconnu<br/> 0x80090327<br/>                |
| \_ \_ Certificat non pris en charge par l’alerte TLS1 \_<br/> 43<br/>    | s \_ \_ certificat E \_ inconnu<br/> 0x80090327<br/>                |
| \_Certificat d’alerte TLS1 \_ \_ révoqué<br/> 44<br/> | chiffrer \_ E \_ révoqué<br/> 0x80092010<br/>                    |
| Le \_ certificat d’alerte TLS1 \_ \_ a expiré<br/> 45<br/> | s \_ \_ a expiré le certificat E \_<br/> 0x80090328<br/>                |
| \_Certificat d’alerte TLS1 \_ \_ inconnu<br/> 46<br/> | s \_ \_ certificat E \_ inconnu<br/> 0x80090327<br/>                |
| \_Paramètre d’alerte SSL3 \_ non conforme \_<br/>                 | s \_ E \_ \_ message illégal<br/> 0x80090326<br/>             |
| Alerte TLS1 d' \_ \_ autorité de \_ certification inconnue<br/> 48<br/>          | SEC \_ E \_ racine non approuvée \_<br/> 0x80090325<br/>              |
| \_ \_ Accès à l’alerte TLS1 \_ refusé<br/> 49<br/>       | s \_ \_ ouverture de session \_ refusée<br/> 0x8009030C<br/>                |
| \_Erreur de \_ décodage d’alerte TLS1 \_<br/> 50<br/>        | s \_ E \_ \_ message illégal<br/> 0x80090326<br/>             |
| \_Erreur de \_ déchiffrement de l’alerte TLS1 \_<br/> 51<br/>       | \_échec de \_ déchiffrement s E \_<br/> 0x80090330<br/>             |
| \_Restriction d' \_ exportation d’alerte TLS1 \_<br/> 60<br/>  | s \_ E \_ \_ message illégal<br/> 0x80090326<br/>             |
| \_Version du \_ protocole d’alerte TLS1 \_<br/> 70<br/>    | SEC \_ E \_ fonction non prise en charge \_<br/> 0x80090302<br/>        |
| TLS1 \_ alerte \_ insuffisante \_ sécurité<br/> 71<br/> | incompatibilité de l' \_ \_ algorithme sec E \_<br/> 0x80090331<br/>          |
| \_ \_ Erreur interne de l’alerte TLS1 \_<br/> 80<br/>      | SEC \_ E \_ \_ erreur interne<br/> 0x80090304<br/>              |
| Annulation de l’utilisateur de l' \_ alerte TLS1 \_ \_<br/> 90<br/>       | contexte d’E/s non \_ \_ terminé \_ \_ supprimé<br/> 0x80090333<br/> |
| \_Alerte TLS1 \_ aucune \_ renégociation<br/> 100<br/>   | s \_ E \_ \_ message illégal<br/> 0x80090326<br/>             |
| \_Alerte TLS1 \_ non prise en charge \_<br/> 110<br/>    | s \_ E \_ \_ message illégal<br/> 0x80090326<br/>             |
| Default<br/>                                         | s \_ E \_ \_ message illégal<br/> 0x80090326<br/>             |



 

 

 
