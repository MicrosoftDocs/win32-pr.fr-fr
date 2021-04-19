---
description: Protection des ressources Windows (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre du système d’exploitation.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: À propos de Protection des ressources Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545063"
---
# <a name="about-windows-resource-protection"></a>À propos de Protection des ressources Windows

Protection des ressources Windows (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre du système d’exploitation. Il est devenu disponible à partir de Windows Server 2008 et Windows Vista. L’autorisation d’accès complet pour modifier les ressources protégées par WRP est limitée à TrustedInstaller. Les ressources protégées par WRP ne peuvent être modifiées qu’à l’aide des [mécanismes de remplacement des ressources pris en charge](supported-file-replacement-mechanisms.md) par le service d’installation des modules Windows. La protection de ces ressources empêche les défaillances de l’application et du système d’exploitation.

Les applications ne doivent pas tenter de modifier les ressources protégées par WRP, car celles-ci sont utilisées par Windows et d’autres applications. Si une application tente de modifier une ressource protégée par WRP, elle peut avoir les résultats suivants.

-   Les programmes d’installation d’application qui tentent de remplacer, de modifier ou de supprimer les fichiers ou clés de Registre critiques de Windows peuvent ne pas réussir à installer l’application et recevront un message d’erreur indiquant que l’accès à la ressource a été refusé.
-   Les applications qui tentent d’ajouter ou de supprimer des sous-clés ou de modifier les valeurs des clés de Registre protégées peuvent échouer et un message d’erreur s’affiche indiquant que l’accès à la ressource a été refusé.
-   Les applications qui reposent sur l’écriture d’informations dans des clés de Registre protégées, des dossiers ou des fichiers peuvent échouer.

WRP est le nouveau nom de la protection de fichiers Windows (WFP). WRP protège les clés de Registre et les dossiers, ainsi que les fichiers système essentiels. WFP était disponible dans Microsoft Windows Server 2003 et Windows XP. WRP remplace WFP dans Windows Server 2008 et Windows Vista.

Les rubriques suivantes décrivent WRP :

-   [Liste des ressources protégées](protected-file-list.md)
-   [Détection du remplacement des ressources](detecting-file-replacement.md)
-   [Mécanismes de remplacement des ressources pris en charge](supported-file-replacement-mechanisms.md)
-   [Vérificateur des fichiers système](system-file-checker.md)
-   [Considérations relatives à l’administration à distance](remote-administration-considerations.md)

 

 



