---
title: Protocole Kerberos V5
description: Protocole Kerberos V5
ms.assetid: a53a1edf-f374-4cbf-8050-7cde45284157
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d78c4bdc457007c04ad66163e2ebfd7f5397f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521848"
---
# <a name="kerberos-v5-protocol"></a>Protocole Kerberos V5

Le protocole d’authentification Kerberos V5 possède un identificateur de service d’authentification RPC \_ C \_ Authn \_ GSS \_ Kerberos. Le protocole Kerberos définit la manière dont les clients interagissent avec un service d’authentification réseau et est standardisé par l’IETF (Internet Engineering Task Force) en septembre 1993, dans le document [RFC 1510](https://www.ietf.org/rfc/rfc1510.txt). Les clients obtiennent des tickets du centre de distribution de clés Kerberos (KDC), et ils présentent ces tickets aux serveurs lorsque les connexions sont établies. Les tickets Kerberos représentent les informations d'identification réseau du client.

Comme NTLM, le protocole Kerberos utilise le nom de domaine, le nom d’utilisateur et le mot de passe pour représenter l’identité du client. Le ticket Kerberos initial obtenu à partir du KDC lorsque l’utilisateur ouvre une session est basé sur un hachage chiffré du mot de passe de l’utilisateur. Ce ticket initial est mis en cache. Lorsque l’utilisateur tente de se connecter à un serveur, le protocole Kerberos examine le cache de tickets pour rechercher un ticket valide pour ce serveur. Si aucun ticket n’est disponible, le ticket initial de l’utilisateur est envoyé au centre de gestion de clés (KDC), ainsi qu’une demande de ticket pour le serveur spécifié. Ce ticket de session est ajouté au cache, et il peut être utilisé pour se connecter au même serveur jusqu’à ce que le ticket expire.

Lorsqu’un serveur appelle [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) à l’aide du protocole Kerberos, le nom de domaine et le nom d’utilisateur du client sont retournés. Lorsqu’un serveur appelle [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), le jeton du client est retourné. Ces comportements sont les mêmes que lors de l’utilisation de NTLM.

Le protocole Kerberos fonctionne à travers les limites de l’ordinateur. Les ordinateurs clients et serveurs doivent tous deux se trouver dans des domaines, et ces domaines doivent avoir une relation d’approbation.

Le protocole Kerberos nécessite une authentification mutuelle et le prend en charge à distance. Le client doit spécifier le nom principal du serveur et l’identité du serveur doit correspondre exactement au nom du principal. Si le client spécifie la **valeur null** pour le nom principal du serveur ou si le nom du principal ne correspond pas au serveur, l’appel échoue.

Avec le protocole Kerberos, les niveaux d’emprunt d’identité identifient, Impersonate et Delegate peuvent être utilisés. Lorsqu’un serveur appelle [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), le jeton retourné est valide sur l’ordinateur pendant une période de temps comprise entre 5 minutes et 8 heures. Après ce délai, il ne peut être utilisé que sur l’ordinateur serveur. Si un serveur est « exécuter en tant qu’activateur » et que l’activation est effectuée avec le protocole Kerberos, le jeton du serveur expirera entre 5 minutes et 8 heures après l’activation.

Le protocole d’authentification Kerberos V5 implémenté par WindowsÂ prend en charge le [masquage](cloaking.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Packages COM et de sécurité](com-and-security-packages.md)
</dt> </dl>

 

 




