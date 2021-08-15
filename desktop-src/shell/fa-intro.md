---
description: 'Cette section sur les types de fichiers et les associations de fichiers est organisée comme suit :'
ms.assetid: 45d8b729-1e9d-40c0-8306-9a475262ac40
title: Types de fichiers et associations de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd096aa81970ee1baff27ae87368d26827fd8d0b46f6bdd7c69190d5ddfc56f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459192"
---
# <a name="file-types-and-file-associations"></a>Types de fichiers et associations de fichiers

Cette section sur les types de fichiers et les associations de fichiers est organisée comme suit :

-   [Inscription de l’application](app-registration.md)
-   [Types de fichiers](fa-file-types.md)
-   [Comment choisir une extension de type de fichier](how-to-choose-a-file-type-extension.md)
-   [Comment définir des attributs de type de fichier](how-to-define-file-type-attributes.md)
-   [Comment inclure une application dans la boîte de dialogue Ouvrir avec](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Comment exclure une application de la boîte de dialogue Ouvrir avec pour les types de fichiers non associés](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)
-   [Fonctionnement des associations de fichiers](fa-how-work.md)
-   [Affichage du contenu par type de fichier ou par type](prophand-content-view.md)
-   [Comment inscrire des propriétés personnalisées et une disposition pour votre type de fichier](how-to-register-custom-properties-and-layout-for-your-file-type.md)
-   [Vérificateur de type de fichier](file-type-verifier.md)
-   [Utilisation du vérificateur de type de fichier](how-to-use-the-file-type-verifier.md)
-   [Gestionnaires de types de fichiers](fa-file-extensions.md)
-   [Identificateurs programmatiques](fa-progids.md)
-   [Comment inscrire un type de fichier pour une nouvelle application](how-to-register-a-file-type-for-a-new-application.md)
-   [Types perçus](fa-perceivedtypes.md)
-   [Tableaux d’association](fa-associationarray.md)

## <a name="additional-resources"></a>Ressources supplémentaires

-   l’option définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD) est un panneau de configuration Windows qui permet aux utilisateurs disposant de privilèges d’administrateur de définir un ordinateur par défaut et de masquer ou d’afficher une application. Les applications de média, de courrier électronique, de navigateur, de messagerie et Java sont des exemples d’applications inscrites dans SPAD. définir vos programmes par défaut (SYDP) est un panneau de configuration Windows, qui fonctionne avec des privilèges limités et permet aux utilisateurs de définir une valeur par défaut de l’utilisateur. Toute application peut s’inscrire dans SYDP. Pour plus d’informations sur SPAD et l’inscription des applications SYDP, consultez [instructions pour les associations de fichiers et les programmes par défaut](appguide-fa-defpro.md), et [définir les paramètres par défaut de l’accès aux programmes et des ordinateurs (SPAD)](cpl-setprogramaccess.md).
-   Pour obtenir des informations conceptuelles connexes, consultez [vue d’ensemble des verbes et des associations de fichiers](fa-verbs.md).
-   Pour créer un magasin de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](nse-implement.md).

Pour obtenir une documentation de référence connexe, consultez les rubriques suivantes :

-   Pour exécuter un verbe sur un élément de Shell, consultez la méthode [**InvokeVerb**](folderitem-invokeverb.md) .
-   Pour récupérer une collection de verbes qui peuvent être exécutés sur un élément de Shell, consultez la méthode [**Verbs**](folderitem-verbs.md) .
-   Pour effectuer une opération sur un fichier spécifié, consultez les fonctions [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .
-   Pour obtenir la liste des types perçus par défaut, consultez l’énumération [**perçue**](/windows/win32/api/shtypes/ne-shtypes-perceived) .
-   Pour récupérer le type perçu d’un fichier en fonction de son extension, consultez la fonction [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .

 

 



