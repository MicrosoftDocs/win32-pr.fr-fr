---
title: Fonctions d’autorisation (RPC)
description: Chaque fois qu’un programme serveur reçoit une demande client pour accéder à l’une des procédures distantes de gestion, la bibliothèque Runtime RPC appelle une fonction d’autorisation par défaut.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104030544"
---
# <a name="authorization-functions"></a>Fonctions d’autorisation

Chaque fois qu’un programme serveur reçoit une demande client pour accéder à l’une des procédures distantes de gestion, la bibliothèque Runtime RPC appelle une fonction d’autorisation par défaut. Cette fonction utilise le SSP pour vérifier les informations d’identification du client et autoriser ou rejeter la demande.

Votre programme serveur peut remplacer la fonction d’autorisation fournie par le fournisseur de services partagés. Appelez la fonction [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) et transmettez-la à l’adresse de votre fonction d’autorisation. Une fois que le programme serveur a défini la fonction d’autorisation, la bibliothèque Runtime RPC l’appelle chaque fois que le programme serveur reçoit une demande du client pour l’une des fonctions de gestion. Pour plus d’informations, consultez [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)et [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).

 

 




