---
description: Si le bit de contrôle visible est défini, le contrôle est visible dans la boîte de dialogue. Si ce bit n’est pas défini, le contrôle est masqué dans la boîte de dialogue. L’état visible ou masqué de l’attribut de contrôle visible peut être modifié ultérieurement par un événement de contrôle.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Attribut de contrôle visible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512955"
---
# <a name="visible-control-attribute"></a>Attribut de contrôle visible

Si le bit de contrôle visible est défini, le contrôle est visible dans la boîte de dialogue. Si ce bit n’est pas défini, le contrôle est masqué dans la boîte de dialogue. L’état visible ou masqué de l’attribut de contrôle visible peut être modifié ultérieurement par un [événement de contrôle](control-events.md).

## <a name="valid-controls"></a>Contrôles valides

Tous les contrôles.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                          |
|---------|-------------|-----------------------------------|
| 1       | 0x00000001  | **msidbControlAttributesVisible** |



 

## <a name="remarks"></a>Notes

Vous pouvez utiliser la [table ControlCondition](controlcondition-table.md) pour afficher ou masquer un contrôle en fonction de la valeur d’une propriété ou d’une instruction conditionnelle. Vous pouvez également afficher ou masquer un contrôle en abonnant le contrôle à un [ControlEvent,](control-events.md). Entrez l’identificateur de l’attribut dans la colonne d’attribut et l’identificateur de l’événement dans la colonne d’événement de la [table EventMapping](eventmapping-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



