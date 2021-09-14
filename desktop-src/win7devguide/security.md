---
title: sécurité (Guide du développeur Windows 7)
description: Windows 7 comprend des fonctionnalités de sécurité nouvelles et améliorées qui permettent aux développeurs d’améliorer, d’utiliser et de gérer plus facilement la sécurité de leurs applications.
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a3b317f2fe0c7d42559245108bae6a5dbf0e6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234821"
---
# <a name="security-windows-7-developer-guide"></a>sécurité (Guide du développeur Windows 7)

Windows 7 comprend des fonctionnalités de sécurité nouvelles et améliorées qui permettent aux développeurs d’améliorer, d’utiliser et de gérer plus facilement la sécurité de leurs applications. Il s’accompagne d’une variété de nouvelles fonctionnalités de sécurité qui vous permettent non seulement de vous protéger contre les menaces, mais également de limiter les dommages que les attaquants peuvent faire s’ils accèdent à un ordinateur.

les améliorations apportées à la plate-forme de filtrage Windows permettent aux développeurs de créer des applications qui interagissent avec le traitement des paquets dans la pile de mise en réseau du système d’exploitation. Les données de réseau peuvent être filtrées et peuvent également être modifiées avant qu'elles atteignent leur destination.

en outre, en raison des modifications apportées au modèle de privilège Windows, la sécurité du système est plus gérable par les développeurs et leurs utilisateurs finaux. Les nouvelles améliorations permettent d’identifier facilement les invites critiques afin de s’assurer que les utilisateurs peuvent accéder aux applications et aux fonctionnalités dont ils ont besoin sans compromettre leurs systèmes. (Voir [MSDN Security Developer Center](https://msdn.microsoft.com/security/default.aspx).)

## <a name="windows-filtering-platform"></a>Plateforme de filtrage Windows

dans Windows 7, la plateforme de filtrage des Windows a été améliorée pour permettre aux développeurs de mieux contrôler les fonctionnalités du pare-feu. Le niveau de filtrage a été augmenté et les *éditeurs de logiciels indépendants* peuvent désormais intégrer une protection et une détection personnalisées à des niveaux inférieurs. en outre, les développeurs de pare-feu peuvent activer ou désactiver des parties du pare-feu Windows.

à l’aide de la plateforme de filtrage Windows, les développeurs peuvent créer des pare-feu, des systèmes de détection d’intrusion, des antivirus, des outils d’analyse réseau et des contrôles de contrôle parental dans leurs applications. Windows La plateforme de filtrage s’intègre à et assure la prise en charge d’un large éventail de fonctionnalités de pare-feu, notamment la communication authentifiée et la configuration de pare-feu dynamique basée sur l’utilisation par les applications de l’API de Sockets (stratégie basée sur les applications). Windows La plateforme de filtrage fournit également une infrastructure pour la gestion des stratégies, les notifications de modifications, les diagnostics réseau et le filtrage avec état.

l’architecture initiale de Windows plate-forme de filtrage dans Windows Vista offrait des fonctionnalités pour le trafic basé sur IP. D’autres protocoles non-IP, tels que le protocole ARP (Address Resolution Protocol) et *Mac*(Media Access Control), pour la gestion et l’authentification réseau, nécessitent également un filtrage, une inspection ou une journalisation. dans Windows 7, une couche d’inspection *NDIS* qui prend en charge le filtrage *MAC* et *ETHERNET* a été fournie pour répondre à ce besoin. (voir [Windows la plateforme de filtrage](../fwp/windows-filtering-platform-start-page.md).)

## <a name="user-account-control"></a>Contrôle de compte d'utilisateur

le contrôle de compte d’utilisateur (UAC) est un composant de sécurité de Windows 7 qui permet aux développeurs de créer des applications qui permettent aux utilisateurs d’effectuer des tâches courantes en tant que non-administrateurs. Les développeurs peuvent réduire les risques de sécurité en exécutant des applications sous un jeton d’utilisateur standard, ce qui réduit les risques d’erreurs ou d’attaques.

Les comptes d’utilisateurs qui sont membres du groupe *administrateurs* local exécutent la plupart des applications en tant qu’utilisateur standard. En séparant les fonctions utilisateur et administrateur tout en activant la productivité, le contrôle de compte d’utilisateur permet aux développeurs de mieux contrôler le niveau d’accès dont disposent les utilisateurs sur les zones protégées d’une application. Le contrôle de compte d’utilisateur demande des informations d’identification en mode *Bureau sécurisé* , où la totalité de l’écran est protégée pour empêcher l’usurpation de l’interface utilisateur ou de la souris. (Consultez [mises à jour de la boîte de dialogue contrôle de compte d’utilisateur](../win7appqual/user-interface---user-account-control-dialog-updates.md) et [contrôle de compte d’utilisateur et WMI](../wmisdk/user-account-control-and-wmi.md).)

 

 
