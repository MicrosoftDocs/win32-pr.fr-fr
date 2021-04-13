---
description: Spécifie le type de annulateur à utiliser par une fonction stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: élément annulateur
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202272"
---
# <a name="deallocator-element"></a>élément annulateur

Spécifie le type de annulateur à utiliser par une fonction stub.

## <a name="usage"></a>Utilisation

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



## <a name="remarks"></a>Notes

Le type annulateur doit être placé dans une paire de <deallocator></deallocator> balises. Les chaînes suivantes sont des valeurs annulateur valides :

-   aucun
-   WSDFreeLinkedMemory
-   CoTaskMemFree
-   gratuit
-   supprimer
-   deleteArray
-   Libérer

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




