---
description: La propriété DisableAutoMouseProcessing active ou désactive la fonctionnalité de traitement de la souris de l’objet MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Propriété DisableAutoMouseProcessing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9728f968e1ce562bc8cc643b5c27b8ac2ace3db1b2d39c45a8ae1fa78b44971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749149"
---
# <a name="disableautomouseprocessing-property"></a>Propriété DisableAutoMouseProcessing

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DisableAutoMouseProcessing` propriété active ou désactive la fonctionnalité de traitement de la souris de l’objet **mswebdvd** .

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant s’il faut désactiver le traitement par défaut de la souris.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture et sa valeur par défaut est false. L’objet **mswebdvd** gère automatiquement les actions de la souris pour les menus sur écran de DVD par défaut ; les utilisateurs peuvent mettre en surbrillance et activer des boutons de menu sans programmation particulière par l’application. Une application peut désactiver cette fonctionnalité de gestion de la souris par défaut en affectant à cette propriété la **valeur true**. Lorsque le traitement automatique de la souris est désactivé, une application doit utiliser les différentes méthodes et propriétés liées aux boutons pour gérer les déplacements de la souris et les clics de souris dans les menus à l’écran. En outre, une application peut utiliser les méthodes associées à un bouton pour remplacer la gestion automatique de la souris même lorsque when `DisableAutoMouseProcessing` a la valeur **false**.

 

 



