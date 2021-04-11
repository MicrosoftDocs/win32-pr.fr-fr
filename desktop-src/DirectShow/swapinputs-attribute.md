---
description: L’attribut swapinputs spécifie s’il faut échanger les entrées de transition. Si la valeur est TRUE, les entrées sont échangées. La valeur par défaut est FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Attribut swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320602"
---
# <a name="swapinputs-attribute"></a>Attribut swapinputs

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `swapinputs` attribut spécifie s’il faut échanger les entrées de transition. Si la valeur est **true**, les entrées sont échangées. La valeur par défaut est **FALSE**.

## <a name="possible-values"></a>Valeurs possibles

Les valeurs suivantes sont définies sur TRUE : y, Y, t, T, 1. Les valeurs suivantes sont définies avec la valeur FALSe : n, N, f, F, 0 (zéro).

## <a name="applies-to"></a>S'applique à

[**passe**](transition-element.md)

## <a name="remarks"></a>Notes

Par défaut, une transition se poursuit à partir du composite de toutes les couches de faible priorité vers la couche sur laquelle la transition réside. Si l' `swapinputs` attribut est 1, cette direction est inversée. Pour plus d’informations sur le modèle de structuration en couches utilisé par DES, consultez [le modèle de chronologie](the-timeline-model.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



