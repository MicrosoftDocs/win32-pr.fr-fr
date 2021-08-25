---
description: La préparation des ressources pour une application MUI prend en charge les modèles PE Win32 et non Win32.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Préparation des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef40453ca6db40bed1c07bad80f7e21cb7adaa7ea48ae8ee5ce2a2a5c657ba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040669"
---
# <a name="preparing-resources"></a>Préparation des ressources

La préparation des ressources pour une application MUI prend en charge les modèles PE Win32 et non Win32. Les ressources Win32 PE sont fournies dans des fichiers PE, tels que des fichiers .dll, .exe ou .sys. Les ressources PE non Win32 sont fournies dans un module personnalisé de votre choix.

> [!Note]  
> Il est fortement recommandé d’utiliser des ressources Win32 PE pour les applications MUI Win32, car ces ressources sont entièrement prises en charge par la technologie de ressources MUI. Les fichiers de ressources PE non Win32 peuvent être localisés en appelant la fonction [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) , comme décrit dans [recherche de ressources PE non Win32](locating-non-win32-pe-resources.md), mais l’application doit fournir ses propres fonctionnalités pour rechercher et charger les ressources requises.

 

Cette section contient les rubriques suivantes :

-   [Création du fichier de ressources de la langue de base](creating-the-base-language-resource-file.md)
-   [Utilisation de la redirection de chaînes de Registre](using-registry-string-redirection.md)
-   [Préparation d’un fichier de configuration de ressource](preparing-a-resource-configuration-file.md)

 

 



