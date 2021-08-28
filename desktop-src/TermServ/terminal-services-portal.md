---
title: Services Bureau à distance (Services Bureau à distance)
description: Bureau à distance Microsoft Services est un logiciel d’accès aux ordinateurs distants qui prend en charge l’accès Bureau à distance. Services Bureau à distance connecte plusieurs clients à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance
- Services Bureau à distance Services Bureau à distance, page d’hébergement
- Services Terminal Server voir Services Bureau à distance Services Bureau à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525f62433c10c8c4f750a8ae1abbfa9496f2f096139c182a677c9dbf69ce4a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999899"
---
# <a name="remote-desktop-services-remote-desktop-services"></a>Services Bureau à distance (Services Bureau à distance)

## <a name="purpose"></a>Objectif

Windows Server 2012 R2, Windows Server 2012, Windows server 2008 R2 ou Windows server 2008 avec Services Bureau à distance (anciennement appelé Terminal Services) permettent à un serveur d’héberger plusieurs sessions clientes simultanées. Bureau à distance utilise la technologie Services Bureau à distance pour permettre l’exécution à distance d’une seule session. Un utilisateur peut se connecter à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) (anciennement appelé serveur Terminal Server) à l’aide du logiciel client Connexion Bureau à distance (RDC). Le Connexion Bureau à distance par le Web étend la technologie Services Bureau à distance au Web.

> [!Note]  
> Cette rubrique est destinée aux développeurs de logiciels. Si vous recherchez des informations sur l’utilisateur pour les connexions Bureau à distance, consultez [Connexion Bureau à distance : Forum aux questions](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).

 

## <a name="where-applicable"></a>Le cas échéant

Un client Connexion Bureau à distance (RDC) peut exister sous différentes formes. les périphériques matériels clients légers qui exécutent un système d’exploitation Windows incorporé peuvent exécuter le logiciel client RDC pour se connecter à un serveur hôte de Session bureau à distance. les ordinateurs Windows, Macintosh ou UNIX peuvent exécuter le logiciel client RDC pour se connecter à un serveur hôte de Session bureau à distance pour afficher des applications basées sur Windows. cette combinaison de clients RDC permet d’accéder aux applications basées sur des Windows à partir de pratiquement n’importe quel système d’exploitation.

## <a name="developer-audience"></a>Développeurs concernés

les développeurs qui utilisent Services Bureau à distance doivent être familiarisés avec les langages de programmation C et C++ et dans l’environnement de programmation basé sur Windows. Vous devez vous familiariser avec l’architecture client/serveur. Le Connexion Bureau à distance par le Web comprend des interfaces scriptables pour créer et déployer des canaux virtuels scriptables dans des applications Web Services Bureau à distance.

## <a name="run-time-requirements"></a>Conditions d’exécution

les Applications qui utilisent Services Bureau à distance requièrent Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 ou Windows Vista. Pour utiliser Connexion Bureau à distance par le Web fonctionnalité, l’application cliente Services Bureau à distance nécessite Internet Explorer et une connexion à la World Wide Web. Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[contrôle de ActiveX Bureau à distance](remote-desktop-activex-control.md)
</dt> <dd>

décrit comment utiliser le contrôle Bureau à distance ActiveX.

</dd> <dt>

[API du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-desktop-protocols.md)
</dt> <dd>

Vous utilisez l’API du fournisseur protocole RDP (Remote Desktop Protocol) pour créer un protocole pour assurer la communication entre le service Services Bureau à distance et plusieurs clients.

</dd> <dt>

[Services Bureau à distance des canaux virtuels](terminal-services-virtual-channels.md)
</dt> <dd>

Les *canaux virtuels* sont des extensions logicielles qui peuvent être utilisées pour ajouter des améliorations fonctionnelles à une application services Bureau à distance.

</dd> <dt>

[RemoteFX API de redirection de média](remotefx-api.md)
</dt> <dd>

l’API de redirection de média RemoteFX est utilisée dans une session Bureau à distance pour identifier les zones du serveur qui affichent du contenu à variation rapide, tel qu’une vidéo. Ce contenu peut ensuite être encodé en vidéo et envoyé au client dans un format encodé.

</dd> <dt>

[API du client Connexion Bureau à distance Broker](connection-broker-client-api.md)
</dt> <dd>

Décrit comment utiliser l’API cliente Connexion Bureau à distance Broker.

</dd> <dt>

[Informations de référence sur l’API agent des tâches du bureau personnel](task-agent-api-reference.md)
</dt> <dd>

L’API agent de tâche de bureau personnel est utilisée pour gérer les mises à jour planifiées d’un bureau virtuel personnel.

</dd> <dt>

[À propos de Services Bureau à distance](about-terminal-services.md)
</dt> <dd>

Services Bureau à distance (anciennement services Terminal Server) offre des fonctionnalités similaires à celles d’un environnement de type terminal, d’un ordinateur hôte centralisé ou d’un macroordinateur dans lequel plusieurs terminaux se connectent à un ordinateur hôte.

</dd> <dt>

[Fournisseur de services de gestion Bureau à distance](rdms-api-reference.md)
</dt> <dd>

Le fournisseur Bureau à distance Management Services (RDMS) gère les environnements VDI (Virtual Desktop Infrastructure).

</dd> <dt>

[Référence Services Bureau à distance](terminal-services-reference.md)
</dt> <dd>

Documentation des méthodes de propriété que vous pouvez utiliser pour examiner et configurer Services Bureau à distance propriétés de l’utilisateur. Services Bureau à distance les fonctions, structures et Connexion Bureau à distance par le Web les interfaces scriptables sont également documentées.

</dd> <dt>

[Touches de raccourci Services Bureau à distance](terminal-services-shortcut-keys.md)
</dt> <dd>

Liste des touches de raccourci de Services Bureau à distance.

</dd> <dt>

[Fournisseur WMI Services Bureau à distance](terminal-services-wmi-provider.md)
</dt> <dd>

Le fournisseur WMI Services Bureau à distance fournit un accès par programmation aux informations et aux paramètres qui sont exposés par le composant logiciel enfichable MMC (Microsoft Management Console) configuration/connections Services Bureau à distance.

</dd> <dt>

[Utilisation de Services Bureau à distance](using-terminal-services.md)
</dt> <dd>

Comment programmer dans l’environnement Services Bureau à distance et comment étendre la technologie Services Bureau à distance (anciennement appelée services Terminal Server) au Web à l’aide de Connexion Bureau à distance par le Web.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Les services Terminal Server sont désormais Services Bureau à distance](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




