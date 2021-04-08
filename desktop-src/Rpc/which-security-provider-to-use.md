---
title: Le fournisseur de sécurité à utiliser
description: Tous les autres éléments sont égaux, utilisez RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673246"
---
# <a name="which-security-provider-to-use"></a>Le fournisseur de sécurité à utiliser

Tous les autres éléments sont égaux, utilisez RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate. Chaque offre le service le plus évolutif et le plus sécurisé. Si vous utilisez RPC \_ C \_ Authn \_ GSS \_ Negotiate sur le serveur, les clients de niveau supérieur, tels que les clients NTLM, peuvent se connecter à votre serveur. Si ce n’est pas souhaitable, limitez le choix à RPC \_ C \_ Authn \_ GSS \_ Kerberos uniquement, ou appelez [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) pour déterminer le fournisseur de sécurité utilisé par le client et refuser l’accès aux clients à l’aide de NTLM. La méthode recommandée pour déterminer quel fournisseur de sécurité est utilisé par le client est la fonction [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .

 

 




