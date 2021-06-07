---
title: Restrictions de l’interpréteur de commandes graphiques de serveur
description: Les applications serveur doivent pouvoir s’exécuter sans l’interpréteur de commandes graphique de serveur
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2a3002fc2395faba3e07d90a2322c770fe3ee9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443220"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Les applications serveur doivent pouvoir s’exécuter sans l’interpréteur de commandes graphique de serveur

## <a name="platform"></a>Plateforme

**Serveurs** – Windows Server 2012 

## <a name="description"></a>Description

L’interpréteur de commandes graphique de serveur, la fonctionnalité qui comprend l’Explorateur Windows et Internet Explorer, est installé par défaut sur les installations « serveur avec une interface graphique utilisateur » de Windows Server 2012. La fonctionnalité d’interpréteur de commandes graphique de serveur peut être désinstallée pour réduire le risque de maintenance et d’encombrement des performances, limitant ainsi le nombre de redémarrages que le serveur peut entraîner, tout en autorisant l’exécution locale des outils de gestion sur le serveur.

Une fois qu’un administrateur a désinstallé l’interpréteur de commandes graphique de serveur, le serveur se trouve dans la configuration d’interface serveur minimale :

![configuration de l’interface d’interpréteur de commandes graphique de serveur](images/minimalserverinterface.png)

Les administrateurs peuvent ensuite choisir de s’exécuter dans la configuration de l’interface serveur minimale (qui inclut un ensemble d’outils d’administration locaux), par défaut, plutôt que sur le serveur avec une configuration GUI. Cela permet la surveillance et la gestion locales, tout en réduisant l’utilisation des ressources et la fréquence de maintenance.

Les administrateurs peuvent réinstaller l’interpréteur de commandes graphique de serveur ultérieurement s’ils en ont besoin. (Les administrateurs peuvent également démarrer à partir d’une installation minimale et se « développer » dans la configuration de l’interface serveur minimale à l’aide de la fonctionnalité fonctionnalités à la demande.)

Les applications serveur doivent pouvoir s’exécuter dans la configuration de l’interface serveur minimale pour tirer parti de l’encombrement réduit de l’utilisation des ressources et de la maintenance. Cette fonctionnalité peut être obtenue en permettant à l’administrateur de choisir de ne pas installer les parties de l’application qui a besoin de l’interpréteur de commandes graphique de serveur, ou en détectant la présence de l’interpréteur de commandes graphique de serveur et en désactivant certains aspects de l’application.

L’interface serveur minimale offre une réduction des ressources et de la maintenance, car de nombreuses API et binaires incluses dans l’interpréteur de commandes graphique de serveur ne sont pas disponibles dans cette configuration. Le cas échéant, les applications serveur doivent également autoriser l’administration à distance (de préférence via la communication à distance Windows PowerShell) à partir d’une autre installation de Windows Server ou d’un client Windows. Cela permet une meilleure administration centralisée d’un ou plusieurs ordinateurs dans la configuration de l’interface serveur minimale, ou des machines dans une configuration à faible encombrement, telle que Server Core.

## <a name="manifestation"></a>Manifestation

Si une application requiert des API ou des fichiers binaires qui ne sont pas disponibles dans la configuration minimale de l’interface serveur, elle risque de ne pas s’afficher correctement à l’écran et/ou être inutilisable.

## <a name="mitigation"></a>Limitation des risques

Les développeurs d’applications serveur doivent identifier les parties de leurs applications qui nécessitent l’une des API ou les binaires supprimées et incluent des informations pour l’administrateur de serveur identifiant les parties de l’application qui ne s’exécutent pas correctement lors de l’utilisation de l’interface serveur minimale. Si ces parties de l’application peuvent éventuellement être installées ou ne sont pas absolument requises pour les fonctionnalités du produit, elles peuvent toujours être installées et exécutées dans le cadre de la configuration minimale de l’interface serveur.

Si l’application ne peut pas être utilisée sans l’interpréteur de commandes graphique de serveur, cette limitation doit être documentée et l’administrateur du serveur doit être invité à installer l’interpréteur de commandes graphique de serveur. (En cas d’ajout à une installation Server Core, il peut être nécessaire d’ajouter des fonctionnalités à l’aide de fonctionnalités à la demande.) En outre, l’application doit vérifier au démarrage que tous les fichiers requis sont disponibles, car l’interpréteur de commandes graphique de serveur peut être désinstallé à tout moment avant ou après l’installation de l’application.

## <a name="solution"></a>Solution

S’appuyer sur le plus petit ensemble de dépendances possible et modulariser les applications afin que la fonctionnalité de l’application principale puisse fonctionner sans nécessiter des composants d’interface utilisateur plus lourds. Développez des applications qui ne nécessitent aucune des API ou binaires supprimées, et reposez-vous plutôt sur les fonctionnalités contenues dans l’interface serveur minimale ou le noyau de serveur. Cela permet de réduire les besoins de maintenance tout en améliorant les performances et la satisfaction des utilisateurs.

Lorsqu’il existe des parties d’une application qui peuvent ajouter des fonctionnalités importantes lorsque l’interpréteur de commandes graphique de serveur est disponible, les développeurs d’applications peuvent :

-   Autorisez ces fonctionnalités supplémentaires à utiliser l’interpréteur de commandes graphique de serveur pour les installer en option, afin qu’ils puissent être omis des installations sur une configuration d’interface serveur minimale.
-   Détecter la présence de l’interpréteur de commandes graphique de serveur et adapter le comportement de l’application

Les développeurs d’applications doivent également s’assurer que les applications serveur sont gérables à distance lorsque cela est possible et approprié.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Détection de l’interface serveur minimale et de Server Core

Windows Server installe une valeur de Registre correspondante pour chaque niveau de serveur installé. Vous pouvez interroger l’existence de ces clés pour déterminer si l’interpréteur de commandes graphique de serveur ou les fonctionnalités minimales de l’interface serveur sont installés et activés.

HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Server \\ ServerLevels :



|   &nbsp;         | Server Core | Interface serveur minimale | Interpréteur de commandes graphique de serveur |
|------------------|-------------|--------------------------|------------------------|
| ServerCore = 1     | X           | X                        | X                      |
| Serveur-GuiMgmt = 1 |             | X                        | X                      |
| ServerGuiShell = 1 |             |                          | X                      |



 

Un « X » dans le tableau ci-dessus signifie que la clé de Registre est présente lorsque la fonctionnalité correspondante est installée.

Notez que ces niveaux de serveur sont additifs ; Si l’interpréteur de commandes graphique de serveur est installé, il s’agit de l’interface serveur minimale et de Server Core. Dans ce cas, les deux clés de Registre sont présentes.

## <a name="tests"></a>Tests

Examinez le code de votre application pour connaître les exigences qui utilisent l’un des API et binaires supprimés. Après avoir supprimé toutes les instances de ces fichiers binaires d’application de base, testez votre application dans un environnement qui n’inclut pas l’interpréteur de commandes graphique de serveur. Les outils tels que Process Monitor peuvent vous aider.

Si vous ne pouvez pas complètement cesser d’utiliser ces API et ces fichiers binaires, assurez-vous que votre application échoue correctement lorsqu’elle est exécutée sur une interface serveur minimale ou sur Server Core.

## <a name="resources"></a>Ressources

-   [Documentation Server Core existante sur MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 