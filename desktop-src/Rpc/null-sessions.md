---
title: Sessions null
description: Parfois, un appel arrivant sur la session NULL peut apparaître comme un appel authentifié.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462415"
---
# <a name="null-sessions"></a>Sessions null

Parfois, un appel arrivant sur la session NULL peut apparaître comme un appel authentifié. Plus précisément, l’appel de la fonction [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) retourne le niveau d’authentification et le fournisseur de sécurité utilisés pour l’appel. Cette opération ne signifie pas que l’appel n’était pas sur une session NULL. Les deux problèmes sont orthogonals. Sur Microsoft Windows 2000, un appel de procédure distante peut tenter d’emprunter l’identité d’un appelant et vérifier les autorisations après l’emprunt d’identité. Sur Microsoft Windows XP, il est plus rapide d’appeler la fonction [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) et de vérifier l’indicateur **NullSession** .

Il existe une autre différence pertinente entre Windows 2000 et Windows XP. Si seul l’indicateur RPC uniquement si l’option \_ \_ autoriser les \_ sécurisés \_ est spécifié, les appels sur la session NULL sont effectués dans Windows 2000. Dans Windows XP, avec le renforcement général des paramètres de sécurité par défaut, lorsque cet indicateur est spécifié, les appels sur la session NULL sont rejetés avec l’accès refusé. Toutefois, même avec l' \_ indicateur RPC if \_ allow \_ Secure \_ only, RPC ne garantit pas le niveau de privilège de l’utilisateur appelant. Toutes les vérifications RPC sont que l’utilisateur dispose d’informations d’identification valides. Il est possible que l’utilisateur appelant utilise le compte invité ou d’autres comptes à faibles privilèges. Assurez-vous que le serveur n’assume pas un privilège élevé une fois RPC \_ si l' \_ autorisation \_ sécurisée \_ uniquement est utilisée.

 

 




