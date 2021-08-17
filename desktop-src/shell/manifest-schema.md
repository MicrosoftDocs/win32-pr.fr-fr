---
description: Ces éléments composent le schéma XML utilisé dans le manifeste de transfert de l’Assistant de publication Web et de commandes d’impression en ligne.
title: Schéma de manifeste de transfert
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 30324e32e1bd841423318a37eb1472d673ffc53c6e745f54f9398cec73138239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858855"
---
# <a name="transfer-manifest-schema"></a>Schéma de manifeste de transfert

Ces éléments composent le schéma XML utilisé dans le manifeste de transfert de l’Assistant de publication Web et de commandes d’impression en ligne.

Les éléments suivants sont définis pour le manifeste de transfert.

-   [cancelledpage](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [failurepage](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [passion](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [file](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [filelist](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [Répertoire](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [folderlist](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [formdata](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [htmlui](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [imageproperty](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [métadonnées](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [emplacement](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [Publier](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [redimensionner](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [successpage](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [cible](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [transfermanifest](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)
-   [uploadinfo](#syntax)
    -   [Syntaxe](#syntax)
    -   [Attributs](#attributes)
    -   [Informations sur les éléments](#element-information)

## <a name="cancelledpage"></a>cancelledpage

Spécifie la page HTML côté serveur à afficher avant la fermeture de l’Assistant lorsque l’utilisateur clique sur le bouton **Annuler** .

### <a name="syntax"></a>Syntaxe


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| href      | Obligatoire. URL de la page HTML côté serveur à afficher lorsque l’utilisateur clique sur le bouton **Annuler** . |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent        | Éléments enfants |
|-----------------------|----------------|
| [uploadinfo](#syntax) | Aucun           |



 

## <a name="failurepage"></a>failurepage

Spécifie la page HTML côté serveur à afficher si le chargement échoue.

### <a name="syntax"></a>Syntaxe


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| href      | Obligatoire. URL de la page HTML côté serveur à afficher si le chargement échoue. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent        | Éléments enfants         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Aucun. Le texte est autorisé. |



 

## <a name="favorite"></a>passion

Indique à l’Assistant de créer une entrée de site Web favori dans le menu **favoris** pour l’URL donnée. Si cet élément n’est pas spécifié, l’élément [htmlui](#syntax) est utilisé à la place.

### <a name="syntax"></a>Syntaxe


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                            |
|-----------|------------------------------------------------------------------------|
| comment   | Obligatoire. Commentaire associé à l’entrée **favoris** .         |
| href      | Obligatoire. URL de l’entrée **favoris** .                          |
| name      | Obligatoire. Nom de l’URL qui s’affiche dans le menu **favoris** . |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent        | Éléments enfants         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Aucun. Le texte est autorisé. |



 

## <a name="file"></a>fichier

Décrit un fichier unique à copier. Plusieurs éléments de [fichier](#syntax) peuvent être contenus sous un seul nœud [filelist](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a>Attributs



| Attribut   | Description                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indiquez | Facultatif. Type MIME du fichier.                                                                                                                                         |
| destination | Obligatoire. Chemin d’accès suggéré pour le fichier une fois qu’il a été téléchargé. Ce chemin d’accès est relatif à l’URL de destination du site de téléchargement. Le site de chargement peut modifier cette valeur si nécessaire. |
| extension   | Facultatif. Extension de nom de fichier du fichier.                                                                                                                               |
| id          | Obligatoire. Index numérique du fichier.                                                                                                                                   |
| taille        | Facultatif. Taille du fichier, en octets.                                                                                                                                    |
| source      | Obligatoire. Chemin d’accès complet du système de fichiers pour le fichier.                                                                                                                            |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent      | Éléments enfants                                          |
|---------------------|---------------------------------------------------------|
| [filelist](#syntax) | [métadonnées](#syntax), [publication](#syntax), [redimensionnement](#syntax) |



 

## <a name="filelist"></a>filelist

Conteneur pour les éléments décrivant les fichiers à copier. Plusieurs éléments [filelist](#syntax) peuvent être contenus sous un seul nœud [transfermanifest](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a>Attributs



| Attribut   | Description      |
|-------------|------------------|
| usesfolders | Non implémenté. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent              | Éléments enfants  |
|-----------------------------|-----------------|
| [transfermanifest](#syntax) | [file](#syntax) |



 

## <a name="folder"></a>dossier

Décrit un dossier dans lequel les fichiers sont stockés. Plusieurs éléments de [dossier](#syntax) peuvent être contenus sous un seul nœud [folderlist](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a>Attributs



| Attribut   | Description                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination | Obligatoire. Chemin d’accès suggéré pour le dossier une fois téléchargé. Ce chemin d’accès est relatif à l’URL de destination du site de téléchargement. Le site de chargement peut modifier cette valeur si nécessaire. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent        | Éléments enfants |
|-----------------------|----------------|
| [folderlist](#syntax) | Aucun           |



 

## <a name="folderlist"></a>folderlist

Conteneur pour les éléments décrivant les fichiers à copier. Plusieurs éléments [folderlist](#syntax) peuvent être contenus sous un seul nœud [transfermanifest](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a>Attributs

Aucun.

### <a name="element-information"></a>Informations sur les éléments



| Élément parent              | Éléments enfants    |
|-----------------------------|-------------------|
| [transfermanifest](#syntax) | [Répertoire](#syntax) |



 

## <a name="formdata"></a>formdata

Décrit les données de formulaire encodées en HTML facultatives qui peuvent être transférées avec les fichiers. Cet élément est ajouté par le service s’il choisit de télécharger les fichiers en tant que publication en plusieurs parties. Les données de formulaire, ainsi que les informations de l’élément de [publication](#syntax) , sont utilisées pour créer l’en-tête de publication.

Plusieurs éléments [FormData](#syntax) peuvent être contenus sous un seul nœud [uploadinfo](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                                      |
|-----------|----------------------------------------------------------------------------------|
| name      | Obligatoire. Définit le nom des données de formulaire associé à cette section du téléchargement. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent        | Éléments enfants |
|-----------------------|----------------|
| [uploadinfo](#syntax) | Aucun           |



 

## <a name="htmlui"></a>htmlui

URL de la page HTML côté serveur à afficher lorsque l’Assistant est fermé. Cet élément crée une entrée de page Web favorite dans le menu **favoris** si l’élément [favori](#syntax) est absent et que le nom convivial du site de chargement est spécifié.

### <a name="syntax"></a>Syntaxe


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| href      | Obligatoire. URL de la page HTML côté serveur à afficher lorsque l’Assistant est fermé. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent        | Éléments enfants         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Aucun. Le texte est autorisé. |



 

## <a name="imageproperty"></a>imageproperty

Spécifie une propriété d’image relative au fichier. Plusieurs éléments [ImageProperty](#syntax) peuvent être contenus sous un seul nœud de [métadonnées](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                  |
|-----------|----------------------------------------------|
| id        | Obligatoire. ID de la propriété particulière. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent      | Éléments enfants         |
|---------------------|------------------------|
| [métadonnées](#syntax) | Aucun. Le texte est autorisé. |



 

## <a name="metadata"></a>metadata

Conteneur pour les éléments et le texte définissant les métadonnées pour le fichier particulier. Plusieurs éléments de [métadonnées](#syntax) peuvent être contenus sous un seul nœud de [fichier](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a>Attributs

Aucun.

### <a name="element-information"></a>Informations sur les éléments



| Élément parent  | Éléments enfants           |
|-----------------|--------------------------|
| [file](#syntax) | [imageproperty](#syntax) |



 

## <a name="netplace"></a>emplacement

Définit la cible d’un emplacement réseau créé dans favoris **réseau** lorsque le téléchargement est terminé. La création d’un emplacement réseau peut être évitée à l’aide de la méthode [**IPublishingWizard :: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .

### <a name="syntax"></a>Syntaxe


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| comment   | Obligatoire. Commentaire affiché pour l’icône d’emplacement réseau lorsque le curseur est placé sur celui-ci.         |
| href      | Obligatoire. URL de l’entrée d’emplacement réseau.                                                   |
| name      | Obligatoire. Nom de l’icône d’emplacement réseau qui apparaît dans le dossier **Favoris réseau** . |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent        | Éléments enfants         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Aucun. Le texte est autorisé. |



 

## <a name="post"></a>post

URL vers laquelle le fichier doit être publié. Cet élément est ajouté par le service lorsque le transfert est effectué sous la forme d’une publication en plusieurs parties et, avec [FormData](#syntax), est utilisé pour générer l’en-tête de publication. Si le service choisit d’effectuer le transfert de fichiers à l’aide d’World Wide Web Distributed Creation and Versioning (WebDAV), il ne doit pas ajouter cet élément. Plusieurs éléments de [publication](#syntax) peuvent être contenus sous un seul nœud de [fichier](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                                    |
|-----------|--------------------------------------------------------------------------------|
| nom_fichier  | Facultatif. Nom de fichier du fichier publié.                                   |
| href      | Obligatoire. URL du dossier de destination.                                   |
| name      | Obligatoire. Définit le nom des données de formulaire associé à cette section de la publication. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent  | Éléments enfants      |
|-----------------|---------------------|
| [file](#syntax) | [formdata](#syntax) |



 

## <a name="resize"></a>resize

Définit la mise à l’échelle et la recompression d’un fichier image au format JPEG. Si le fichier source est déjà au format JPEG et qu’il est inférieur ou égal à la largeur et à la hauteur spécifiées, il n’est pas dimensionné. Si le fichier source n’est pas un fichier JPEG, il est converti. La mise à l’échelle, la recompression et la conversion du fichier peuvent être évitées à l’aide de la méthode [**IPublishingWizard :: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) . Plusieurs éléments de [redimensionnement](#syntax) peuvent être contenus sous un seul nœud de [fichier](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| adéquat        | Obligatoire. Largeur de l’image, en pixels, après le chargement. Si cette valeur est égale à 0, **CX** est calculé à partir de la valeur **CY** pour conserver les dimensions relatives.  |
| cy        | Obligatoire. Hauteur de l’image, en pixels, après le chargement. Si cette valeur est 0, **ca** est calculé à partir de la valeur **CX** pour conserver les dimensions relatives. |
| qualité   | Obligatoire. Valeur de qualité JPEG, comprise entre 0 et 100, avec 100 de qualité supérieure.                                                                            |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent  | Éléments enfants |
|-----------------|----------------|
| [file](#syntax) | Aucun.          |



 

## <a name="successpage"></a>successpage

Spécifie la page HTML côté serveur à afficher si le chargement a réussi.

### <a name="syntax"></a>Syntaxe


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| href      | Obligatoire. URL de la page HTML côté serveur à afficher si le chargement a réussi. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent        | Éléments enfants         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Aucun. Le texte est autorisé. |



 

## <a name="target"></a>target

Un dossier de destination spécifié au format UNC (Universal Naming Convention) ou en tant que serveur WebDAV. Le service ajoute cette cible pour spécifier un dossier de destination si le transfert utilise un protocole WebDAV ou le protocole de système de fichiers. Si le service choisit d’effectuer le transfert de fichiers en tant que publication en plusieurs parties, il ne doit pas ajouter cet élément.

### <a name="syntax"></a>Syntaxe


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a>Attributs



| Attribut | Description                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| href      | Obligatoire. URL du dossier de destination. Utilisez le formulaire **https://** pour WebDAV ou le formulaire de **\\ \\ \\ partage de serveur** pour UNC. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent        | Éléments enfants         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Aucun. Le texte est autorisé. |



 

## <a name="transfermanifest"></a>transfermanifest

Nœud parent du fichier de manifeste de transfert.

### <a name="syntax"></a>Syntaxe


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a>Attributs

Aucun.

### <a name="element-information"></a>Informations sur les éléments



| Élément parent | Éléments enfants                                                    |
|----------------|-------------------------------------------------------------------|
| None           | [filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax) |



 

## <a name="uploadinfo"></a>uploadinfo

Conteneur pour les éléments fournissant des informations à partir du site de chargement utilisé dans la transaction. Plusieurs éléments [uploadinfo](#syntax) peuvent être contenus sous un seul nœud [transfermanifest](#syntax) .

### <a name="syntax"></a>Syntaxe


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a>Attributs



| Attribut    | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| convivial | Obligatoire. Nom convivial du site Web qui s’affiche dans l’Assistant. |



 

### <a name="element-information"></a>Informations sur les éléments



| Élément parent              | Éléments enfants                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transfermanifest](#syntax) | [cancelledpage](#syntax), [failurepage](#syntax), [favori](#syntax), [htmlui](#syntax), [netplace](#syntax), [SuccessPage](#syntax), [cible](#syntax) |



 

 

 



