---
title: Publication avec le service de noms RPC
description: Les services RPC peuvent publier leurs identificateurs dans un espace de noms à l’aide des API RpcNs (RPC Name Service).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Publication avec la publicité service de noms RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd53922bd4ce952c18c58d1b71cb485887bdc0fd020f4113679eb114b32b6f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025367"
---
# <a name="publishing-with-the-rpc-name-service"></a>Publication avec le service de noms RPC

Les services RPC peuvent publier leurs identificateurs dans un espace de noms à l’aide des API RpcNs (RPC Name Service). les api RpcNs dans Windows 2000 publient les entrées RPC dans Active Directory Domain Services. Les services créent des liaisons RPC et les publient dans l’espace de noms en tant qu’entrées de serveur RPC nommées avec des attributs, y compris l’ID d’interface unique, un GUID qui est reconnu par les clients. Un client peut ensuite rechercher les serveurs RPC qui offrent l’interface souhaitée, importer la liaison et se connecter au serveur.

Pour plus d’informations sur la publication d’un service RPC, consultez [liaison côté serveur](/windows/desktop/Rpc/server-side-binding).

 

 