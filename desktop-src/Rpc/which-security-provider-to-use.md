---
title: Le fournisseur de sécurité à utiliser
description: Tous les autres éléments sont égaux, utilisez RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b89bdb10eb95952183b2a992fd12a668e79b0716f3c453f597d2241323c4ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010447"
---
# <a name="which-security-provider-to-use"></a>Le fournisseur de sécurité à utiliser

Tous les autres éléments sont égaux, utilisez RPC \_ c \_ Authn \_ GSS \_ Kerberos ou RPC \_ c \_ Authn \_ GSS \_ Negotiate. Chaque offre le service le plus évolutif et le plus sécurisé. Si vous utilisez RPC \_ C \_ Authn \_ GSS \_ Negotiate sur le serveur, les clients de niveau supérieur, tels que les clients NTLM, peuvent se connecter à votre serveur. Si ce n’est pas souhaitable, limitez le choix à RPC \_ C \_ Authn \_ GSS \_ Kerberos uniquement, ou appelez [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) pour déterminer le fournisseur de sécurité utilisé par le client et refuser l’accès aux clients à l’aide de NTLM. La méthode recommandée pour déterminer quel fournisseur de sécurité est utilisé par le client est la fonction [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .

 

 




