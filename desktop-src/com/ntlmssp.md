---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363596"
---
# <a name="ntlmssp"></a>NTLMSSP

NTLMSSP, dont l’identificateur de service d’authentification est RPC \_ C \_ Authn \_ WinNT, est un fournisseur de support de sécurité qui est disponible sur toutes les versions de DCOM. Elle utilise le protocole NTLM pour l’authentification. NTLM ne transmet jamais réellement le mot de passe de l’utilisateur au serveur lors de l’authentification. Par conséquent, le serveur ne peut pas utiliser le mot de passe lors de l’emprunt d’identité pour accéder aux ressources réseau auxquelles l’utilisateur a accès. Seules les ressources locales sont accessibles.

NTLM fonctionne à la fois localement et sur plusieurs ordinateurs. Autrement dit, si le client et le serveur se trouvent sur des ordinateurs différents, NTLM peut toujours s’assurer que le client est bien celui qu’il prétend être.

Avec NTLM, l’identité du client est représentée par un nom de domaine, un nom d’utilisateur et un mot de passe ou un jeton. Lorsqu’un serveur appelle [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), le nom de domaine et le nom d’utilisateur du client sont retournés. Toutefois, lorsqu’un serveur appelle [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), le jeton du client est retourné. S’il n’existe aucune relation d’approbation entre le client et le serveur et si le serveur possède un compte local avec le même nom et le même mot de passe que le client, ce compte sera utilisé pour représenter le client.

NTLM prend en charge l’authentification mutuelle inter-threads et inter-processus (localement uniquement). Si le client spécifie le nom principal du serveur sous la forme utilisateur de domaine \\ dans un appel à [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), l’identité du serveur doit correspondre à ce nom de principal, sans quoi l’appel échoue. Si le client spécifie **null**, l’identité du serveur n’est pas vérifiée.

NTLM prend également en charge le niveau d’emprunt d’identité du délégué, inter-threads et inter-processus (localement uniquement).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Packages COM et de sécurité](com-and-security-packages.md)
</dt> </dl>

 

 