---
description: Un assembly partagé est un assembly pouvant être utilisé par plusieurs applications sur l’ordinateur.
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: À propos des assemblys partagés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5db7f10ea5ffa6e04fd5cd905262eb026b4ca4c24309ffd4c53cb10f9df00b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142622"
---
# <a name="about-shared-assemblies"></a>À propos des assemblys partagés

Un assembly partagé est un assembly pouvant être utilisé par plusieurs applications sur l’ordinateur. sur Windows Vista et Windows XP, les [assemblys côte à côte](about-side-by-side-assemblies-.md) peuvent être installés en tant qu’assemblys partagés. Les assemblys côte à côte partagés ne sont pas inscrits globalement sur le système, mais ils sont globalement disponibles pour les applications qui spécifient une dépendance sur l’assembly dans les [manifestes](manifests.md). Plusieurs versions d’assemblys côte à côte peuvent être partagées par différentes applications qui s’exécutent en même temps. Pour plus d’informations, consultez [à propos des applications isolées et des assemblys côte à côte](about-isolated-applications-and-side-by-side-assemblies.md). par exemple, les [assemblys Microsoft côte à côte pris en charge](supported-microsoft-side-by-side-assemblies.md) fournis avec Windows XP sont généralement utilisés comme assemblys partagés par plusieurs applications.

Les assemblys côte à côte partagés sont installés dans le dossier WinSxS. Les éditeurs d’assemblys, les applications et les administrateurs peuvent modifier la version des dépendances d’assembly côte à côte après le déploiement via la [configuration](configuration.md). les assemblys côte à côte partagés peuvent être installés par une mise à jour du système d’exploitation ou par un package Windows Installer qui installe ou met à jour une application. Pour plus d’informations, consultez [installation d’assemblys Win32](../msi/installation-of-win32-assemblies.md).

avant Windows XP, les assemblys partagés étaient inscrits globalement et installés dans le dossier système Windows. Dans ce cas, la dernière version installée de l’assembly est disponible pour toutes les applications qui y sont liées. Un assembly côte à côte peut également être installé en tant qu’assembly privé pour l’utilisation exclusive d’une application. Pour plus d'informations, consultez [Assemblys privés](/windows/desktop/Msi/private-assemblies).

 

 
