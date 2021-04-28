---
description: Services Bureau à distance (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Services Bureau à distance (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725844d49f465c3c79dbc19fd01ec0f18b09759e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116117"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Services Bureau à distance (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)

## <a name="affected-platforms"></a>Plateformes affectées

**Serveurs** – windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>Description

Services Bureau à distance (anciennement services Terminal Server) permet à plusieurs utilisateurs simultanés d’accéder à Windows Server afin de fournir des services d’hébergement d’applications et de données à l’aide de la technologie Microsoft « Presentation Virtualization ».

Alors que la plupart des applications 32 bits et 64 bits s’exécutent comme sur Windows Services Bureau à distance, plusieurs autres ne fonctionnent pas comme prévu en raison de la différence dans la plateforme (environnement multi-utilisateur, accès simultané par plusieurs utilisateurs, etc.).

Pour plus d’informations sur la qualité des applications, consultez le livre blanc *sur la préparation des applications pour les services Terminal Server* . Pour en savoir plus sur Services Bureau à distance, consultez la page Services Bureau à distance Product et les sites Web TS TechNet. Pour en savoir plus sur le développement d’applications pour Services Bureau à distance, consultez les *instructions de programmation des services Terminal Server*. (Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.)

## <a name="manifestation-of-impacts-and-their-mitigations"></a>La manifestation des impacts et leurs atténuations

Trois modifications apportées à Windows 7 affectent les applications sur Services Bureau à distance :

-   Windows Server 2008 R2 est 64 bits uniquement
-   Virtualisation IP par session
-   Déploiements basés sur MSI – clés spécifiques à l’utilisateur

**64 bits uniquement Windows Server 2008 R2**

Les applications écrites pour le serveur 32 bits s’exécuteront en mode WoW et non en mode natif sur Windows Server 2008 R2 ou, par conséquent, sur Services Bureau à distance. Pour plus d’informations, consultez la rubrique Windows 7 64 bits uniquement.

*Atténuations pour Windows Server 2008 uniquement 64 bits*

La plupart des applications écrites pour 32 bits continuent de fonctionner normalement en mode WoW. Toutes les nouvelles applications écrites pour Windows 7 Services Bureau à distance doivent être développées et testées pour le déploiement sur les plateformes 64 bits.

**Virtualisation IP**

Virtualisation IP des services Bureau à distance permet à l’utilisateur d’attribuer des adresses IP à des connexions Bureau à distance par session ou par programme :

-   Si vous attribuez des adresses IP par session, toutes les applications utilisent l’adresse IP de la session.
-   Si vous attribuez des adresses IP par programme, seules les applications spécifiées utiliseront l’adresse IP de session et les applications restantes de la session ne seront pas affectées.
-   Si vous attribuez des adresses IP à plusieurs programmes, elles partagent une adresse IP de session.
-   Si vous avez plusieurs cartes réseau sur l’ordinateur, vous devez également en choisir une pour Virtualisation IP des services Bureau à distance.

*Solutions de contournement pour la virtualisation IP*

Certains programmes requièrent une adresse IP unique pour chaque instance de l’application. Avant Windows Server 2008 R2, chaque session sur un serveur de bureau à distance partageait la même adresse IP, provoquant des problèmes de compatibilité pour ces applications. Virtualisation IP des services Bureau à distance permet à ces applications de s’exécuter sur un serveur Bureau à distance.

**Déploiements basés sur MSI**

La compatibilité des services Bureau à distance de Microsoft est une nouvelle fonctionnalité incluse dans Services Bureau à distance dans Windows Server 2008 R2. Avec Services Bureau à distance dans Windows Server 2008 R2, les installations d’applications par utilisateur sont mises en file d’attente par le serveur Bureau à distance, puis gérées par le programme d’installation de Microsoft.

Dans Windows Server 2008 R2, vous pouvez installer un programme sur le serveur Bureau à distance de la même façon que vous installez le programme sur un bureau local. Toutefois, veillez à installer le programme pour tous les utilisateurs et à installer tous les composants du programme localement sur le serveur de Bureau à distance.

*Solutions de contournement pour les déploiements basés sur MSI*

Avant la version Windows Server 2008 R2 de Services Bureau à distance, Windows ne prenait en charge qu’une seule installation Windows Installer à la fois. Pour les applications nécessitant des configurations par utilisateur, telles que Microsoft Office Word, un administrateur qui devait préinstaller l’application, et les développeurs d’applications devaient tester ces applications à la fois sur le client Bureau à distance et l’hôte de session Bureau à distance. Windows Installer fonctionnalité de compatibilité RDS permet d’identifier et d’installer des configurations par utilisateur manquantes simultanément pour plusieurs utilisateurs et de rendre l’installation de l’application sur Bureau à distance serveur similaire à celle sur un bureau local.

**Windows Server 2008 R2 avec le rôle [services Bureau à distance](../termserv/terminal-services-portal.md) activé :** Non pris en charge. L’installation de plusieurs packages à l’aide de la [table MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) échoue si le rôle [services Bureau à distance](../termserv/terminal-services-portal.md) est activé.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Instructions de programmation des services Terminal Server](../termserv/terminal-services-programming-guidelines.md)
-   [Page d’hébergement du produit des services Terminal Server](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Livre blanc sur la préparation des applications pour les services Terminal Server](/collaborate/connect-redirect)

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.

 

 

 
