---
title: Utilisation de l’API de virtualisation Bureau à distance
description: Les développeurs peuvent utiliser cette API pour personnaliser la logique utilisée par le Service Broker pour les connexions Bureau à distance pour déterminer la destination optimale pour une connexion client entrante.
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance à l’aide de l’API de virtualisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9ebfc014a2c8ec20d299bbb8be9183b25ce89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217361"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>Utilisation de l’API de virtualisation Bureau à distance

Le service de rôle annuaire de sessions des services Terminal Server (annuaire de sessions TS) permet aux serveurs Terminal Server de stocker les informations d’utilisateur et de session dans une base de données appelée annuaire de sessions. Lorsqu’un utilisateur se connecte à un serveur Terminal Server dans une batterie de serveurs, l’annuaire de sessions TS détermine si l’utilisateur a déjà une session en cours d’exécution sur un serveur Terminal Server et, si tel est le cas, il redirige l’utilisateur vers ce serveur Terminal Server.

dans Windows Server 2008, le service de rôle annuaire de sessions ts a été développé et renommé Terminal Services session broker (session broker ts). Outre la maintenance d’un répertoire de sessions existantes, le service session Broker TS peut également négocier les connexions entrantes. Lorsque session Broker TS reçoit une connexion entrante d’un utilisateur, il consulte sa base de données pour déterminer si l’utilisateur a une session existante sur un serveur Terminal Server. Dans ce cas, le service session Broker TS redirige la connexion vers ce même serveur Terminal Server. Si ce n’est pas le cas, la session Broker TS détermine quel serveur Terminal Server a le moins de connexions et redirige la connexion vers ce serveur.

à compter de Windows Server 2008, Microsoft a également publié une interface de programmation d’applications (API) publique pour la surveillance et l’interaction avec les sessions sur les serveurs terminal server. Cette API est décrite dans [Connexion Bureau à distance référence du plug-in Broker](/windows/desktop/TermServ/terminal-services-virtualization-api-reference). À l’aide de cette API, les développeurs peuvent créer des plug-ins de stratégie personnalisés qui remplacent la logique de redirection standard de session Broker TS. Les plug-ins personnalisés peuvent rediriger les sessions vers les serveurs Terminal Server, ainsi que pour les machines virtuelles, les bureaux virtuels, les serveurs lames et les bureaux physiques.

dans Windows Server 2008 R2, l’architecture de Connexion Bureau à distance broker (service broker pour les connexions bureau à distance) (anciennement Session broker TS) a été étendue pour prendre en charge les connexions aux ordinateurs virtuels. La nouvelle architecture prend en charge la gestion des sessions pour les machines virtuelles via l’API de virtualisation Bureau à distance. Les développeurs peuvent utiliser cette API pour personnaliser la logique utilisée par le Service Broker pour les connexions Bureau à distance pour déterminer la destination optimale pour une connexion client entrante.

Bureau à distance API de virtualisation offre plusieurs avantages aux développeurs :

-   Les interfaces permettant de travailler avec des serveurs terminaux physiques sont similaires à celles utilisées pour travailler avec des machines virtuelles.
-   Les développeurs peuvent remplacer tout ou partie de la logique de redirection standard. Les développeurs peuvent s’appuyer sur le code fourni avec le produit et n’ont pas besoin de tout écrire à partir de zéro.
-   Aucun agent de gestion supplémentaire n’est requis sur le serveur de gestion ou dans la session.
-   les plug-ins Session Broker TS développés pour être utilisés avec Windows Server 2008 sont toujours pris en charge.
-   L’API permet également aux développeurs de créer des interfaces utilisateur pour l’administration des serveurs Bureau à distance hôte de session (hôte de session Bureau à distance) (anciennement appelés « serveurs Terminal Server ») et des machines virtuelles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur l’API de virtualisation Bureau à distance](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[Informations de référence sur le plug-in Service Broker Connexion Bureau à distance](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 