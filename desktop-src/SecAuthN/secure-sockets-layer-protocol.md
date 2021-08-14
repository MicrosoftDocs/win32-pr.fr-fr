---
description: les informations contenues dans cette rubrique s’appliquent à Windows Server 2003 et Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Protocole SSL (Secure Sockets Layer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8e6b7232db8bef98d5170887d6be75c9770927954a40b606450bf214efdf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918382"
---
# <a name="secure-sockets-layer-protocol"></a>Protocole SSL (Secure Sockets Layer)

les informations contenues dans cette rubrique s’appliquent à Windows Server 2003 et Windows XP. pour les suites de chiffrement pour Windows Server 2008 et Windows Vista, voir [suites de chiffrement dans Schannel](cipher-suites-in-schannel.md).

Schannel prend en charge les versions 2,0 et 3,0 du [*protocole SSL (Secure Sockets Layer) (SSL)*](../secgloss/s-gly.md).

> [!Note]  
> à partir de Windows 10, version 1607 et Windows Server 2016, SSL 2,0 a été supprimé et n’est plus pris en charge.

 

## <a name="ssl-30"></a>SSL 3.0

SSL 3,0 est le prédécesseur du [protocole TLS (Transport Layer Security](transport-layer-security-protocol.md)).

Schannel prend en charge les suites de chiffrement listées sous [suites de chiffrement TLS](tls-cipher-suites.md) pour SSL 3,0. SSL 3,0 prend en charge toutes les suites de chiffrement listées sous les suites de chiffrement TLS, ainsi que les \_ Kea Fortezza SSL \_ \_ avec \_ Fortezza \_ CBC \_ Sha.

## <a name="ssl-20"></a>SSL 2.0

SSL 2,0 a été remplacé par TLS et ne doit pas être utilisé pour un nouveau développement.

Schannel prend en charge les suites de chiffrement suivantes pour SSL 2,0. Les suites sont répertoriées dans l’ordre, de la plus sécurisée à la moins sécurisée.

-   SSL \_ RC4 \_ 128 \_ avec \_ MD5
-   SSL \_ des \_ 192 \_ EDE3 \_ CBC \_ avec \_ MD5
-   SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ avec \_ MD5
-   SSL \_ des \_ 64 \_ CBC \_ avec \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ avec \_ MD5

 

 
