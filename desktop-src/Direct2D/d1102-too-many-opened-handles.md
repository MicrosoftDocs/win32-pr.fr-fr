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
ms.openlocfilehash: baaa4c46850919aed50897583bfa68c9003bcf496ad884c68cfb57d3e8a90147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666350"
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

 

 




