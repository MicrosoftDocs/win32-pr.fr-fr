---
description: Les périphériques d’entrée utilisateur sont représentés par ces classes. Une machine virtuelle est toujours associée à une instance de chaque classe.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Classes d’entrée
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519594"
---
# <a name="input-classes"></a>Classes d’entrée

Les périphériques d’entrée utilisateur sont représentés par ces classes. Une machine virtuelle est toujours associée à une instance de chaque classe. Ces appareils ne peuvent pas être ajoutés ou supprimés de la machine virtuelle. Par conséquent, il n’existe aucune instance de pool de ressources pour les périphériques clavier ou souris.

Les périphériques clavier et souris sont liés à l’ordinateur virtuel via l’Association [**MSVM \_ SystemDevice**](msvm-systemdevice.md) . Un ordinateur virtuel contient à la fois un périphérique PS2 et un périphérique de souris synthétique. Un seul périphérique de pointage est actif à la fois.

Voici les classes WMI de virtualisation associées à l’entrée.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                          | Description                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [**\_Clavier MSVM**](msvm-keyboard.md)<br/>             | Représente un périphérique clavier.<br/>        |
| [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md)<br/>             | Représente un périphérique de souris PS2.<br/>       |
| [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md)<br/> | Représente un périphérique de souris synthétique.<br/> |



 

 

 




