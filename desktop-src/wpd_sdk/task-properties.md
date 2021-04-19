---
description: Appareils mobiles Windows prend en charge les propriétés de tâche suivantes.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Propriétés de la tâche (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539186"
---
# <a name="task-properties"></a>Propriétés de la tâche

Appareils mobiles Windows prend en charge les propriétés de tâche suivantes.



| Propriété                         | VarType        | Description                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| **propriétaire de la \_ tâche wpd \_**             | **\_LPWStr VT** | Propriétaire de la tâche.                                                                      |
| **pourcentage d’achèvement de la \_ tâche wpd \_ \_** | **VT \_ UI4**    | Nombre compris entre 0 et 100 qui spécifie le mode de réalisation de la tâche.                         |
| **Date du rappel de la \_ tâche wpd \_ \_**    | **\_Date VT**   | Valeur qui spécifie quand un rappel doit être envoyé pour effectuer la tâche, si elle n’est pas terminée. |
| **État de la \_ tâche wpd \_**            | **\_LPWStr VT** | Description de la chaîne de l’état de la tâche, par exemple, « en cours ».                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




