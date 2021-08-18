---
description: Contrôle de version du système d’exploitation
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Contrôle de version du système d’exploitation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707594f7e17b1518f56c0dc889911740f1bbddf50038c1908b7a47d7a0629b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994869"
---
# <a name="operating-system-versioning"></a>Contrôle de version du système d’exploitation

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -haute  
**Fréquence** -élevée  









## <a name="description"></a>Description

le numéro de version interne pour Windows 7 et Windows Server 2008 R2 est 6,1. La fonction GetVersion retourne maintenant ce numéro de version aux applications lorsqu’elles sont interrogées. Ceci est particulièrement important pour les AntiVirus, les sauvegardes, les applications utilitaires et la protection contre la copie.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

La description de cette modification est spécifique à l’application. Cela signifie que toute application qui recherche spécifiquement la version du système d’exploitation obtiendra un numéro de version plus élevé, ce qui peut entraîner une ou plusieurs des situations suivantes :

-   Les programmes d’installation d’application ne peuvent pas installer l’application, et les applications peuvent ne pas pouvoir démarrer
-   Les applications peuvent devenir instables ou se bloquer
-   Les applications peuvent générer des messages d’erreur, mais continuer à fonctionner correctement

## <a name="mitigation"></a>Limitation des risques

la plupart des applications fonctionneront correctement sur Windows 7 et Windows server 2008 r2, car la compatibilité des applications dans Windows 7 et Windows server 2008 r2 est très élevée. toutefois, Windows 7 et Windows Server 2008 R2 incluent une vue de compatibilité pour les programmes d’installation et les applications qui vérifient la version du système d’exploitation.

pour activer l’affichage de compatibilité, les utilisateurs peuvent cliquer avec le bouton droit sur le raccourci ou le fichier exécutable, puis appliquer l’affichage de compatibilité Windows XP SP2 ou Windows Vista à partir de l’onglet compatibilité. Dans la plupart des cas, cela doit permettre à l’application de fonctionner correctement sans avoir à modifier l’application.

les professionnels de l’informatique peuvent également appliquer l’un des correctifs de compatibilité VersionLie applicables, à l’aide de l’outil d’administration de la compatibilité, qui est installé avec le Shared Computer Toolkit de compatibilité des applications (ACT). par exemple, si une application ne fonctionne pas, car elle recherche, mais ne trouve pas, les informations de version de Windows XP® avec Service Pack 2 (SP2), le WinXPSP2VersionLie peut être appliqué pour retourner les informations de numéro de version appropriées à l’application, quelle que soit la version du système d’exploitation en cours d’exécution sur l’ordinateur. Les correctifs de compatibilité VersionLie disponibles sont les suivants :

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

-   [compatibilité des applications Shared Computer Toolkit téléchargement](/windows-hardware/get-started/adk-install)
-   [Correctifs de compatibilité connus, modes de compatibilité et messages AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
