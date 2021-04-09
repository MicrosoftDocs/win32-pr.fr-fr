---
description: Les applications isolées et les assemblys côte à côte fournissent une solution qui réduit les conflits de contrôle de version des DLL. Elles permettent aux applications de partager en toute sécurité des assemblys. Pour plus d’informations, consultez assemblys partagés.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: À propos des applications isolées et des assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9099ca2e41d61c84e2952661b33ca008651f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115494"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>À propos des applications isolées et des assemblys côte à côte

Les [applications isolées](isolated-applications.md) et les [assemblys côte à côte](about-side-by-side-assemblies-.md) fournissent une solution qui réduit les conflits de contrôle de [*version des dll*](d-sbscs-gly.md). Elles permettent aux applications de partager en toute sécurité des assemblys. Pour plus d’informations, consultez [assemblys partagés](/windows/desktop/Msi/shared-assemblies).

Un assembly est une unité fondamentale pour l’affectation de noms, la liaison, le contrôle de version, le déploiement ou la configuration d’un bloc de code de programmation. Les applications avec des fonctionnalités communes peuvent exécuter des blocs partagés de code de programmation, appelés modules ou assemblys de code. Ces assemblys de code peuvent être placés dans des dll ou des assemblys COM. L’infrastructure pour le partage sécurisé des assemblys est appelée partage d’assembly côte à côte.

Les [assemblys côte à côte](about-side-by-side-assemblies-.md) sont des assemblys de code décrits par des [manifestes](manifests.md) et créés de sorte que plusieurs versions puissent s’exécuter en même temps sans entrer en conflit. Lorsque les développeurs créent des manifestes et écrivent des applications pour utiliser le [partage d’assembly côte à côte](side-by-side-assembly-sharing.md), plusieurs versions d’assembly peuvent s’exécuter sur le système et chaque application peut spécifier la version d’assembly qu’elle doit utiliser.

Un [*assembly côte à côte*](s-sbscs-gly.md) classique est une dll unique avec un manifeste unique. Les assemblys côte à côte stockent les informations relatives à la liaison et à l’activation COM, traditionnellement enregistrées dans le registre, dans les manifestes. Dans certains cas, les versions de l’assembly spécifiées dans les manifestes peuvent être modifiées, sur une base globale ou par application, par les serveurs de publication d’assembly, les développeurs d’applications ou les administrateurs. Pour plus d’informations, consultez [configuration par défaut](default-configuration.md), configuration du serveur de [publication](publisher-configuration.md)et [configuration par application](per-application-configuration.md).

Les développeurs peuvent utiliser les assemblys côte à côte fournis par Microsoft, ou d’autres serveurs de publication d’assembly côte à côte, dans leurs applications. Par exemple, les développeurs peuvent obtenir les fonctionnalités des contrôles communs mis à jour, tels que les thèmes, en concevant leurs applications de manière à utiliser l’assembly côte à côte qui contient Comctl32.dll 6,0. Pour obtenir la liste des assemblys et des manifestes côte à côte fournis avec Windows XP, consultez [assemblys côte à côte pris en charge par Microsoft](supported-microsoft-side-by-side-assemblies.md). Les développeurs peuvent également créer leurs propres assemblys côte à côte. Pour plus d’informations, consultez [instructions relatives à la création d’assemblys côte à côte](guidelines-for-creating-side-by-side-assemblies.md).

 

 
