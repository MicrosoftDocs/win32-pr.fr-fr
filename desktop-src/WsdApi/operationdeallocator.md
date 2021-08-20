---
description: Spécifie le type annulateur à utiliser par une fonction stub d’opérations.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: élément operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ce2902bbfac16cb096da334cf3f22a12c68e3720d575fa303b8f3b133c9328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991689"
---
# <a name="operationdeallocator-element"></a>élément operationDeallocator

Spécifie le type annulateur à utiliser par la fonction stub d’une opération.

## <a name="usage"></a>Usage

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



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




