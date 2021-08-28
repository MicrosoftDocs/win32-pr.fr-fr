---
description: Le contrôle Line est une ligne horizontale.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Contrôle Line
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb4dc02db9c701c0c5156a0e3f3e15a039893bae290fc7e8bee7dfce64f2eb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763489"
---
# <a name="line-control"></a>Contrôle Line

Le contrôle Line est une ligne horizontale.

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec ce contrôle. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                       | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md) |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la table de [contrôle](control-table.md) ou de la [table BBControl](bbcontrol-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                         |
| [Visible](visible-control-attribute.md)   | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs dans la table de [contrôle](control-table.md) ou la [table BBControl](bbcontrol-table.md) pour rendre le contrôle visible ou masqué lors de sa création.<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)     | 0x00000000 0x00000004<br/> | Affiche le style visuel par défaut. Affiche le contrôle avec une apparence 3D enfoncée.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Remarques

Ce contrôle peut être créé à partir de la classe statique à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Il a les styles **SS \_ ETCHEDHORZ** et **SS \_ 3D enfoncé** .

 

 
