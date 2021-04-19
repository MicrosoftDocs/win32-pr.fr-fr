---
description: Spécifie le type de port pour lequel le code doit être généré.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: élément portType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a466ccdcfda133a2a314609e9698cd37c6bf31c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519136"
---
# <a name="porttype-element"></a>élément portType

Spécifie le type de port pour lequel le code doit être généré.

## <a name="usage"></a>Utilisation

``` syntax
<portType/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                                                                 | Description                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.<br/> <br/>                                    |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.<br/> <br/>                                               |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Génère des définitions de structure C pour les types de messages.<br/> <br/>                                                                   |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.<br/> <br/>                                             |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Génère des constantes C pour les tables de schéma XML pour les types de messages.<br/> <br/>                                                         |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Génère des déclarations de constante C pour les types de port.<br/> <br/>                                                                      |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Génère des constantes C pour les types de ports.<br/> <br/>                                                                                  |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Génère des implémentations pour les fonctions proxy pour les opérations de type de port.<br/> <br/>                                                |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Génère des déclarations pour les fonctions stub pour les opérations de type de port.<br/> <br/>                                                    |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Génère des implémentations pour les fonctions stub pour les opérations de type de port.<br/> <br/>                                                 |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Génère des déclarations d’implémentation pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Génère des déclarations IDL pour les fonctions de proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Génère des implémentations pour les fonctions proxy d’abonnement/annulation d’abonnement pour les opérations de notification de type de port.<br/> <br/>             |



## <a name="remarks"></a>Notes

Par défaut, le code est généré pour tous les types de port dans les fichiers d’entrée WSDL.

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




