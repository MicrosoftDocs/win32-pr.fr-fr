---
description: Schannel utilise CryptoAPI pour les opérations de chiffrement telles que le stockage des clés publiques/privées.
ms.assetid: 5ad9a171-5f69-4035-aac5-ae8d27d0abfb
title: Schannel et CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0684cd690911444b77ba27d2876e578fd71c73a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393356"
---
# <a name="schannel-and-cryptoapi"></a>Schannel et CryptoAPI

Schannel utilise [CryptoAPI](../seccrypto/cryptography-essentials.md) pour les opérations de chiffrement telles que le stockage des [*clés publiques/privées*](../secgloss/p-gly.md).

Les rubriques suivantes fournissent des informations détaillées sur la façon dont Schannel utilise CryptoAPI.



| Rubrique                                                                   | Description                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Magasin de certificats](certificate-stores.md)<br/>                 | Les certificats client et serveur doivent être stockés dans un magasin de certificats.<br/>                                |
| [CryptoAPI 2.0 les clés privées](cryptoapi-2-0-private-keys.md)<br/> | Les informations d’identification Schannel sont représentées en interne en tant que structures de [**\_ contexte de certificat**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .<br/> |



 

 

 
