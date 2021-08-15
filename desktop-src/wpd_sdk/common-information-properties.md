---
description: Windows Les appareils mobiles prennent en charge les propriétés d’informations courantes suivantes.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Propriétés des informations communes (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41a8845a41714ed1a775d19e14f0996aad698aaf99de18da4eceb4df92688409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431102"
---
# <a name="common-information-properties"></a>Propriétés des informations communes

Windows Les appareils mobiles prennent en charge les propriétés d’informations courantes suivantes.



| Propriété                                      | VarType        | Description                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **\_Notes d' \_ informations \_ communes wpd**           | **\_LPWStr VT** | Pour les rendez-vous, les tâches et les objets similaires, cette propriété contient toutes les remarques relatives à l’objet donné.     |
| **\_objet d' \_ informations \_ communes wpd**         | **\_LPWStr VT** | Valeur qui spécifie le champ objet de cet objet.                                                 |
| **\_ \_ \_ texte du corps d’informations communes wpd \_**      | **\_LPWStr VT** | Cette propriété contient le texte du corps d’un objet, en texte brut ou au format HTML.                          |
| **\_priorité des \_ informations \_ communes wpd**        | **VT \_ UI4**    | Valeur qui spécifie la priorité de cet objet. 0 indique la priorité la plus élevée.                    |
| **\_date et \_ \_ heure de début des informations communes wpd \_** | **\_Date VT**   | Valeur qui spécifie la date/l’heure de début planifiée d’un rendez-vous, d’une tâche ou d’un objet similaire. |
| **\_date et \_ \_ heure de fin des informations communes wpd \_**   | **\_Date VT**   | Valeur qui spécifie la date/l’heure de fin planifiée d’un rendez-vous, d’une tâche ou d’un objet similaire.   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




