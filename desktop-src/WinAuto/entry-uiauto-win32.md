---
title: Automatisation de l’interface utilisateur
description: Microsoft UI Automation est une infrastructure d’accessibilité qui permet aux applications Windows de fournir et d’utiliser des informations de programmation sur les interfaces utilisateur.
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842541"
---
# <a name="ui-automation"></a>Automatisation de l’interface utilisateur

Microsoft UI Automation est une infrastructure d’accessibilité qui permet aux applications Windows de fournir et d’utiliser des informations de programmation sur les interfaces utilisateur. Il fournit un accès par programme à la plupart des éléments d’interface utilisateur sur le bureau. Il permet aux produits de technologie d’assistance, tels que les lecteurs d’écran, de fournir des informations sur l’interface utilisateur aux utilisateurs finaux et de manipuler l’interface utilisateur par d’autres moyens que l’entrée standard. UI Automation permet également aux scripts de test automatisés d’interagir avec l’interface utilisateur.

-   [Le cas échéant](#where-applicable)
-   [Public destiné aux développeurs](#developer-audience)
-   [Spécifications d’exécution](#run-time-requirements)
-   [Prise en charge des systèmes d’exploitation de niveau supérieur](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a>Cas d'emploi

À l’aide d’UI Automation et des pratiques de conception accessibles suivantes, les développeurs peuvent rendre les applications s’exécutant sur Windows plus accessibles à de nombreuses personnes avec une vision, une audition ou un handicap moteur. En outre, UI Automation est spécifiquement conçu pour fournir des fonctionnalités robustes pour les scénarios de test automatisé.

## <a name="developer-audience"></a>Public de développeurs

UI Automation est conçu pour les développeurs C/C++ expérimentés. En général, les développeurs ont besoin d’un niveau modéré de compréhension des objets COM (Component Object Model) et des interfaces, d’Unicode et de la programmation des API Windows.

Pour plus d’informations sur UI Automation pour le code managé, consultez [accessibilité](/dotnet/framework/ui-automation/) dans la section Guide du développeur .NET Framework de MSDN.

## <a name="run-time-requirements"></a>Exigences d'exécution

UI Automation est pris en charge sur les systèmes d’exploitation suivants : Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 et Windows Server 2019.

> [!Note]  
> Windows XP et Windows Server 2003 nécessitent également Microsoft .NET Framework 3,0.

 

## <a name="support-for-down-level-operating-systems"></a>Prise en charge des systèmes d’exploitation de niveau supérieur

La mise à jour de plateforme pour Windows Vista est un ensemble de bibliothèques d’exécution qui permet aux développeurs de cibler des applications sur des systèmes d’exploitation Windows 7 et de niveau supérieur. La mise à jour de plateforme pour Windows Server 2008 est un ensemble de bibliothèques d’exécution qui permet aux développeurs de cibler des applications à la fois vers Windows Server 2008 R2 et pour les versions antérieures de Windows Server. La mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008 seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update. Les applications tierces qui requièrent une mise à jour de plateforme pour Windows Vista ou une mise à jour de plateforme pour Windows Server 2008 peuvent avoir Windows Update détecter si elles sont installées ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.

La mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 prennent en charge l’ensemble des fonctionnalités de l’API Windows Automation 3,0 sur les systèmes d’exploitation suivants.

-   Windows XP (anglais) <dl> Windows XP famille SP3 x86  
    Windows XP Professionnel SP3 x86  
    </dl>
-   Windows Server 2003 (English) <dl> Windows Server 2003 SP2 (x86 et x64)  
    </dl>
-   Windows Vista (anglais) <dl> Starter SP2 (x86 et x64)  
    Édition familiale Premium SP2 (x86 et x64)  
    Business Pack SP2 (x86 et x64)  
    Enterprise SP2 (x86 et x64)  
    Ultimate SP2 (x86 et x64)  
    </dl>
-   Windows Server 2008 (anglais) <dl> Windows Server 2008 SP2 (x86 et x64)  
    </dl>

Pour plus d’informations sur les deux mises à jour, consultez [mise à jour de la plateforme pour Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

## <a name="in-this-section"></a>Dans cette section

-   [Notions de base d’UI Automation](entry-uiautocore-overview.md)
-   [Guide du programmeur du fournisseur UI Automation](uiauto-providerportal.md)
-   [Guide du programmeur du client UI Automation](uiauto-clientportal.md)
-   [Référence](entry-uiautocore-ref.md)
-   [Exemples](samples-entry.md)
-   [Annexes](appendix-entry.md)

 

 