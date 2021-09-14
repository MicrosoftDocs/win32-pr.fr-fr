---
description: Tous les protocoles Schannel requièrent que le serveur fournisse un certificat d’une autorité de certification approuvée comme preuve de son identité.
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: Exécution de l’authentification à l’aide de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a37b8dedf07680286288234c7ca4422f44c2c3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123337"
---
# <a name="performing-authentication-using-schannel"></a>Exécution de l’authentification à l’aide de Schannel

Tous les protocoles Schannel requièrent que le serveur fournisse un [*certificat*](../secgloss/c-gly.md) d’une [*autorité de certification*](../secgloss/c-gly.md) approuvée comme preuve de son identité. Ce processus est appelé authentification du serveur. L’authentification du client, où le client fournit une preuve de son identité, est facultative et peut être demandée par le serveur à tout moment.

## <a name="authenticating-the-server"></a>Authentification du serveur

Le comportement par défaut de Schannel consiste à utiliser la fonction [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) pour vérifier l' [*intégrité*](../secgloss/i-gly.md) et la propriété du [*certificat de serveur*](../secgloss/s-gly.md). Pour désactiver cette fonctionnalité, spécifiez \_ \_ \_ la validation du CRED manuel d’ISC req lors de \_ l’appel de la fonction [**InitializeSecurityContext (SChannel)**](./initializesecuritycontext--schannel.md) . Pour plus d’informations, consultez [validation manuelle des informations d’identification Schannel](manually-validating-schannel-credentials.md).

## <a name="authenticating-the-client"></a>Authentification du client

Schannel ne valide pas les certificats du client ; le serveur doit effectuer cette authentification manuellement. En règle générale, le serveur vérifie l’identité du client dans une base de données contenant des informations sur le compte d’utilisateur. Pour les serveurs qui doivent obtenir le compte d’un client à l’aide d’un certificat, consultez [mappage de certificats](mapping-certificates.md).

Lorsque le serveur demande l’authentification du client, le client doit envoyer au serveur l’un de ses certificats. Par défaut, Schannel n’envoie aucune notification au client et tente de localiser un [*certificat client*](../secgloss/c-gly.md) et de l’envoyer au serveur. Pour désactiver cette fonctionnalité, les clients spécifient \_ \_ les références d’identification fournies par l’ISC \_ \_ en appelant la fonction [**InitializeSecurityContext (SChannel)**](./initializesecuritycontext--schannel.md) . Lorsque cet indicateur est spécifié, Schannel retourne \_ \_ \_ les informations d’identification des e/s incomplètes au client lorsque le serveur demande l’authentification et que le client n’a pas fourni de certificat précédemment.

 

 
