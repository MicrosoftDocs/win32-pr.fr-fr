---
description: un assembly côte à côte Windows est décrit par les manifestes.
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: À propos des assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e190e6428f2e366af45a4f0961ad6ea6fb3561fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238176"
---
# <a name="about-side-by-side-assemblies"></a>À propos des assemblys côte à côte

un assembly côte à côte Windows est décrit par les [manifestes](manifests.md). un assembly côte à côte contient une collection de ressources (un groupe de dll, de classes de Windows, de serveurs COM, de bibliothèques de types ou d’interfaces) qui sont toujours fournies aux applications ensemble. Celles-ci sont décrites dans le manifeste de l’assembly.

En général, un assembly côte à côte est une DLL unique. par exemple, l’assembly Microsoft COMCTL32 est une DLL unique avec un manifeste, tandis que l’assembly des bibliothèques runtime du système de développement Microsoft Visual C++ contient plusieurs fichiers. Les manifestes contiennent des [*métadonnées*](m-sbscs-gly.md) qui décrivent des assemblys côte à côte et des dépendances d’assembly côte à côte.

Les assemblys côte à côte sont utilisés par le système d’exploitation comme unités fondamentales de dénomination, de liaison, de contrôle de version, de déploiement et de configuration. Chaque assembly côte à côte a une identité unique. L’un des attributs de l’identité de l’assembly est sa version. Pour plus d’informations, consultez [versions d’assembly](assembly-versions.md).

à partir de Windows XP, plusieurs versions d’assemblys côte à côte peuvent être utilisées par les applications qui s’exécutent en même temps. Les manifestes, et le numéro de version de l’assembly, sont utilisés par le chargeur pour déterminer la liaison correcte des versions d’assembly aux applications. Les assemblys et les manifestes côte à côte fonctionnent avec les applications et le gestionnaire côte à côte, comme illustré dans la figure suivante.

![représentation d’un assembly côte à côte classique](images/sxsman.png)

Dans l’exemple précédent, les Comctl32.DLL version 6,0 et Comctl32.DLL version 5,0 se trouvent dans le cache d’assembly côte à côte et sont disponibles pour les applications. Quand une application appelle pour charger la DLL, le gestionnaire côte à côte détermine si l’application a une dépendance de version décrite dans un manifeste. S’il n’existe aucun manifeste pertinent, le système charge la version par défaut de l’assembly. pour Windows XP, la version 5,0 de Comctl32.DLL est la valeur système par défaut. Si le gestionnaire côte à côte trouve une dépendance sur la version 6,0 indiquée dans un manifeste, cette version est chargée pour s’exécuter avec l’application.

Plusieurs assemblys système clés sont mis à disposition par Microsoft en tant qu’assemblys côte à côte. Pour plus d’informations, consultez [assemblys côte à côte Microsoft pris en charge](supported-microsoft-side-by-side-assemblies.md). Les développeurs d’applications peuvent également créer leurs propres assemblys côte à côte. Pour plus d’informations, consultez [instructions relatives à la création d’assemblys côte à côte](guidelines-for-creating-side-by-side-assemblies.md). Dans de nombreux cas, il est possible de mettre à jour des applications existantes pour utiliser des assemblys côte à côte sans avoir à modifier le code de l’application.

Les développeurs sont encouragés à utiliser des assemblys côte à côte pour créer des [applications isolées](isolated-applications.md)et à mettre à jour des applications existantes dans des applications isolées pour les raisons suivantes :

-   Les assemblys côte à côte réduisent le risque de conflits de versions de DLL.
-   le partage d’assembly côte à côte permet l’exécution de plusieurs versions d’assemblys COM ou Windows en même temps.
-   Les applications et les administrateurs peuvent mettre à jour la configuration de l’assembly à la base d’une configuration [globale](publisher-configuration.md) ou [par application](per-application-configuration.md) après le déploiement. Par exemple, une application peut être mise à jour pour utiliser un assembly côte à côte qui comprend une mise à jour sans avoir à réinstaller l’application.

 

 



