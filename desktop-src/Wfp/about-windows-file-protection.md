---
description: Windows La protection des ressources (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre du système d’exploitation.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: à propos de Protection des ressources Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d06110c668e48a401cc329d79982e7c1b2746408ce45da9b7b3dffaca40b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134195"
---
# <a name="about-windows-resource-protection"></a>à propos de Protection des ressources Windows

Windows La protection des ressources (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre du système d’exploitation. il est devenu disponible à partir de Windows Server 2008 et Windows Vista. L’autorisation d’accès complet pour modifier les ressources protégées par WRP est limitée à TrustedInstaller. les ressources protégées par WRP ne peuvent être modifiées qu’à l’aide des [mécanismes de remplacement des ressources pris en charge](supported-file-replacement-mechanisms.md) par le service d’installation des Modules Windows. La protection de ces ressources empêche les défaillances de l’application et du système d’exploitation.

les applications ne doivent pas tenter de modifier les ressources protégées par WRP, car elles sont utilisées par les Windows et d’autres applications. Si une application tente de modifier une ressource protégée par WRP, elle peut avoir les résultats suivants.

-   les programmes d’installation d’application qui tentent de remplacer, de modifier ou de supprimer des fichiers Windows critiques ou des clés de registre peuvent ne pas réussir à installer l’application et recevront un message d’erreur indiquant que l’accès à la ressource a été refusé.
-   Les applications qui tentent d’ajouter ou de supprimer des sous-clés ou de modifier les valeurs des clés de Registre protégées peuvent échouer et un message d’erreur s’affiche indiquant que l’accès à la ressource a été refusé.
-   Les applications qui reposent sur l’écriture d’informations dans des clés de Registre protégées, des dossiers ou des fichiers peuvent échouer.

WRP est le nouveau nom de la protection de fichier Windows (WFP). WRP protège les clés de Registre et les dossiers, ainsi que les fichiers système essentiels. WFP était disponible dans Microsoft Windows Server 2003 et Windows XP. WRP remplace WFP dans Windows Server 2008 et Windows Vista.

Les rubriques suivantes décrivent WRP :

-   [Liste des ressources protégées](protected-file-list.md)
-   [Détection du remplacement des ressources](detecting-file-replacement.md)
-   [Mécanismes de remplacement des ressources pris en charge](supported-file-replacement-mechanisms.md)
-   [Vérificateur des fichiers système](system-file-checker.md)
-   [Considérations relatives à l’administration à distance](remote-administration-considerations.md)

 

 



