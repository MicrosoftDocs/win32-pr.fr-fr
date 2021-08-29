---
description: les fonctions suivantes sont utilisées avec interface utilisateur multilingue (MUI).
ms.assetid: 918d1f04-78fe-4b60-bee7-08d2f131437e
title: interface utilisateur multilingue Mission
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507118ce04895c9b13f5c9d71fae69717a38e2d74186159fb2efcef7f45a0c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041219"
---
# <a name="multilingual-user-interface-functions"></a>interface utilisateur multilingue Mission

les fonctions suivantes sont utilisées avec interface utilisateur multilingue (MUI).



| Fonction                                                                 | Description                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa)                               | Énumère les langues d’interface utilisateur disponibles sur le système d’exploitation.                                     |
| [**EnumUILanguagesProc**](/windows/win32/api/winnls/nc-winnls-uilanguage_enumproca)                       | Fonction définie par l’application utilisée avec la fonction [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .                      |
| [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)                                 | Décrémente le décompte de références d’un module de ressource chargé par [ **LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                  |
| [**GetFileMUIInfo**](/windows/desktop/api/Winnls/nf-winnls-getfilemuiinfo)                                 | Récupère des informations relatives aux ressources sur un fichier.                                                                    |
| [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)                                 | Récupère le chemin d’accès à un fichier de ressources spécifique à un langage associé au fichier LN fourni.                           |
| [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages) | Récupère les langues d’interface utilisateur préférées du processus.                                                                           |
| [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)         | récupère l’identificateur de langue pour la langue d’interface utilisateur par défaut du système, appelée « langue d’installation » sur Windows Vista. |
| [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)   | Récupère les langues d’interface utilisateur par défaut du système.                                                                            |
| [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)   | Récupère les langues d’interface utilisateur préférées du thread pour le thread actuel.                                                     |
| [**GetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getthreaduilanguage)                       | Retourne l’identificateur de langue de la première langue de l’interface utilisateur pour le thread actuel.                            |
| [**GetUILanguageFallbackList**](/windows/desktop/api/Muiload/nf-muiload-getuilanguagefallbacklist)           | Obtient une liste de secours des langues de l’interface utilisateur, représentées sous la forme de noms de langage.                                         |
| [**GetUILanguageInfo**](/windows/desktop/api/Winnls/nf-winnls-getuilanguageinfo)                           | Récupère une variété d’informations sur une langue de l’interface utilisateur.                                                     |
| [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage)             | Retourne l’identificateur de langue pour la langue de l’interface utilisateur de l’utilisateur actuel.                                          |
| [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)       | Récupère les langues d’interface utilisateur préférées de l’utilisateur.                                                                              |
| [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                                 | Retourne un handle vers les ressources spécifiques au langage associées à un fichier spécifique à la langue (LN).            |
| [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) | Définit les langues d’interface utilisateur préférées pour le processus d’application.                                                    |
| [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)   | Définit les langues d’interface utilisateur préférées du thread.                                                                                 |
| [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage)                       | Définit la langue de l’interface utilisateur par défaut pour le thread actuel.                                                      |



 

 

 
