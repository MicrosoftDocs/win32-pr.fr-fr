---
description: Un tableau d’associations est une liste ordonnée d’emplacements de Registre utilisée pour stocker des informations sur un type d’élément, y compris les gestionnaires, les verbes et d’autres attributs, tels que l’icône et le nom d’affichage du type.
title: Tableaux d’association
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d3d2143c4febd683aef1d175d61f97b300db5382e97fe8f466b58b069665fa1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050409"
---
# <a name="association-arrays"></a>Tableaux d’association

Un tableau d’associations est une liste ordonnée d’emplacements de Registre utilisée pour stocker des informations sur un type d’élément, y compris les gestionnaires, les verbes et d’autres attributs, tels que l’icône et le nom d’affichage du type. L’interpréteur de commandes utilise des tableaux d’association pour interroger un ensemble prédéfini d’emplacements de Registre qui peut contenir des informations sur un élément de Shell.

Cette rubrique est organisée comme suit :

-   [À propos des tableaux d’association](#about-association-arrays)
-   [Interrogation des tableaux d’association](#querying-association-arrays)
-   [Utilisation de tableaux d’association pour une source de données Shell particulière](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [Groupes d’associations de la source de données Shell](#shell-data-source-association-arrays)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="about-association-arrays"></a>À propos des tableaux d’association

Un tableau d’associations est une liste ordonnée d’emplacements de Registre qui contiennent des informations sur un type d’élément, y compris les gestionnaires, les verbes et d’autres attributs tels que l’icône et le nom d’affichage du type. Ces informations sur le type d’élément peuvent être enregistrées à différents niveaux de spécificité. Par exemple, vous pouvez inscrire un verbe qui s’affichera uniquement pour un type de fichier spécifique (tel que .jpg) ou pour tous les éléments ayant le même System. Kind (par exemple, System. Kind = image) ou pour tous les éléments.

L’interpréteur de commandes utilise des tableaux d’association pour interroger un ensemble prédéfini d’emplacements du Registre susceptibles de contenir des informations sur l’élément. Les API de tableau d’association peuvent être utilisées pour extraire de la sous-clé de Registre une valeur unique qui contient les informations demandées, avec cette valeur provenant de la première entrée du tableau qui le fournit. Par exemple, la valeur de l’icône par défaut est Récupérée de cette façon. Le tableau d’association peut également être utilisé pour récupérer un ensemble de valeurs stockées dans les sous-clés du Registre. Par exemple, la liste de verbes est créée à partir de ces verbes inscrits sous toutes les sous-clés.

Une fois que l’interpréteur de commandes a retenu un ensemble prédéfini d’emplacements de Registre pour obtenir des informations sur un élément de Shell, il place les emplacements du Registre dans un tableau dans l’ordre de l’emplacement le plus spécifique au plus général.

Étant donné que les tableaux d’association sont des listes triées, ils fournissent aux développeurs d’applications un mécanisme permettant d’ajouter des informations au registre qui seront retournées pour un type d’élément spécifique. De même, les tableaux d’association permettent aux développeurs d’applications d’ajouter des informations au registre pour un groupe spécifique d’éléments lorsque ces éléments sont inscrits à un emplacement plus général. Cette logique informe votre décision sur l’emplacement le plus approprié dans le registre pour stocker des informations sur les éléments de l’interpréteur de commandes.

sur un système Windows par défaut, un fichier .jpg contient le tableau d’association suivant :

-   **HKEY \_ Jpgfile \_ racine des classes** \\ 
-   **HKEY \_ CLASSES \_ racine** \\ **SystemFileAssociations** \\ **.jpg**
-   **HKEY \_ Image \_ racine des classes** \\ 
-   **\_racine des classes HKEY \_**\\**\***
-   **HKEY \_ AllFilesystemObjects \_ racine des classes** \\ 

Pour plus d’informations sur l’inscription des tableaux [d'](app-registration.md)Association, consultez inscription des applications.

## <a name="querying-association-arrays"></a>Interrogation des tableaux d’association

Il existe des API Shell permettant de récupérer des informations à partir d’une plage de sous-clés de Registre, de la sous-clé de registre la plus spécifique à un sur-ensemble des informations sur toutes les sous-clés du Registre.

L’utilisation la plus courante d’un tableau d’association consiste à interroger une valeur unique que l’interpréteur de commandes retourne à partir de l’élément le plus spécifique dans le tableau qui contient les informations demandées. L’exemple de code suivant montre comment procéder.


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



Les API suivantes peuvent être utilisées pour interroger un tableau d’association ou pour construire un objet [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de tableau d’association pouvant être interrogé :

-   [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (avant Windows Vista)
-   [**AssocCreateForClasses**](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a>Utilisation de tableaux d’association pour une source de données Shell particulière

Chaque source de données de Shell définit le tableau d’association pour ses éléments. La définition d’un tableau d’associations est généralement une fonction du type d’élément. Les implémenteurs de sources de données Shell doivent définir et documenter les tableaux d’association pour permettre aux applications d’étendre le comportement de ces types, par exemple pour inscrire des verbes ou d’autres informations. Les applications peuvent étendre le comportement des éléments en fonction de l’ajout de données aux sous-clés du tableau d’association, telles que l’ajout de verbes pour les éléments.

La source de données du système de fichiers crée un tableau d’association pour les fichiers basés sur les sous-clés de Registre suivantes et les ProgID spéciaux :

-   Si le fichier contient un ProgID enregistré, le ProgID **\_ \_ racine de la classe HKEY** \\  est utilisé. Sinon, la racine de la racine de la **\_ \_ classe HKEY** \\  est utilisée.
-   L’extension de nom de fichier est inscrite sous la **\_ \_** \\  \\ sous-clé SystemFileAssociations *. FileExtension* racine de la classe HKEY.
-   Les ProgID spéciaux sont répertoriés dans le tableau suivant. 

    | ProgID spécial                                    | Description                   |
    |---------------------------------------------------|-------------------------------|
    | **\_racine des classes HKEY \_**\\**\***                   | Tous les fichiers (sans dossiers)       |
    | **HKEY \_ AllFilesystemObjects \_ racine des classes** \\  | Fichiers et dossiers du système de fichiers |
    | **HKEY \_ Répertoire \_ racine des classes** \\             | Dossiers du système de fichiers           |
    | **HKEY \_ Dossier \_ racine des classes** \\                | Conteneurs de Shell              |

    

     

### <a name="shell-data-source-association-arrays"></a>Groupes d’associations de la source de données Shell

La liste suivante représente certains des tableaux d’association du magasin de données Shell qui peuvent être utilisés pour les opérations décrites dans cette rubrique :

-   **\_racine des classes HKEY \_**\\**\***
-   **HKEY \_ AllFilesystemObjects \_ racine des classes** \\ 
-   **HKEY \_ CLASSES \_ racine** \\ **Kind.Document**
-   **HKEY \_ Résultats des classes \_ racine** \\ 
-   **HKEY \_ CLASSES \_ racine** \\ **SystemFileAssociations** \\ **.docx**
-   **HKEY \_ CLASSES \_ racine** \\ **Word.Document. 12**

Les tableaux d’association de la source de données Shell qui peuvent être utilisés pour DBFolder (un magasin de données Shell qui représente des éléments dans les résultats de recherche et les vues basées sur des requêtes) sont les suivants :

-   Lecteurs
-   Réseau
-   RegItems
-   Exemples :
    -   ContentView
    -   Verbes

D’autres groupes d’associations communs incluent le dossier et les imprimantes.

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour créer un magasin de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](nse-implement.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription de l’application](app-registration.md)
</dt> <dt>

[Types de fichiers](fa-file-types.md)
</dt> <dt>

[Fonctionnement des associations de fichiers](fa-how-work.md)
</dt> <dt>

[Affichage du contenu par type de fichier ou par type](prophand-content-view.md)
</dt> <dt>

[Vérificateur de type de fichier](file-type-verifier.md)
</dt> <dt>

[Gestionnaires de types de fichiers](fa-file-extensions.md)
</dt> <dt>

[Identificateurs programmatiques](fa-progids.md)
</dt> <dt>

[Types perçus](fa-perceivedtypes.md)
</dt> </dl>

 

 
