---
description: Indique au générateur de code de générer un fichier et spécifie le nom du fichier de sortie.
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: file (élément)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41970da9cc6e389f4e45c5e55901ce8eb2e7797f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518044"
---
# <a name="file-element"></a>file (élément)

Indique au générateur de code de générer un fichier et spécifie le nom du fichier de sortie.

## <a name="usage"></a>Utilisation

``` syntax
<file
  name = "pathname string">
  child elements
</file>
```

## <a name="attributes"></a>Attributs



| Attribut           | Type                       | Obligatoire       | Description                                                                                                                         |
|---------------------|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **name**<br/> | chaîne du chemin d’accès<br/> | Oui<br/> | Nom de fichier de sortie pour le contenu généré. La chaîne de nom de fichier doit inclure des informations sur le chemin d’accès complet.<br/> <br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                 | Description                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CDATA**<br/>                                                                                    | Les sections Text et CDATA sont copiées dans le fichier sans modification. Le code source qui n’est pas une fonction des données d’entrée de contrat peut être ajouté aux fichiers de sortie à l’aide des sections Text et CDATA.<br/> <br/> |
| [**enumerationValueDeclarations**](enumerationvaluedeclarations.md)<br/>                         | Génère des déclarations C pour les valeurs de tous les types énumérés.<br/> <br/>                                                                                                                                   |
| [**eventSourceBuilderDeclarations**](eventsourcebuilderdeclarations.md)<br/>                     | Génère des déclarations pour les fonctions qui créent des classes de sources d’événements.<br/> <br/>                                                                                                                         |
| [**eventSourceBuilderImplementations**](eventsourcebuilderimplementations.md)<br/>               | Génère des fonctions qui créent des classes de sources d’événements.<br/> <br/>                                                                                                                                          |
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.<br/> <br/>                                                                                                            |
| [**hostBuilderDeclaration**](hostbuilderdeclaration.md)<br/>                                     | Génère une déclaration pour une fonction qui crée un hôte typé.<br/> <br/>                                                                                                                              |
| [**hostBuilderImplementation**](hostbuilderimplementation.md)<br/>                               | Génère une fonction qui crée un hôte typé.<br/> <br/>                                                                                                                                                |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.<br/> <br/>                                                                                                                       |
| [**inclusion**](include.md)<br/>                                                                   | Comprend le contenu d’une macro ou d’un fichier dans la sortie générée.<br/> <br/>                                                                                                                              |
| [**IUnknownDeclarations**](iunknowndeclarations.md)<br/>                                         | Génère des déclarations pour QueryInterface, AddRef et Release.<br/> <br/>                                                                                                                                 |
| [**IUnknownDefinitions**](iunknowndefinitions.md)<br/>                                           | Génère des implémentations pour QueryInterface, AddRef et Release.<br/> <br/>                                                                                                                              |
| [**literalInclude**](literalinclude.md)<br/>                                                     | Place une instruction include C ou IDL dans le code généré. <br/> <br/>                                                                                                                                    |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Génère des définitions de structure C pour les types de messages.<br/> <br/>                                                                                                                                           |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.<br/> <br/>                                                                                                                     |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Génère des constantes C pour les tables de schéma XML pour les types de messages.<br/> <br/>                                                                                                                                 |
| [**namespaceDeclarations**](namespacedeclarations.md)<br/>                                       | Génère des déclarations C pour les tables d’espaces de noms.<br/> <br/>                                                                                                                                                 |
| [**namespaceDefinitions**](namespacedefinitions.md)<br/>                                         | Génère des définitions C pour les tables d’espaces de noms.<br/> <br/>                                                                                                                                                  |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Génère des déclarations de constante C pour les types de port.<br/> <br/>                                                                                                                                              |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Génère des constantes C pour les types de ports.<br/> <br/>                                                                                                                                                          |
| [**proxyBuilderDeclarations**](proxybuilderdeclarations.md)<br/>                                 | Génère des déclarations pour les fonctions afin de créer des proxies typés.<br/> <br/>                                                                                                                                  |
| [**proxyBuilderImplementations**](proxybuilderimplementations.md)<br/>                           | Génère des fonctions pour créer des proxies typés.<br/> <br/>                                                                                                                                                   |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Génère des implémentations pour les fonctions proxy pour les opérations de type de port.<br/> <br/>                                                                                                                        |
| [**relationshipMetadataDeclaration**](relationshipmetadatadeclaration.md)<br/>                   | Génère une déclaration anticipée pour les métadonnées d’hébergement spécifiées dans l’élément [**hostMetadata**](hostmetadata.md) . <br/> <br/>                                                                       |
| [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md)<br/>                     | Génère une définition de constante C pour les métadonnées d’hébergement spécifiées dans l’élément [**hostMetadata**](hostmetadata.md) . <br/> <br/>                                                                     |
| [**structDeclarations**](structdeclarations.md)<br/>                                             | Génère des déclarations de structure C pour les types connus.<br/> <br/>                                                                                                                                            |
| [**structDefinitions**](structdefinitions.md)<br/>                                               | Génère des définitions de structure C pour les types connus.<br/> <br/>                                                                                                                                             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Génère des déclarations pour les fonctions stub pour les opérations de type de port.<br/> <br/>                                                                                                                            |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Génère des implémentations pour les fonctions stub pour les opérations de type de port.<br/> <br/>                                                                                                                         |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.<br/> <br/>                                                                         |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.<br/> <br/>                                                                                    |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.<br/> <br/>                                                                                     |
| **text**<br/>                                                                                     | Les sections Text et CDATA sont copiées dans le fichier sans modification. Le code source qui n’est pas une fonction des données d’entrée de contrat peut être ajouté aux fichiers de sortie à l’aide des sections Text et CDATA.<br/> <br/> |
| [**thisModelMetadataDeclaration**](thismodelmetadatadeclaration.md)<br/>                         | Génère une déclaration anticipée pour la constante C pour les métadonnées de fabricant spécifiées dans l’élément [**thisModelMetadata**](thismodelmetadata.md) .<br/> <br/>                                      |
| [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md)<br/>                           | Génère une constante C pour les métadonnées de fabricant spécifiées dans l’élément [**thisModelMetadata**](thismodelmetadata.md) .<br/> <br/>                                                                  |
| [**typeTableDeclarations**](typetabledeclarations.md)<br/>                                       | Génère des déclarations de constante C pour les tables de schéma XML pour les types connus.<br/> <br/>                                                                                                                       |
| [**typeTableDefinitions**](typetabledefinitions.md)<br/>                                         | Génère des constantes C pour les tables de schéma XML pour les types connus.<br/> <br/>                                                                                                                                   |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  text, 
  CDATA, 
  namespaceDeclarations*, 
  namespaceDefinitions*, 
  structDeclarations*, 
  structDefinitions*, 
  typeTableDeclarations*, 
  typeTableDefinitions*, 
  thisModelMetadataDeclaration*, 
  thisModelMetadataDefinition*, 
  portTypeDeclarations*, 
  portTypeDefinitions*, 
  messageStructureDefinitions*, 
  messageTypeDeclarations*, 
  messageTypeDefinitions*, 
  idlFunctionDeclarations*, 
  subscriptionIdlFunctionDeclarations*, 
  functionDeclarations*, 
  subscriptionFunctionDeclarations*, 
  proxyFunctionImplementations*, 
  subscriptionProxyFunctionImplementations*, 
  stubDeclarations*, 
  stubDefinitions*, 
  enumerationValueDeclarations*, 
  include*, 
  IUnknownDeclarations*, 
  IUnknownDefinitions*, 
  relationshipMetadataDeclaration*, 
  relationshipMetadataDefinition*, 
  proxyBuilderDeclarations*, 
  proxyBuilderImplementations*, 
  hostBuilderDeclaration*, 
  hostBuilderImplementation*, 
  eventSourceBuilderDeclarations*, 
  eventSourceBuilderImplementations*, 
  literalInclude*
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                                     | Description                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Élément racine d’un fichier de script XML du générateur de code WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Remarques

Le nom du fichier est déterminé par la valeur de l’attribut Name ou de l’élément enfant. Le contenu du fichier est déterminé par les autres éléments enfants, Text et CDATA dans l’élément **file** . Les textes et CDATA sont copiés dans le fichier sans être modifiés. Les éléments enfants sont remplacés par du code généré. Le texte, les CDATA et les éléments enfants peuvent se produire dans n’importe quel ordre et peuvent être répétés indéfiniment.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




