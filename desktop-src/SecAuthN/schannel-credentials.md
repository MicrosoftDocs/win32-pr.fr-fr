---
description: Les protocoles Schannel requièrent des informations d’identification pour authentifier les serveurs et, éventuellement, les clients.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Informations d’identification Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951884"
---
# <a name="schannel-credentials"></a>Informations d’identification Schannel

Les protocoles Schannel requièrent des informations d’identification pour authentifier les serveurs et, éventuellement, les clients. L’authentification du serveur, où le serveur fournit la preuve de son identité au client, est requise par les [*protocoles de sécurité*](../secgloss/s-gly.md)Schannel. L’authentification du client peut être demandée par le serveur à tout moment.

Les informations d’identification Schannel sont des certificats [*X. 509*](../secgloss/x-gly.md) . Les informations de clés [*publiques*](../secgloss/p-gly.md) et [*privées*](../secgloss/p-gly.md) des certificats sont utilisées pour authentifier le serveur et éventuellement le client. Ces clés sont également utilisées pour assurer [*l’intégrité*](../secgloss/i-gly.md) des messages lorsque le client et le serveur échangent les informations requises pour générer et échanger des [*clés de session*](../secgloss/s-gly.md).

Pour plus d’informations sur la programmation, consultez [obtention d’informations d’identification Schannel](obtaining-schannel-credentials.md).

 

 
