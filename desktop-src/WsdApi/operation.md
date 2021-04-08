---
description: Spécifie une opération pour laquelle du code doit être généré.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: Operation, élément
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034302"
---
# <a name="operation-element"></a>Operation, élément

Spécifie une opération pour laquelle du code doit être généré.

## <a name="usage"></a>Utilisation

``` syntax
<operation/>
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

Il est possible de spécifier un nombre quelconque d’opérations. Si aucune opération n’est spécifiée, du code est généré pour toutes les opérations dans tous les types de port appropriés. L’utilisation de l’élément **operation** limite les méthodes générées à celles contenues dans l’opération.

Par exemple, une imprimante prend en charge ces opérations entre autres :

-   **PrintJobByPost**
-   **PrintJobByReference**
-   **CancelJob**
-   **GetJobElements**
-   **GetActiveJobs**
-   **GetJobHistory**
-   **SubscribeToPrinterConfigChange**
-   **UnsubscribeToPrinterConfigChange**

Toutefois, pour inclure uniquement les méthodes liées aux opérations **PrintJobByPost** et **GetJobElements** , le script de génération de code utilisera les éléments [**idlFunctionDeclarations**](idlfunctiondeclarations.md) comme suit :

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

Cela génère des déclarations de fonction idl pour toutes les méthodes associées aux deux opérations (par exemple, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** et **EndGetJobElements**).

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




