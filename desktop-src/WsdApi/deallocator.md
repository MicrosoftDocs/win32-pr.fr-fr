---
description: Spécifie le type de annulateur à utiliser par une fonction stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: élément annulateur
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e9a27f768d0c9d854d13bd58c0c797234a0526c4abb95a0c5f4fb553466a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991749"
---
# <a name="deallocator-element"></a>élément annulateur

Spécifie le type de annulateur à utiliser par une fonction stub.

## <a name="usage"></a>Usage

``` syntax
<deallocator/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                               | Description                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**stubDefinitions**](stubdefinitions.md)<br/> | Génère des implémentations pour les fonctions stub pour les opérations de type de port.<br/> <br/> |



## <a name="remarks"></a>Remarques

Le type annulateur doit être placé dans une paire de <deallocator></deallocator> balises. Les chaînes suivantes sont des valeurs annulateur valides :

-   aucun
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   gratuit
-   supprimer
-   deleteArray
-   Libérer

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




