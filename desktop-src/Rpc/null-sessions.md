---
title: Sessions null
description: Parfois, un appel arrivant sur la session NULL peut apparaître comme un appel authentifié.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5476a49513019fe15afa4a30beae08104533a6621a84c4e0d1de4e9f315275ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019559"
---
# <a name="null-sessions"></a>Sessions null

Parfois, un appel arrivant sur la session NULL peut apparaître comme un appel authentifié. Plus précisément, l’appel de la fonction [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) retourne le niveau d’authentification et le fournisseur de sécurité utilisés pour l’appel. Cette opération ne signifie pas que l’appel n’était pas sur une session NULL. Les deux problèmes sont orthogonals. sur Microsoft Windows 2000, un appel de procédure distante peut tenter d’emprunter l’identité d’un appelant et vérifier les autorisations après l’emprunt d’identité. sur Microsoft Windows XP, il est plus rapide d’appeler la fonction [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) et de vérifier l’indicateur **NullSession** .

il existe une autre différence pertinente entre Windows 2000 et Windows XP. si seul l’indicateur RPC uniquement si l’option autoriser les communications \_ \_ \_ sécurisées \_ est spécifié, les appels sur la session null passent par Windows 2000. dans Windows XP, avec le renforcement général des paramètres de sécurité par défaut, lorsque cet indicateur est spécifié, les appels sur la session null sont rejetés avec l’accès refusé. Toutefois, même avec l' \_ indicateur RPC if \_ allow \_ Secure \_ only, RPC ne garantit pas le niveau de privilège de l’utilisateur appelant. Toutes les vérifications RPC sont que l’utilisateur dispose d’informations d’identification valides. Il est possible que l’utilisateur appelant utilise le compte invité ou d’autres comptes à faibles privilèges. Assurez-vous que le serveur n’assume pas un privilège élevé une fois RPC \_ si l' \_ autorisation \_ sécurisée \_ uniquement est utilisée.

 

 




