---
title: Comment sécuriser mon serveur RPC maintenant
description: L’utilisation de la sécurité décrite dans cette section, fournie ailleurs dans le kit de développement logiciel (SDK) RPC et généralement acceptée comme des pratiques de sécurité appropriées, aboutit à un serveur qui est très sécurisé. Ces serveurs sont protégés contre les attaques par pénétration ou les violations de confidentialité.
ms.assetid: 528ff35c-f37c-43d8-8cc1-dbc36a9a826c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34279e4fb8899db6b7e980a0e868e91c6edb8166
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940015"
---
# <a name="how-secure-is-my-rpc-server-now"></a>Quelle est la sécurité de mon serveur RPC maintenant ?

L’utilisation de la sécurité décrite dans cette section, fournie ailleurs dans le kit de développement logiciel (SDK) RPC et généralement acceptée comme des pratiques de sécurité appropriées, aboutit à un serveur qui est très sécurisé. Ces serveurs sont protégés contre les attaques par pénétration ou les violations de confidentialité.

Si l’État est conservé entre les appels RPC, assurez-vous qu’un client unique n’entraîne pas l’allocation de ressources excessives, ce qui pourrait potentiellement refuser le service à d’autres clients.

 

 




