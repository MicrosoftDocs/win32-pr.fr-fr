---
description: Les fichiers de description de bibliothèque sont des fichiers XML qui définissent des bibliothèques.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Schéma de description de la bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfbaa8401468a6bab79cf4bccc5d7d4cd0ff7bb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879645"
---
# <a name="library-description-schema"></a>Schéma de description de la bibliothèque

Les fichiers de description de bibliothèque sont des fichiers XML qui définissent des bibliothèques. les bibliothèques regroupent les éléments des emplacements de stockage locaux et distants dans un affichage unique dans Windows Explorer. Les fichiers de description de la bibliothèque suivent le schéma de description de la bibliothèque et sont enregistrés en tant que \* fichiers. Library-ms.

Cette rubrique contient les sections suivantes :

-   [Vue d’ensemble du schéma de description de la bibliothèque](#overview-of-the-library-description-schema)
-   [Contrôle de version des espaces de noms](#namespace-versioning)
-   [Exemple de fichier de description de bibliothèque](#example-of-a-library-description-file)
-   [Rubriques connexes](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>Vue d’ensemble du schéma de description de la bibliothèque

Les bibliothèques contiennent des fichiers stockés dans un ou plusieurs emplacements de stockage. Les bibliothèques ne stockent pas réellement ces fichiers ; au lieu de cela, ils surveillent les dossiers qui contiennent les fichiers et permettent aux utilisateurs d’accéder aux fichiers et de les organiser de différentes façons. Par exemple, un utilisateur peut avoir des fichiers musicaux dans plusieurs dossiers sur un disque dur local et également sur un disque dur externe. à l’aide de la **bibliothèque de Musique**, l’utilisateur peut accéder à tous ces fichiers en même temps et les trier par nom d’artiste ou titre d’album en tant que groupe unique.

Le schéma de description de la bibliothèque se compose de trois parties majeures, décrites dans le tableau suivant :



| Partie                        | Description                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informations générales sur la bibliothèque | informations sur la bibliothèque, telles que le nom, le propriétaire, la version, l’icône, que Windows explorateur peut utiliser lorsqu’il affiche la bibliothèque à un utilisateur.                   |
| Propriétés de la bibliothèque          | Une ou plusieurs propriétés qui décrivent la bibliothèque. Ces propriétés personnalisées sont spécifiques à la bibliothèque.                                                     |
| Emplacements de bibliothèque           | Un ou plusieurs connecteurs de recherche qui identifient les emplacements de stockage à inclure dans la bibliothèque. Chacun de ces emplacements peut également avoir un ensemble unique de propriétés. |



 

les fichiers de bibliothèque dans Windows 7 sont stockés dans le dossier connu, FOLDERID \_ libraries. par défaut, le \_ dossier FOLDERID libraries se trouve dans% USERPROFILE% \\ AppData \\ roaming \\ Microsoft \\ Windows \\ libraries.

## <a name="namespace-versioning"></a>Contrôle de version des espaces de noms

Les versions du format de fichier de description de la bibliothèque ( \* . Library-ms) sont suivies en modifiant l’espace de noms. pour Windows 7, le format de fichier est l’espace de noms par défaut suivant : https://schemas.microsoft.com/windows/2009/library .

Toutefois, les versions du contenu de la bibliothèque sont suivies à l’aide de l’élément [ &lt; version &gt; ](schema-library-version.md) dans un fichier de description de bibliothèque spécifique.

## <a name="example-of-a-library-description-file"></a>Exemple de fichier de description de bibliothèque

Voici un exemple de fichier de description de bibliothèque qui définit une bibliothèque pour les fichiers de document.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Élément folderType (schéma de bibliothèque)](schema-library-foldertype.md)
</dt> <dt>

[Élément iconReference (schéma de bibliothèque)](schema-library-iconreference.md)
</dt> <dt>

[Élément isLibraryPinned (schéma de bibliothèque)](schema-library-islibrarypinned.md)
</dt> <dt>

[Élément libraryDescription (schéma de bibliothèque)](schema-librarydescription.md)
</dt> <dt>

[Élément Name (schéma de bibliothèque)](schema-library-name.md)
</dt> <dt>

[Élément ownerSID (schéma de bibliothèque)](schema-library-ownersid.md)
</dt> <dt>

[Property, élément (schéma de bibliothèque)](schema-library-property.md)
</dt> <dt>

[Élément propertyStore (schéma de bibliothèque)](schema-library-propertystore.md)
</dt> <dt>

[Élément searchConnectorDescription (schéma de bibliothèque)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Élément searchConnectorDescriptionList (schéma de bibliothèque)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Élément templateInfo (schéma de bibliothèque)](schema-library-templateinfo.md)
</dt> <dt>

[version, élément (schéma de bibliothèque)](schema-library-version.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
