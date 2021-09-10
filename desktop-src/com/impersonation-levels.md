---
title: Niveaux d’emprunt d’identité (COM)
description: Si l’emprunt d’identité s’effectue correctement, cela signifie que le client a accepté de laisser le serveur être le client dans une certaine mesure.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363400"
---
# <a name="impersonation-levels"></a>Niveaux d’emprunt d’identité

Si l’emprunt d’identité s’effectue correctement, cela signifie que le client a accepté de laisser le serveur être le client dans une certaine mesure. Les différents degrés d’emprunt d’identité sont appelés « *niveaux d’emprunt d’identité*» et indiquent la quantité d’autorité accordée au serveur lorsqu’il emprunte l’identité du client.

Actuellement, il existe quatre niveaux d’emprunt d’identité : *anonyme*, *identifier*, *emprunter l’identité* et *déléguer*. La liste suivante décrit brièvement chaque niveau d’emprunt d’identité :

<dl> <dt>

<span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>Anonyme (RPC \_ C \_ IMP \_ niveau \_ Anonymous)
</dt> <dd>

Le client est anonyme au serveur. Le processus serveur peut emprunter l'identité du client, mais le jeton d'emprunt d'identité ne contient pas d'informations sur le client. Ce niveau est pris en charge uniquement sur le transport de communication interprocessus local. Tous les autres transports promeuvent silencieusement ce niveau pour identifier.

</dd> <dt>

<span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identifier ( \_ identification du \_ niveau d’IMP RPC C \_ \_ )
</dt> <dd>

Niveau par défaut du système. Le serveur peut obtenir l'identité du client et peut emprunter l'identité du client pour vérifier des listes ACL.

</dd> <dt>

<span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>Impersonate (RPC \_ C \_ IMP \_ niveau \_ Impersonate)
</dt> <dd>

Le serveur peut emprunter l'identité du contexte de sécurité du client tout en agissant au nom du client. Le serveur peut accéder aux ressources locales sous l'identité du client. Si le serveur est local, il peut accéder aux ressources réseau en tant que client. Si le serveur est distant, il ne peut accéder qu’aux ressources qui se trouvent sur le même ordinateur que le serveur.

</dd> <dt>

<span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>délégué ( \_ délégué de \_ niveau IMP RPC c \_ \_ )
</dt> <dd>

Niveau d'emprunt d'identité le plus puissant. Quand ce niveau est sélectionné, le serveur (local ou distant) peut emprunter l’identité du contexte de sécurité du client tout en agissant au nom du client. Pendant l’emprunt d’identité, les informations d’identification du client (locales et réseau) peuvent être transmises à un nombre quelconque d’ordinateurs.

Pour que l’emprunt d’identité fonctionne au niveau du délégué, les conditions suivantes doivent être remplies :

-   Le client doit définir le niveau d’emprunt d’identité sur \_ le \_ délégué de niveau IMP RPC C \_ \_ .
-   Le compte client ne doit pas être marqué « le compte est sensible et ne peut pas être délégué » dans le service Active Directory.
-   Le compte de serveur doit être marqué avec l’attribut « approuvé pour la délégation » dans le service Active Directory.
-   Les ordinateurs qui hébergent le client, le serveur et tous les serveurs « en aval » doivent tous être en cours d’exécution dans un domaine.

</dd> </dl>

En choisissant le niveau d’emprunt d’identité, le client indique au serveur la manière dont il peut emprunter l’identité du client. Le client définit le niveau d’emprunt d’identité sur le proxy qu’il utilise pour communiquer avec le serveur.

## <a name="setting-the-impersonation-level"></a>Définition du niveau d’emprunt d’identité

Il existe deux façons de définir le niveau d’emprunt d’identité :

-   Le client peut le définir échelle, à l’aide d’un appel à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   Un client peut définir la sécurité au niveau du proxy sur une interface d’un objet distant par le biais d’un appel à [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (ou à la fonction d’assistance [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).

Vous définissez le niveau d’emprunt d’identité en passant une \_ \_ valeur de niveau d’IMP RPC appropriée \_ \_ à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) via le paramètre *dwImpLevel* .

Les différents services d’authentification prennent en charge l’emprunt d’identité au niveau du délégué sur des étendues différentes. Par exemple, NTLMSSP prend en charge l’emprunt d’identité au niveau du délégué inter-threads et interprocessus, mais pas entre les ordinateurs. En revanche, le protocole Kerberos prend en charge l’emprunt d’identité au niveau du délégué au-delà des limites de l’ordinateur, tandis que Schannel ne prend pas en charge l’emprunt d’identité au niveau du délégué. Si vous avez un proxy à un niveau d’emprunt d’identité et que vous souhaitez définir le niveau d’emprunt d’identité à déléguer, vous devez appeler [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) à l’aide des constantes par défaut pour chaque paramètre, à l’exception du niveau d’emprunt d’identité. COM choisit NTLM localement et le protocole Kerberos à distance (lorsque le protocole Kerberos fonctionne).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Délégation et emprunt d’identité](delegation-and-impersonation.md)
</dt> </dl>

 

 