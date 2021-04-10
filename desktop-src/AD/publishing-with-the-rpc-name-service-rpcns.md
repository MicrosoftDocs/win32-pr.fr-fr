---
title: Publication avec le service de noms RPC
description: Les services RPC peuvent publier leurs identificateurs dans un espace de noms à l’aide des API RpcNs (RPC Name Service).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Publication avec la publicité service de noms RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030992"
---
# <a name="publishing-with-the-rpc-name-service"></a>Publication avec le service de noms RPC

Les services RPC peuvent publier leurs identificateurs dans un espace de noms à l’aide des API RpcNs (RPC Name Service). Les API RpcNs dans Windows 2000 publient les entrées RPC dans Active Directory Domain Services. Les services créent des liaisons RPC et les publient dans l’espace de noms en tant qu’entrées de serveur RPC nommées avec des attributs, y compris l’ID d’interface unique, un GUID qui est reconnu par les clients. Un client peut ensuite rechercher les serveurs RPC qui offrent l’interface souhaitée, importer la liaison et se connecter au serveur.

Pour plus d’informations sur la publication d’un service RPC, consultez [liaison côté serveur](/windows/desktop/Rpc/server-side-binding).

 

 