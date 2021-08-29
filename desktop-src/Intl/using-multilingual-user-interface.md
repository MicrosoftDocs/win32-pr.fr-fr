---
description: utilisation de interface utilisateur multilingue
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: utilisation de interface utilisateur multilingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bcd970b71957fe865f30d031d0706f37cccdbd527ee65fb6e4a812f2836bb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764619"
---
# <a name="using-multilingual-user-interface"></a>utilisation de interface utilisateur multilingue

cette section décrit comment utiliser la fonctionnalité de interface utilisateur multilingue (MUI) pour concevoir et implémenter vos applications. Vous trouverez ci-dessous des aspects de la technologie MUI qui vont être joués à la plupart des étapes du cycle de vie de l’application.

-   Développement d’applications, notamment la préparation des ressources, le paramétrage des préférences linguistiques de l’application, la recherche et le chargement des ressources
-   Génération et localisation de l’application
-   Déploiement de l’application

Voici quelques questions à prendre en compte lors de la conception et de l’implémentation d’une application MUI.

-   quelles sont les versions de Windows que l’application prendra en charge ?
-   Dans quelles langues l’application sera-t-elle localisée ?
-   Les paramètres de langue de l’application doivent-ils toujours suivre les paramètres de langue du système d’exploitation ou l’utilisateur de l’application est-il en mesure de définir des langues spécifiques ?
-   Quels types de ressources d’interface utilisateur l’application utilise-t-elle et où sont-elles stockées ?

Cette section comprend les rubriques suivantes. les descriptions supposent une application MUI ciblée sur Windows Vista et versions ultérieures. Les ressources de cette application sont des ressources Win32, avec des ressources spécifiques à la langue et du code exécutable résidant dans des fichiers PE Win32 distincts. des considérations spéciales pour la prise en charge des systèmes d’exploitation antérieurs à Windows Vista ou pour différents types de ressources sont ajoutées, le cas échéant.

-   [Préparation des ressources](preparing-resources.md)
-   [Définition des préférences linguistiques de l’application](setting-application-language-preferences.md)
-   [Recherche de ressources Win32 PE](locating-win32-pe-resources.md)
-   [Recherche de ressources PE non Win32](locating-non-win32-pe-resources.md)
-   [Localisation des ressources et génération de l’application](localizing-resources-and-building-the-application.md)
-   [MUI : exemple d’Application Paramètres système](mui-system-settings-application-sample.md)
-   [MUI : exemple de Paramètres Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
-   [MUI : exemple de Paramètres Application-Specific (pré-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)

 

 



