---
description: Spécifie le type annulateur à utiliser par une fonction stub d’opérations.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: élément operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522704"
---
# <a name="operationdeallocator-element"></a>élément operationDeallocator

Spécifie le type annulateur à utiliser par la fonction stub d’une opération.

## <a name="usage"></a>Utilisation

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a>Attributs



| Attribut                  | Type                         | Obligatoire       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **annulateur**<br/> | chaîne de caractères \_<br/> | Oui<br/> | Annulateur à utiliser pour l’opération.<br/> <br/> Les chaînes suivantes sont des valeurs valides.<br/> <br/> <dl><span id="none"></span><span id="NONE"></span>* * * * <dt>aucun *</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> * * * * * * * * <dt>WSDFreeLinkedMemory * *</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> * * * * * * * * * * * * <dt>CoTaskMemFree * *</dt> <span id="free"></span> <span id="FREE"></span> * * * * * * <dt>gratuit * *</dt> <span id="delete"></span> <span id="DELETE"></span> * * * * * * <dt>supprimer *</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> * * * * * * * <dt>deleteArray * *</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> * * * * * * * * * * * * <dt>Version *</dt> * * * </dl> |
| **opération**<br/>   | chaîne de caractères \_<br/> | Oui<br/> | Nom de l'opération.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                               | Description                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Génère des implémentations pour les fonctions stub pour les opérations de type de port.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




