---
description: Les applications isolées sont des applications auto-descriptives installées avec des manifestes. Les applications isolées peuvent utiliser des assemblys privés et des assemblys partagés.
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: Applications isolées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10c1b3f175ec05751bfc84e3826b19c9c9db01f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237954"
---
# <a name="isolated-applications"></a>Applications isolées

Les applications isolées sont des applications auto-descriptives installées avec des [manifestes](manifests.md). Les applications isolées peuvent utiliser des [assemblys privés](/windows/desktop/Msi/private-assemblies) et des [assemblys partagés](/windows/desktop/Msi/shared-assemblies).

Une application est considérée comme totalement isolée si tous ses composants sont des [assemblys côte à côte](about-side-by-side-assemblies-.md) partagés ou des assemblys privés. Elle est appelée partiellement isolée si elle utilise des composants qui ne sont pas des assemblys côte à côte. Notez que, si une application utilise des composants qui ne sont pas des assemblys côte à côte, ou utilise des assemblys privés, l’application peut être affectée par l’installation ou la suppression d’autres applications sur le système. Pour plus d’informations, consultez [partage d’assembly côte à côte](side-by-side-assembly-sharing.md).

Les développeurs sont encouragés à concevoir des applications isolées et à mettre à jour des applications existantes dans des applications isolées pour les raisons suivantes :

-   Les applications isolées sont plus stables et mises à jour de façon fiable, car elles ne sont pas affectées par l’installation, la suppression ou la mise à niveau d’autres applications sur le système.
-   Les applications isolées peuvent être conçues pour s’exécuter toujours à l’aide des mêmes versions d’assembly avec lesquelles elles ont été générées et testées.
-   Les applications isolées peuvent utiliser les fonctionnalités fournies par les assemblys côte à côte mis à disposition par Microsoft. Pour plus d’informations, consultez [assemblys côte à côte Microsoft pris en charge](supported-microsoft-side-by-side-assemblies.md).
-   Les applications isolées ne sont pas liées à la planification des expéditions de leurs assemblys côte à côte, car les applications et les administrateurs peuvent mettre à jour la configuration après le déploiement sans avoir à réinstaller l’application. Cela ne s’applique pas dans le cas où une seule version de l’assembly est mise à disposition.
-   Une application totalement isolée peut être installée à l’aide de la commande **xcopy** . [Windows Installer](../msi/windows-installer-portal.md) peut également être utilisé pour installer une application isolée sans impact sur le registre. Pour plus d’informations, consultez [installation d’assemblys Win32](../msi/installation-of-win32-assemblies.md).

Dans certains cas, les applications existantes peuvent être mises à jour dans une application isolée sans avoir à réécrire le code de l’application. Un [manifeste d’application](application-manifests.md) peut être créé pour décrire les dépendances de l’application vis-à-vis des [assemblys côte à côte](about-side-by-side-assemblies-.md). Si l’application utilise des composants qui ne sont pas des assemblys côte à côte, ceux-ci peuvent être déployés en tant qu' [assemblys privés](/windows/desktop/Msi/private-assemblies). Notez que la possibilité de le faire avec des composants tiers peut dépendre de la licence, car le composant devra être créé en tant qu’assembly. par exemple, en créant un manifeste d’application et en spécifiant une dépendance sur les contrôles communs côte à côte (COMCTL32), une application qui s’exécute sur Windows XP peut tirer parti *de Windows.* Vous devez toujours tester votre application pour vous assurer qu’elle est compatible avec la nouvelle version de l’assembly COMCTL32.

Il se peut qu’il ne soit pas possible de mettre à jour toutes les applications existantes dans une application totalement isolée. par exemple, certains assemblys système de [Protection de fichiers Windows (WFP)](/windows/desktop/Wfp/windows-resource-protection-portal) ne sont pas disponibles en tant qu’assemblys côte à côte et ne peuvent pas être installés avec l’application comme un assembly privé. Il peut être possible d’isoler partiellement ces applications en spécifiant des dépendances d’assembly côte à côte pour certains des assemblys de l’application dans un manifeste d’application.

 

 
