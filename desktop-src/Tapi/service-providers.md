---
description: Les fournisseurs de services implémentent des contrôles d’appareil téléphoniques détaillés. Un fournisseur de services de téléphonie (TSP) fournit des contrôles d’appel et un fournisseur de services de média, s’il existe, permet de contrôler le flux multimédia.
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: Fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424c11d5b99af7440835e8822a5631e1b36f48cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414672"
---
# <a name="service-providers"></a>Fournisseurs de services

Les fournisseurs de services implémentent des contrôles d’appareil téléphoniques détaillés. Un fournisseur de services de téléphonie (TSP) fournit des contrôles d’appel et un fournisseur de services de média, s’il existe, permet de contrôler le flux multimédia.

Tous les fournisseurs de services de téléphonie s’exécutent dans le processus TAPISRV. Les fournisseurs de services peuvent créer des threads dans le contexte TAPISRV en fonction des besoins pour effectuer leur travail et être assuré qu’aucune des ressources qu’ils créent ne seront détruites par la sortie de toute application individuelle. Le serveur TAPI traduit les commandes d’application en fonction des besoins en un ensemble cohérent de commandes appelé TSPI (Telephony Service Provider Interface).

Les fournisseurs de services de média s’exécutent dans l’espace de processus de l’application, ce qui permet une réponse rapide parfois requise dans les contrôles multimédias. La DLL TAPI fournit un respect cohérent de l’interface MSPI (Media Service Provider Interface).

Pour une couverture plus détaillée des fournisseurs de services, consultez [vue d’ensemble du fournisseur de services TAPI](./tapi-service-provider-overview.md).

Sous la DLL du fournisseur de services de téléphonie, le fournisseur de services peut utiliser toutes les fonctions système ou les autres composants nécessaires. Ces fonctions incluent [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) et [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol), qui fonctionnent avec des composants et des services en mode noyau conçus par des fournisseurs de matériel indépendants, ainsi que des appareils standard tels que des ports série et parallèles pour contrôler les appareils externes connectés localement. ils peuvent également accéder aux services réseau (tels que RPC, Windows sockets et canaux nommés) pour la téléphonie client/serveur.

La DLL de l’interface utilisateur du fournisseur de services de téléphonie est chargée par l’interface TAPI dans le processus d’une application qui appelle l’une des fonctions du fournisseur de services qui peut afficher une boîte de dialogue (par exemple, [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)). Le fournisseur de services peut également provoquer le chargement et l’exécution de la DLL d’interface utilisateur associée dans le processus d’une application si le fournisseur de services doit afficher l’interface utilisateur à des moments inattendus. par exemple, pour afficher la boîte de dialogue **parler/raccrocher** affichée par le pilote de modem universel (Unimodem) lorsqu’un modem de données est utilisé pour composer un appel vocal interactif à l’aide de [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) (qui n’est normalement pas considéré comme une fonction de génération d’interface utilisateur).

Le gestionnaire de requêtes de proxy est une application de téléphonie complète qui s’exécute normalement sur un serveur de téléphonie (le même serveur que celui sur lequel le fournisseur de service de téléphonie s’exécute pour les périphériques de ligne associés). Cette architecture, plutôt que l’architecture du fournisseur de services WOSA, est utilisée lorsqu’un service particulier est implémenté de manière plus appropriée dans une application que dans un pilote sur le serveur. Par exemple, les fonctions de gestion de l’agent ACD sont implémentées dans un gestionnaire de demandes de proxy plutôt que dans un fournisseur de services.

le fournisseur de services de pilote unimodem pour le contrôle de modem est disponible sur les systèmes d’exploitation Windows Server 2003, Windows XP, Windows 2000 et Windows NT. Windows La téléphonie comprend également un mappeur générique TSPI (kernel-mode Telephony Service Provider Interface), KMDDSP, qui permet aux fournisseurs de services d’être implémentés en tant que pilotes de périphérique en mode noyau.

 

 
