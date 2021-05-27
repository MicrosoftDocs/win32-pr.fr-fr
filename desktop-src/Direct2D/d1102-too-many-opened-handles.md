---
title: D1102 trop de handles ouverts
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Un grand nombre d’interfaces qui n’ont pas été publiées ont été trouvées. Actuellement, il existe des interfaces non libérées allouées par cette DLL.
keywords:
- D1102 trop grand nombre de handles ouverts Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548684"
---
# <a name="d1102-too-many-opened-handles"></a>D1102 : trop de handles ouverts

Un grand nombre d’interfaces qui n’ont pas été publiées ont été trouvées. Actuellement, il \[ *existe des* \] interfaces non libérées allouées par cette dll.

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*certain*
</dt> <dd>

Nombre d’interfaces non libérées allouées par cette DLL.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Niveau d’erreur | Avertissement |



 

## <a name="possible-causes"></a>Causes possibles

Un grand nombre de ressources ont été créées. Bien que Direct2D n’ait aucune limite supérieure quant au nombre de ressources disponibles (à l’exception de la mémoire), la couche de débogage émet ce message d’information lorsqu’il rencontre des objets actifs 1001, des objets en direct 2001, ou 3001 des objets actifs, etc. en effet, cela peut indiquer une fuite dans l’application.

 

 




