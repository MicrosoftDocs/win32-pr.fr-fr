---
description: Contrôle de version du système d’exploitation
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Contrôle de version du système d’exploitation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b8c60994eaee7a3becfa9acc03fe2c61fb12
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088037"
---
# <a name="operating-system-versioning"></a>Contrôle de version du système d’exploitation

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**Serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -haute  
**Fréquence** -élevée  









## <a name="description"></a>Description

Le numéro de version interne de Windows 7 et de Windows Server 2008 R2 est 6,1. La fonction GetVersion retourne maintenant ce numéro de version aux applications lorsqu’elles sont interrogées. Ceci est particulièrement important pour les AntiVirus, les sauvegardes, les applications utilitaires et la protection contre la copie.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

La description de cette modification est spécifique à l’application. Cela signifie que toute application qui recherche spécifiquement la version du système d’exploitation obtiendra un numéro de version plus élevé, ce qui peut entraîner une ou plusieurs des situations suivantes :

-   Les programmes d’installation d’application ne peuvent pas installer l’application, et les applications peuvent ne pas pouvoir démarrer
-   Les applications peuvent devenir instables ou se bloquer
-   Les applications peuvent générer des messages d’erreur, mais continuer à fonctionner correctement

## <a name="mitigation"></a>Limitation des risques

La plupart des applications fonctionneront correctement sur Windows 7 et Windows Server 2008 R2, car la compatibilité des applications dans Windows 7 et Windows Server 2008 R2 est très élevée. Toutefois, Windows 7 et Windows Server 2008 R2 incluent une vue de compatibilité pour les programmes d’installation et les applications qui vérifient la version du système d’exploitation.

Pour activer l’affichage de compatibilité, les utilisateurs peuvent cliquer avec le bouton droit sur le raccourci ou le fichier exécutable, puis appliquer l’affichage de compatibilité Windows XP SP2 ou Windows Vista à partir de l’onglet compatibilité. Dans la plupart des cas, cela doit permettre à l’application de fonctionner correctement sans avoir à modifier l’application.

Les professionnels de l’informatique peuvent également appliquer l’un des correctifs de compatibilité VersionLie applicables, à l’aide de l’outil d’administration de la compatibilité, qui est installé avec Application Compatibility Toolkit (ACT). Par exemple, si une application ne fonctionne pas parce qu’elle recherche, mais ne trouve pas, les informations de version de Windows XP® avec Service Pack 2 (SP2), le WinXPSP2VersionLie peut être appliqué pour retourner les informations de numéro de version appropriées à l’application, quelle que soit la version du système d’exploitation en cours d’exécution sur l’ordinateur. Les correctifs de compatibilité VersionLie disponibles sont les suivants :

-   Win95VersionLie
-   Win98VersionLie
-   WinNT4SP5VersionLie
-   Win2000VersionLie
-   Win2000SP1VersionLie
-   Win2000SP2VersionLie
-   Win2000SP3VersionLie
-   WinXPVersionLie
-   WinXPSP1VersionLie
-   WinXPSP2VersionLie
-   VistaRTMVersionLie
-   VistaSP1VersionLie
-   VistaSP2VersionLie
-   Win2K3RTMVersionLie
-   Win2K3SP1VersionLie

## <a name="solution"></a>Solution

En règle générale, les applications ne doivent pas effectuer de vérifications de version du système d’exploitation. Si une application a besoin d’une fonctionnalité spécifique, il est préférable d’essayer de la trouver et d’échouer uniquement si la fonctionnalité nécessaire est manquante. Au minimum, les applications doivent toujours accepter les numéros de version supérieurs ou égaux à la version la plus ancienne prise en charge du système d’exploitation. Les exceptions doivent se produire uniquement si une exigence légale, commerciale ou de composant système spécifique est requise.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Téléchargement de l’outil Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Correctifs de compatibilité connus, modes de compatibilité et messages AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
