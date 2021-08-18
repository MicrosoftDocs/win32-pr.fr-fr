---
description: Protection des ressources Windows supplémentaires sur les clés de registre
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Protection des ressources Windows supplémentaires sur les clés de registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3ea823b2075905b8f22cbc02539f058c9ad8f2ed33ed51d712cd8cb43f59d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995019"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Protection des ressources Windows supplémentaires sur les clés de registre

## <a name="platform"></a>Plateforme

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -moyenne  
**Fréquence** -faible  


## <a name="description"></a>Description

des ressources système supplémentaires ont ajouté des paramètres Protection des ressources Windows (WRP) dans Windows 7, ce qui les rend accessibles en lecture seule. La grande majorité des ressources qui ont reçu une protection supplémentaire sont des clés de serveur COM système, bien que certaines fonctionnalités aient ajouté une protection des ressources ciblée. Microsoft a modifié ces ressources afin de protéger le système et d’autres applications contre les interruptions et de fournir une plateforme cohérente et stable sur laquelle les applications peuvent s’exécuter de manière fiable. Dans le passé, les applications pouvaient fournir des fichiers personnalisés et utiliser l’inscription COM non protégée pour modifier le système. Dans le cas d’applications plus anciennes, cela peut rétrograder les runtimes du système ou modifier l’interface sur laquelle les autres applications devaient fonctionner correctement. Dans le pire des cas, ces installations peuvent entraîner des défaillances ou une dégradation du système au fil du temps. Pour offrir une meilleure expérience et une plate-forme d’application plus stable, nous avons verrouillé ces inscriptions afin que seules les mises à jour Microsoft puissent modifier les composants système.

Étant donné que la plupart des ressources modifiées sont des clés COM utilisées par le système, cette modification n’affecte pas la majorité des applications. bien que nous pensons que la plupart des applications ont une meilleure expérience sur Windows 7 suite à ces modifications, un petit sous-ensemble d’applications peut être affecté. Les couches de compatibilité des applications du système résolvent automatiquement les problèmes d’installation en indiquant toujours à l’application qu’elle a réussi à modifier un paramètre, même si elle a échoué en raison d’une ressource protégée. Cela empêche les configurations d’applications de s’arrêter, mais peut entraîner des problèmes si le paramètre devait être modifié pour que l’application fonctionne correctement.

## <a name="manifestation"></a>Manifestation

les Applications ont peut-être modifié ces paramètres avant le Windows 7. lors de l’installation de sur Windows 7, certaines fonctionnalités peuvent ne plus fonctionner, car les paramètres ne reflètent pas ce que l’application attendait.

Il existe deux scénarios dans lesquels les applications peuvent rencontrer des problèmes liés à cette protection supplémentaire :

-   Applications qui utilisaient peut-être des paramètres protégés en tant que magasin de données ou comme un point d’extensibilité rare ou non ATTENDU
-   Dans de rares cas, le mécanisme de détection utilisé pour identifier les configurations d’applications peut ne pas reconnaître une configuration particulière et la couche d’atténuation de la compatibilité des applications ne peut donc pas être appliquée.

## <a name="mitigation"></a>Limitation des risques

Le principal moyen d’atténuation est la couche de compatibilité des applications du système, qui est appliquée automatiquement aux configurations d’applications lorsqu’elles sont détectées. Vous pouvez également l’appliquer manuellement à n’importe quelle application à l’aide de l’onglet compatibilité dans les propriétés de l’application.

Cette couche résout le problème en interceptant les opérations du Registre. Dans le cas où l’application essayait de modifier un paramètre en lecture seule (WRP), la couche retourne toujours Success, même si le paramètre n’a pas été vraiment modifié. Pour la plupart des applications, cela ne pose aucun problème. Toutefois, il est possible que l’application ait besoin de ce paramètre modifié pour fonctionner correctement, qui est le premier scénario décrit ci-dessus.

## <a name="solution"></a>Solution

Pour les deux scénarios identifiés ci-dessus :

-   Si l’application requiert que la clé soit accessible en écriture pour fonctionner ou utiliser le magasin de données, il n’existe aucune solution autre que la modification de l’application afin qu’elle n’écrit plus à cet emplacement.
-   Si la couche de compatibilité n’a pas été appliquée à une installation, l’échec du programme d’installation doit être détecté et proposé pour être appliqué et réexécuté. Les applications peuvent également s’exécuter en mode de compatibilité, auquel cas la couche d’atténuation est toujours appliquée.

## <a name="compatibility-tests"></a>Tests de compatibilité

Comment détecter si un programme d’atténuation de WRP est appliqué à une application :

-   Windows Le programme d’installation prend en charge WRP ; elle ignore automatiquement et silencieusement les tentatives d’écriture ou de modification d’une ressource protégée. si l’application a été installée avec Windows Installer et que la journalisation a été activée, un avertissement est consigné pour chaque opération d’écriture de clé de registre ignorée en raison de sa ressource protégée par WRP.
-   L’API WRP intègre SfCIsKeyProtected, qui peut demander si une clé de Registre est protégée par WRP sur le système actuel. Pour plus d’informations sur l’utilisation de cette API, consultez l’entrée WRP sur MSDN dans les liens ci-dessous.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

<dl>

[Windows Protection des ressources](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
