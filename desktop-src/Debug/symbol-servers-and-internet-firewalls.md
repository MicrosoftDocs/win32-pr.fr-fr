---
description: Certains systèmes utilisent des pare-feu Internet ou des serveurs proxy qui nécessitent une authentification pour tout le trafic Internet.
ms.assetid: b79e9a6f-2ffb-4ec0-ac2d-63e79ecfc26c
title: Serveur de symboles et pare-feu Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2a85a5d0ee2d41e6ffee40bbb275155bdf1e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523068"
---
# <a name="symbol-server-and-internet-firewalls"></a>Serveur de symboles et pare-feu Internet

Certains systèmes utilisent des pare-feu Internet ou des serveurs proxy qui nécessitent une authentification pour tout le trafic Internet. Les versions antérieures du serveur de symboles n’ont pas pu accéder aux symboles à partir d’Internet, sauf si le système a utilisé un client de pare-feu qui gérait l’authentification en toute transparence.

À compter de dbghelp 6,1, le serveur de symboles prend en charge les serveurs proxy qui nécessitent une telle authentification. Le serveur de symboles utilise le serveur qui est configuré par défaut dans les paramètres réseau de l’ordinateur. Pour ce faire, ouvrez l’élément **Options Internet** dans le panneau de configuration, cliquez sur l’onglet **connexions** , puis sur **paramètres réseau**. Vous pouvez également effectuer cette opération à partir d’Internet Explorer en cliquant sur **Options Internet** dans le menu **Outils** . Le serveur de symboles a été testé sur de nombreuses marques de serveurs proxy à l’aide des méthodes de base et de stimulation/réponse de l’authentification.

Pour définir un serveur proxy spécifique pour l’utilisation du serveur de symboles, définissez la \_ \_ variable d’environnement proxy de symboles NT \_ sur le nom (ou l’adresse IP) du serveur proxy, suivi du numéro de port. Séparez les deux valeurs par un signe deux-points. Par exemple :

**définir \_ \_Proxy de symboles NT \_ =**_myProxyServer_*_: 80_*

Lorsque vous utilisez le débogueur WinDbg, configurez votre chemin d’accès aux symboles pour qu’il pointe vers le magasin de symboles que vous souhaitez utiliser. La seule différence est que le système affiche une boîte de dialogue dans laquelle vous devez entrer votre ID d’utilisateur et votre mot de passe pour passer au serveur proxy. Si vous entrez des informations incorrectes, la boîte de dialogue s’affiche à nouveau. Si vous cliquez sur le bouton **Annuler** , la boîte de dialogue est fermée et le serveur de symboles est désactivé pour une utilisation via Internet.

Lorsque vous utilisez les versions les plus récentes de cdb.exe ou ntsd.exe, cette fonctionnalité est désactivée par défaut. Toutefois, vous pouvez activer ou désactiver cette fonctionnalité à l’aide de la commande d’extension ! sym comme suit :

-   Pour activer l’invite pour l’ID d’utilisateur et le mot de passe : **! les invites sym**.
-   Pour désactiver l’invite pour l’ID utilisateur et le mot de passe : **! sym invites**.

Si vous activez l’invite, vous devrez recharger les symboles à l’aide de la commande. Reload.

L’API DbgHelp a été développée pour prendre en charge ces modifications. La fonction [**SymbolServerSetOptions**](/previous-versions//ms680676(v=vs.85)) prend en charge l' \_ option de proxy SSRVOPT. Si le paramètre de données est **null**, le proxy par défaut défini dans **Options Internet** est utilisé. Dans le cas contraire, une chaîne se terminant par zéro est passée en spécifiant le nom et le numéro de port du serveur proxy. Le nom et le port sont séparés par un signe deux-points, comme suit : *myProxyServer*: 80. La fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) prend en charge l' \_ option SYMOPT no \_ invites. Cela désactive toutes les demandes de validation à partir du serveur de symboles.

 

 
