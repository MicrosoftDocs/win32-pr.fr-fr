---
title: Utilisation des fonctions de configuration de l’analyseur de High-Level
description: Utilisation des fonctions de configuration de l’analyseur de High-Level
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- surveiller, fonctions
- surveiller, fonctions de configuration de haut niveau
- surveiller, énumérer les moniteurs physiques
- moniteur, paramètres continus
- configuration de l’analyse, fonctions de configuration de haut niveau
- configuration de l’analyse, fonctions
- surveiller la configuration, énumération des analyses physiques
- configuration de l’analyse, paramètres continus
- énumération des analyses physiques
- fonctions de configuration de haut niveau
- paramètres d’analyse continue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d19ef0006dc89208061c18ef34c28c8f993c3e0d6ebd0d1c1005daf2cd640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066599"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a>Utilisation des fonctions de configuration de l’analyseur de High-Level

## <a name="enumerating-physical-monitors"></a>Énumération des analyses physiques

Il existe plusieurs fonctions qui énumèrent les appareils d’affichage, y compris [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) et [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow). ces fonctions sont documentées dans la documentation Windows GDI, sous la rubrique [moniteurs à affichage Multiple](/windows/desktop/gdi/multiple-display-monitors). Ces fonctions retournent des handles **HMONITOR** . En dépit du nom, toutefois, un descripteur **HMONITOR** peut être associé à plusieurs analyses physiques. Pour configurer les paramètres d’une analyse, l’application doit obtenir un handle unique vers le moniteur physique en appelant [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor).

Si votre application utilise Direct3D, vous pouvez obtenir un handle de moniteur à partir d’un périphérique Direct3D en appelant [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9).

## <a name="supported-functions"></a>Fonctions prises en charge

Une analyse peut ne pas prendre en charge toutes les fonctions de configuration de l’analyse. Pour connaître les fonctions prises en charge par une analyse, appelez [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities).

## <a name="continuous-monitor-settings"></a>moniteur continu Paramètres

Un paramètre de moniteur *continu* est une valeur qui peut être comprise entre une valeur minimale et une valeur maximale. La plupart des fonctions de configuration d’analyse de haut niveau contrôlent les paramètres de moniteur continus. Par exemple, la luminosité et le contraste sont des paramètres continus.

Les paramètres d’analyse continue n’ont pas d’unités réelles définies. Les unités sont arbitraires et peuvent varier d’un fabricant à l’autre. Si deux moniteurs ont la même valeur de luminosité, par exemple, un moniteur peut paraître nettement plus clair qu’un autre. En règle générale, une application présente des contrôles Slider ou des contrôles up-out à l’utilisateur. L’utilisateur peut ensuite ajuster les paramètres pour offrir la meilleure qualité subjective.

## <a name="changes-in-monitor-state"></a>Modifications de l’état du moniteur

Une analyse peut modifier les États pour diverses raisons, notamment :

-   L’utilisateur modifie les paramètres avec les contrôles du panneau avant de l’analyse.
-   L’utilisateur modifie la résolution d’écran, la fréquence d’actualisation ou la profondeur de bit du moniteur.
-   L’application utilise les fonctions d’analyse de bas niveau pour modifier un paramètre qui n’est pas accessible à partir des fonctions de haut niveau.
-   L’application appelle [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) ou [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults).

Tous ces événements peuvent modifier les paramètres d’analyse. Elles peuvent également modifier la valeur minimale et la valeur maximale d’un paramètre.

## <a name="dependencies-among-monitor-settings"></a>dépendances entre l’analyse Paramètres

La modification de la température de couleur peut modifier le lecteur actuel et obtenir les paramètres, et l’inverse est également vrai. Il s’agit des seules dépendances entre les fonctions de configuration de l’analyse de haut niveau. D’autres paramètres peuvent être accessibles uniquement par le biais des fonctions de surveillance de bas niveau. Il peut y avoir des dépendances entre ces paramètres et les paramètres de haut niveau. Ces dépendances sont spécifiques au fournisseur. Une application peut gérer ce problème de plusieurs façons :

-   Utilisez uniquement des fonctions de haut niveau.
-   Après avoir appelé une fonction de bas niveau, récupérez la valeur actuelle de chaque paramètre d’analyse. Malheureusement, cette approche peut être lente, car l’obtention de chaque paramètre dure environ 40 millisecondes.
-   Utilisez des fonctions de bas niveau uniquement avec des modèles d’analyse spécifiques dont vous comprenez le comportement.

## <a name="disabled-monitor-settings"></a>Paramètres du moniteur désactivé

Une application ne peut pas désactiver les paramètres d’analyse en appelant les fonctions de surveillance de haut niveau. Toutefois, une application peut désactiver accidentellement un paramètre si elle utilise les fonctions de bas niveau pour modifier un paramètre d’analyse qui n’est pas pris en charge par les fonctions de haut niveau. En outre, un utilisateur peut désactiver un paramètre à l’aide du contrôle de panneau avant. Ces comportements sont spécifiques au fournisseur.

Si un paramètre d’analyse est désactivé, toute fonction qui définit ou récupère ce paramètre échoue et définit le dernier code d’erreur sur le paramètre d’analyse « erreur \_ désactivée » \_ \_ . Dans ce cas, l’application peut effectuer l’une des opérations suivantes :

-   Affichez un message d’erreur et Suggérez à l’utilisateur qu’il tente d’ajuster le paramètre à l’aide du contrôle de panneau avant.
-   Appelez la fonction [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) . Si un moniteur a les paramètres \_ par défaut de l’usine de restauration MC \_ active l' \_ indicateur de \_ \_ fonctionnalités surveiller les \_ paramètres, cette fonction active tous les paramètres d’analyse pris en charge par les fonctions d’analyse de haut niveau. Malheureusement, la fonction rétablit également les paramètres d’usine par défaut de l’analyse.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la configuration de l’analyse](using-monitor-configuration.md)
</dt> </dl>

 

 