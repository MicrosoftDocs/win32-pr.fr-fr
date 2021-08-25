---
title: Utilisation des informations de version
description: Cette rubrique explique comment utiliser les fonctions d’informations de version.
ms.assetid: 447b57c9-9e94-4a28-897e-f7b87d9cb25a
keywords:
- ressources, informations sur la version
- informations de version
- informations sur le fichier d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0447bc1dfc3b2d5d5006bb5ff9ca3e9fa8f3d488e9b5621acb932c843fc3630f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846989"
---
# <a name="using-version-information"></a>Utilisation des informations de version

Un programme d’installation a généralement les objectifs suivants :

-   Pour placer les fichiers à l’emplacement approprié.
-   Pour avertir l’utilisateur si le programme d’installation remplace un fichier existant par une version qui est très différente, par exemple, en remplaçant un fichier en allemand par un fichier de langue anglaise ou en remplaçant un fichier plus récent par un fichier plus ancien.

Lors de l’écriture du programme d’installation, vous devez disposer des informations suivantes pour chaque fichier :

-   Nom et emplacement du fichier (appelé fichier source).
-   Nom du fichier équivalent sur le disque dur de l’utilisateur (connu sous le nom de fichier de destination). Ce nom est généralement le même que le nom de fichier sur le disque d’installation.
-   État de partage du fichier, c’est-à-dire si le fichier est privé pour l’application en cours d’installation ou s’il peut être partagé par plusieurs applications.

Le programme d’installation peut utiliser la fonction [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) pour déterminer l’emplacement où le fichier doit être copié sur le disque. Cette fonction peut également être utilisée pour spécifier si le fichier est privé pour l’application ou s’il peut être partagé. Si un problème se produit lors de la recherche du fichier, **VerFindFile** retourne une valeur d’erreur. Par exemple, si le système utilise le fichier de destination, **VerFindFile** retourne **VFF \_ FILEINUSE**. Le programme d’installation doit avertir l’utilisateur du problème et répondre à la décision de l’utilisateur de continuer ou de mettre fin à l’installation.

La fonction [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) copie le fichier source dans un fichier temporaire dans le répertoire spécifié par [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea). Si nécessaire, **VerInstallFile** développe le fichier à l’aide des fonctions de la bibliothèque de décompression des données.

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) compare les informations de version du fichier temporaire à celles du fichier de destination. Si les deux diffèrent, **VerInstallFile** retourne une ou plusieurs valeurs d’erreur. Par exemple, elle retourne **vif \_ SRCOLD** si le fichier temporaire est plus ancien que le fichier de destination et **vif \_ DIFFLANG** si les fichiers ont des identificateurs de langue ou des valeurs de page de codes différents. Le programme d’installation doit avertir l’utilisateur du problème et répondre à la décision de l’utilisateur de continuer ou de mettre fin à l’installation.

Certaines erreurs de [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) sont récupérables. Autrement dit, le programme d’installation peut appeler à nouveau **VerInstallFile** , en spécifiant l’option **VIFF \_ FORCEINSTALL** pour installer le fichier, quel que soit le conflit de version. Si **VerInstallFile** retourne **vif \_ tempfile** et que l’utilisateur choisit de ne pas forcer l’installation, le programme d’installation doit supprimer le fichier temporaire.

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) peut rencontrer une erreur irrécupérable lors de la tentative de forcer l’installation, même si l’erreur n’existait pas précédemment. Par exemple, le fichier peut être verrouillé par un autre utilisateur avant que le programme d’installation ne tente de forcer l’installation. Si un programme d’installation tente de forcer l’installation après une erreur non récupérable, **VerInstallFile** échoue. Le programme d’installation doit contenir des routines pour effectuer une récupération à partir de ce type d’erreur.

La solution recommandée consiste à afficher une boîte de dialogue avec les boutons **installer**, **Ignorer** et **installer tout**. (Une autre solution est une boîte de dialogue avec les boutons **Oui**, **Oui pour tout**, **Ignorer** et **Annuler**.) Le bouton **installer tout** doit empêcher le programme d’installation de demander à l’utilisateur des erreurs similaires en incluant l’option **VIFF \_ FORCEINSTALL** dans toutes les utilisations suivantes de [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea). Pour les erreurs irrécupérables, les boutons **installer** et **installer tout** doivent être désactivés.

Pour afficher un message d’erreur utile à l’utilisateur, le programme d’installation doit généralement récupérer des informations à partir des ressources de version des fichiers en conflit. Le programme d’installation peut utiliser quatre fonctions à cet effet :

-   [**Échec GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)
-   [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)
-   [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
-   [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)

[**Échec GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) retourne la taille des informations de version. [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) utilise les informations extraites par **échec GetFileVersionInfoSize** pour récupérer une structure qui contient les informations de version. [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) récupère un membre spécifique de cette structure.

Par exemple, si [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) retourne l' **erreur \_ vif DIFFTYPE** , le programme d’installation doit utiliser les fonctions [**échec GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea), [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)et [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) sur les fichiers temporaires et de destination pour obtenir le type général de chaque fichier. Si les langues des fichiers sont en conflit, le programme d’installation doit également utiliser [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea) pour convertir l’identificateur de langue binaire en une représentation textuelle de la langue. (Par exemple, 0x040C se traduit par la chaîne « French ».)

Si [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) retourne une erreur de fichier, par exemple **vif \_ ACCESSVIOLATION**, le programme d’installation doit utiliser la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour récupérer la valeur d’erreur la plus récente. Le programme doit traduire cette valeur en message d’information à afficher à l’utilisateur. Le programme ne doit pas générer de contrôle entre les appels à **VerInstallFile** et **GetLastError**.

 

 