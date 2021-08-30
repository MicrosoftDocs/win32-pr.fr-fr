---
title: Automatisation de l’interface utilisateur
description: Microsoft UI Automation est une infrastructure d’accessibilité qui permet à Windows applications de fournir et de consommer des informations de programmation sur les interfaces utilisateur (iu).
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55951bf103906aace627a03ab84557d6a555aa793f1e0cec7ff2c81598e71558
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071829"
---
# <a name="ui-automation"></a>Automatisation de l’interface utilisateur

Microsoft UI Automation est une infrastructure d’accessibilité qui permet à Windows applications de fournir et de consommer des informations de programmation sur les interfaces utilisateur (iu). Il fournit un accès par programme à la plupart des éléments d’interface utilisateur sur le bureau. Il permet aux produits de technologie d’assistance, tels que les lecteurs d’écran, de fournir des informations sur l’interface utilisateur aux utilisateurs finaux et de manipuler l’interface utilisateur par d’autres moyens que l’entrée standard. UI Automation permet également aux scripts de test automatisés d’interagir avec l’interface utilisateur.

-   [Le cas échéant](#where-applicable)
-   [Public destiné aux développeurs](#developer-audience)
-   [Spécifications d’exécution](#run-time-requirements)
-   [Prise en charge des systèmes d’exploitation de niveau supérieur](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a>Cas d'emploi

à l’aide d’UI Automation et des pratiques de conception accessibles suivantes, les développeurs peuvent rendre les applications qui s’exécutent sur Windows plus accessibles à de nombreuses personnes avec une vision, une audition ou un handicap moteur. En outre, UI Automation est spécifiquement conçu pour fournir des fonctionnalités robustes pour les scénarios de test automatisé.

## <a name="developer-audience"></a>Public de développeurs

UI Automation est conçu pour les développeurs C/C++ expérimentés. en général, les développeurs ont besoin d’un niveau modéré de compréhension des objets COM (component Object Model) et des interfaces, d’Unicode et de la programmation d’API Windows.

pour plus d’informations sur UI Automation pour le code managé, consultez [accessibilité](/dotnet/framework/ui-automation/) dans la section Guide du développeur .NET Framework de MSDN.

## <a name="run-time-requirements"></a>Exigences d'exécution

UI Automation est pris en charge sur les systèmes d’exploitation suivants : Windows XP, Windows server 2003, Windows server 2003 r2, Windows Vista, Windows 7, Windows 10, Windows server 2008, Windows server 2008 r2, Windows Server 2012, Windows Server 2012 r2, Windows Server 2016 et Windows server 2019.

> [!Note]  
> Windows XP et Windows Server 2003 requièrent également Microsoft .NET Framework 3,0.

 

## <a name="support-for-down-level-operating-systems"></a>Prise en charge des systèmes d’exploitation de niveau supérieur

la mise à jour de plateforme pour Windows Vista est un ensemble de bibliothèques runtime qui permet aux développeurs de cibler des applications à la fois sur Windows 7 et sur des systèmes d’exploitation de niveau supérieur. la mise à jour de la plateforme pour Windows Server 2008 est un ensemble de bibliothèques runtime qui permet aux développeurs de cibler des applications à la fois sur Windows server 2008 R2 et les versions antérieures de Windows server. la mise à jour de plateforme pour Windows vista et la mise à jour de plateforme pour Windows Server 2008 seront disponibles pour tous les clients Windows Vista et Windows Server 2008 par le biais de Windows Update. les applications tierces qui requièrent la mise à jour de la plateforme pour Windows Vista ou la mise à jour de la plateforme pour Windows Server 2008 peuvent avoir Windows Update détecter si elle est installée ou non ; si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.

la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plate-forme pour Windows Server 2008 prennent en charge l’ensemble des fonctionnalités de l’API d’automatisation Windows 3,0 sur les systèmes d’exploitation suivants.

-   Windows XP (anglais) <dl> Windows XP famille SP3 x86  
    Windows XP Professional SP3 x86  
    </dl>
-   Windows Server 2003 (English) <dl> Windows Serveur 2003 SP2 (x86 et x64)  
    </dl>
-   Windows Vista (anglais) <dl> Starter SP2 (x86 et x64)  
    page d’hébergement Premium SP2 (x86 et x64)  
    Business Pack SP2 (x86 et x64)  
    Enterprise SP2 (x86 et x64)  
    Ultimate SP2 (x86 et x64)  
    </dl>
-   Windows Serveur 2008 (anglais) <dl> Windows Server 2008 SP2 (x86 et x64)  
    </dl>

pour plus d’informations sur les deux mises à jour, consultez [mise à jour de la plateforme pour Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

## <a name="in-this-section"></a>Dans cette section

-   [Notions de base d’UI Automation](entry-uiautocore-overview.md)
-   [Guide du programmeur du fournisseur UI Automation](uiauto-providerportal.md)
-   [Guide du programmeur du client UI Automation](uiauto-clientportal.md)
-   [Référence](entry-uiautocore-ref.md)
-   [Exemples](samples-entry.md)
-   [Annexes](appendix-entry.md)

 

 