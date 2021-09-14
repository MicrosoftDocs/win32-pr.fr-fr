---
description: Un assembly Win32 peut être installé en tant qu’assembly partagé et être disponible pour une utilisation par plusieurs applications sur l’ordinateur. les assemblys partagés doivent être installés par un package Windows Installer utilisé pour installer ou mettre à jour une application.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Assemblys partagés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218713"
---
# <a name="shared-assemblies"></a>Assemblys partagés

Un assembly Win32 peut être installé en tant qu’assembly partagé et être disponible pour une utilisation par plusieurs applications sur l’ordinateur. les assemblys partagés doivent être installés par un package Windows Installer utilisé pour installer ou mettre à jour une application.

Les assemblys partagés sont installés en tant qu' [assemblys côte à côte](side-by-side-assemblies.md). le Windows Installer installe les assemblys côte à côte partagés dans le dossier Winsxs. Les assemblys ne sont pas inscrits globalement sur le système, mais ils sont disponibles à l’échelle mondiale pour toute application qui spécifie une dépendance sur l’assembly dans un fichier manifeste. Pour plus d’informations, consultez [applications isolées et assemblys côte à côte](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

sur les systèmes d’exploitation antérieurs à Windows XP, les assemblys partagés sont généralement installés dans le dossier système Windows et enregistrés globalement. La dernière version installée est disponible pour toutes les applications qui y sont liées.

pour plus d’informations sur la création d’un package Windows Installer pour installer un assembly partagé, consultez les rubriques suivantes :

-   [installation d’assemblys Win32 pour le partage côte à côte sur Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [installation d’assemblys Win32 pour l’utilisation privée d’une Application sur Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
