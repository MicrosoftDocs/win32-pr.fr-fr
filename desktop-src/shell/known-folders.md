---
description: Windows Vista introduit de nouveaux scénarios de stockage et un nouvel espace de noms de profil utilisateur.
title: Dossiers connus
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3b5fbdaf0086f88fc4eed42ce47749a99ab07b40
ms.sourcegitcommit: 8bfe4f468ee5de7bbe096e5db81e427db53d977c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/26/2021
ms.locfileid: "114680312"
---
# <a name="known-folders"></a>Dossiers connus

Windows Vista introduit de nouveaux scénarios de stockage et un nouvel espace de noms de profil utilisateur. Pour répondre à ces nouveaux facteurs, l’ancien système de référence aux dossiers standard par une valeur [**CSIDL**](csidl.md) a été remplacé. à partir de Windows Vista, ces dossiers sont référencés par un nouvel ensemble de valeurs GUID appelé id de dossier connu.

Le système de dossiers connu offre les avantages suivants :

-   Les éditeurs de logiciels indépendants (ISV) peuvent étendre l’ensemble des ID de dossiers connus avec leur propre ID. Ils peuvent définir des dossiers, leur attribuer des ID et les inscrire auprès du système. Impossible d’étendre les valeurs CSIDL.
-   Tous les dossiers connus sur un système peuvent être énumérés. Aucune API n’offrait cette fonctionnalité pour les valeurs CSIDL. Pour plus d’informations, consultez [**IKnownFolderManager :: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) .
-   Un dossier connu ajouté par un éditeur de logiciels indépendant peut ajouter des propriétés personnalisées qui lui permettent d’expliquer son rôle et son utilisation prévue.
-   De nombreux dossiers connus peuvent être redirigés vers de nouveaux emplacements, y compris des emplacements réseau. Sous le système CSIDL, seul le dossier **Mes documents** peut être redirigé.
-   Les dossiers connus peuvent avoir des gestionnaires personnalisés à utiliser lors de la création ou de la suppression.

Le système CSIDL et les API qui font appel aux valeurs CSIDL sont toujours pris en charge pour la compatibilité. Toutefois, il n’est pas recommandé de les utiliser dans un nouveau développement.


Les rubriques suivantes décrivent les caractéristiques du système de dossiers connus.

-   [Utilisation de dossiers connus dans les applications](working-with-known-folders.md)
-   [Comment étendre des dossiers connus avec des dossiers personnalisés](how-to-extend-known-folders-with-custom-folders.md)
-   [**KNOWNFOLDERID**](knownfolderid.md)

Les pages de référence suivantes décrivent les fonctions de dossiers connus Win32, qui peuvent être utilisées pour récupérer l’emplacement des dossiers connus ou les rediriger vers un nouvel emplacement. Ces fonctions remplacent les anciennes fonctions Win32. Les nouvelles fonctions sont fournies pour fournir un comportement équivalent aux anciennes fonctions, mais chaque nouvelle fonction est également dupliquée par une API COM (Component Object Model).



| Nouvelle fonction                                             | Remplace                                           | Équivalent COM                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [**IKnownFolder::GetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [**SHGetKnownFolderIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [**IKnownFolder::GetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [**IKnownFolder::SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

Les pages de référence suivantes décrivent les API de dossiers connus COM, qui fournissent toutes les fonctionnalités des API Win32 répertoriées ci-dessus, ainsi que la possibilité d’énumérer tous les dossiers connus, d’accéder aux propriétés de dossier connues et d’étendre l’ensemble standard de dossiers connus.

-   [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

un exemple C++ qui illustre les api de dossiers connus est inclus dans le kit de développement logiciel (SDK) Windows. une fois que vous avez installé le SDK Windows sur votre ordinateur, l’exemple se trouve sous% ProgramFiles% \\ Microsoft sdk \\ Windows \\ v 6.0 \\ samples \\ WinUI \\ Shell \\ AppPlatform \\ fichier knownfolders.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Dossiers connus, exemple](/windows/win32/shell/samples-knownfolders)
</dt> </dl>
