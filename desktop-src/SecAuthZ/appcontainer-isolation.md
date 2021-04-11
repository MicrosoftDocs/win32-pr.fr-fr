---
description: L’isolation est l’objectif principal d’un environnement d’exécution AppContainer.
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: Isolation d’AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fec44fd3d6eb9495370c42e52726ceb0f63806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204151"
---
# <a name="appcontainer-isolation"></a>Isolation d’AppContainer

L’isolation est l’objectif principal d’un environnement d’exécution AppContainer. En isolant une application des ressources inutiles et d’autres applications, les opportunités de manipulation malveillante sont réduites. L’octroi d’un accès basé sur des privilèges minimaux empêche les applications et les utilisateurs d’accéder aux ressources au-delà de leurs droits. Le contrôle de l’accès aux ressources protège le processus, l’appareil et le réseau.

La plupart des vulnérabilités dans Windows démarrent avec l’application. Parmi les exemples les plus courants, citons la séparation d’une application de son navigateur ou l’envoi d’un document incorrect à Internet Explorer, ainsi que l’exploitation de plug-ins, tels que Flash. Plus ces applications peuvent être isolées dans un AppContainer, plus la sécurité de l’appareil et des ressources est sûre. Même si une vulnérabilité dans une application est exploitée, l’application ne peut pas accéder aux ressources au-delà de ce qui est accordé à l’AppContainer. Les applications malveillantes ne peuvent pas prendre le contrôle du reste de l’ordinateur.

## <a name="credential-isolation"></a>Isolement des informations d’identification

La gestion des identités et des informations d’identification, l’AppContainer empêche l’utilisation des informations d’identification de l’utilisateur pour accéder aux ressources ou se connecter à d’autres environnements. L’environnement AppContainer crée un identificateur qui utilise les identités combinées de l’utilisateur et de l’application. Par conséquent, les informations d’identification sont propres à chaque association utilisateur/application et l’application ne peut pas emprunter l’identité de l’utilisateur.

## <a name="device-isolation"></a>Isolation des appareils

Isolation de l’application à partir des ressources de l’appareil, telles que les capteurs passifs (caméra, microphone, GPS) et les pompes à argent (3G/4G, dial phone) l’environnement AppContainer empêche l’application d’exploiter l’appareil de manière malveillante. Ces ressources sont bloquées par défaut et peuvent se voir accorder l’accès si nécessaire. Dans certains cas, ces ressources sont protégées par des « courtiers ». Certaines ressources, telles que le clavier et la souris, sont toujours disponibles pour l’AppContainer et l’application résidente.

## <a name="file-isolation"></a>Isolation des fichiers

Contrôle de l’accès aux fichiers et au registre, l’environnement AppContainer empêche l’application de modifier les fichiers qu’elle ne devrait pas. L’accès en lecture-écriture peut être accordé à des fichiers persistants et à des clés de Registre spécifiques. L’accès en lecture seule est moins restreint. Une application a toujours accès aux fichiers résidents en mémoire créés spécifiquement pour cet AppContainer.

## <a name="network-isolation"></a>Isolement réseau

L’isolation de l’application des ressources réseau au-delà de celles allouées spécifiquement, AppContainer empêche l’application de « échapper » son environnement et d’exploiter de manière malveillante les ressources réseau. Un accès granulaire peut être accordé pour l’accès à Internet, l’accès intranet et l’action en tant que serveur.

## <a name="process-isolation"></a>Isolement des processus

En sandbox les objets du noyau de l’application, l’environnement AppContainer empêche l’application d’influencer ou d’influer sur d’autres processus d’application. Cela empêche une application à relation contenant-contenu de corrompre d’autres processus en cas d’exception.

## <a name="window-isolation"></a>Isolation des fenêtres

L’isolation de l’application à partir d’autres fenêtres, l’environnement AppContainer empêche l’application d’affecter d’autres interfaces d’application.

 

 



