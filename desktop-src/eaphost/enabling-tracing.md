---
title: Activation du suivi EAPHost
description: Peut aider les utilisateurs à trouver les causes racines des problèmes qui se produisent pendant le processus d’authentification EAP. Les informations de débogage peuvent inclure des appels d’API effectués, des appels de fonction internes effectués et des transitions d’État effectuées.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104032132"
---
# <a name="enabling-eaphost-tracing"></a>Activation du suivi EAPHost

Les journaux de suivi contenant des informations de débogage peuvent aider les utilisateurs à trouver les causes racines des problèmes qui se produisent pendant le processus d’authentification EAP. Les informations de débogage peuvent inclure des appels d’API effectués, des appels de fonction internes effectués et des transitions d’État effectuées.

Le suivi peut être activé côté client et côté authentificateur. Le suivi peut également être activé pour les appels aux API du [service de routage et d’accès à distance (RRAS)](/windows/desktop/RRAS/routing-start-page) . Pour plus d’informations, consultez [suivi sur le service Routage et accès distant](#tracing-on-the-routing-and-remote-access-service).

> [!Note]  
> Les journaux de suivi sont disponibles en anglais uniquement.

 

Quand le suivi EAPHost est activé, les informations de journalisation sont stockées dans un fichier. etl à un emplacement spécifié par l’utilisateur. Si des erreurs se produisent pendant l’authentification EAP, le suivi génère un fichier. etl qui peut être envoyé à Microsoft Developer Support pour l’analyse de la cause racine. Les partenaires qui ont accès aux partages de build, aux symboles et aux fichiers TraceFormat de Microsoft Windows peuvent convertir les fichiers. etl en fichier texte brut à l’aide de l’outil **Tracerpt** .

Les échecs du serveur de stratégie réseau (NPS) ne sont pas capturés dans les journaux EAPHost. Si vous essayez de résoudre un échec du serveur NPS, affichez le IASSAM. LOG et [IASNAP. Fichiers journaux](https://go.microsoft.com/fwlink/p/?linkid=84108) .

## <a name="tracing-on-the-client"></a>Suivi sur le client

Pour activer le suivi côté client :

1.  Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges.
2.  Exécutez la commande suivante : **Logman** **Start trace** **EapHostPeer** **-o** **. \\ EapHostPeer. etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ETS**
3.  Reproduisez le scénario que vous souhaitez tracer.
4.  Exécutez la commande suivante : **Logman** **Stop** **EapHostPeer** **-ETS**
5.  Convertissez le fichier ETL en texte à l’aide de la commande suivante : **Tracerpt EapHostPeer. etl** **– PDB** **&lt; PDBPATH &gt;** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**
    > [!Note]  
    > Si vous n’avez pas accès à l’outil tracerpt, évitez la dernière étape et envoyez le fichier. etl à Microsoft Developer Support.

     

## <a name="tracing-on-the-authenticator"></a>Suivi sur l’authentificateur

Pour activer le suivi côté authentificateur :

1.  Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges.
2.  Exécutez la commande suivante : **Logman** **Start trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr. etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**
3.  Reproduisez le scénario que vous souhaitez tracer.
4.  Exécutez la commande suivante : **Logman** **Stop** **EapHostAuthr** **-ETS**
5.  Convertissez le fichier ETL en texte à l’aide de la commande suivante : **Tracerpt EapHostAuthr. etl** **– PDB** **&lt; PDBPATH &gt;** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**
    > [!Note]  
    > Si vous n’avez pas accès à l’outil tracerpt, évitez la dernière étape et envoyez plutôt le fichier. etl à Microsoft Developer Support.

     

## <a name="event-tracing"></a>Suivi d’événements

Dans Windows 7 et les versions ultérieures de Windows, EapHost fournit un suivi basé sur les événements sur l’authentificateur et l’homologue. L’avantage du suivi basé sur les événements est qu’aucun fichier de symboles n’est nécessaire pour afficher les messages de trace. Pour activer le suivi d’événements :

1.  Ouvrez **Observateur**.
2.  Les messages EapHost critiques sont journalisés sous : « vues personnalisées \\ événements d’administration »
3.  Les messages non critiques sont journalisés sous : «applications et services \\ Microsoft \\ Windows \\ EAPHost
4.  Les messages d’événements de type « analyse » et « débogage » peuvent être affichés sous le même chemin d’accès en sélectionnant **afficher les journaux d’analyse et de débogage** dans le menu **affichage** de la barre de titre.

## <a name="tracing-on-the-routing-and-remote-access-service"></a>Suivi sur le service Routage et accès distant

Pour activer le suivi RRAS :

1.  Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges.
2.  Exécutez la commande suivante : **netsh** **RAS** **Set** **TR** **\* *_ _* fr**
3.  Ouvrir **\\ le suivi% systemroot%** pour afficher les traces RAS

Pour désactiver le suivi RRAS :

1.  Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges.
2.  Exécutez la commande suivante : **netsh** **RAS** **Set** **TR** **\* *_ _* dis**

Pour plus d’informations, consultez [commandes netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’EAPHost](using-eap-host.md)
</dt> <dt>

[Service Routage et accès à distance](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 