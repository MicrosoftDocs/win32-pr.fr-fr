---
description: Spécifie le type de annulateur à utiliser par une fonction stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: élément annulateur
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994936"
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



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




