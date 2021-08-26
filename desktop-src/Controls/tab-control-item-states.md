---
title: États des éléments de contrôle d’onglet (CommCtrl. h)
description: Les éléments de contrôle d’onglet prennent désormais en charge l’état d’un élément pour prendre en charge le \_ message DESELECTALL TCM. En outre, la structure TCITEM prend en charge les valeurs d’état des éléments.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75f3bba0ecd29c7ab84c6b68010f8af52c8db2cfc9dc4080fb73e37b408ee1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919279"
---
# <a name="tab-control-item-states"></a>États des éléments de contrôle d’onglet

Les éléments de contrôle d’onglet prennent désormais en charge l’état d’un élément pour prendre en charge le message [**\_ DESELECTALL TCM**](tcm-deselectall.md) . En outre, la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) prend en charge les valeurs d’état des éléments.



| Constante                                                                                                                                                                     | Description                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**TCIS \_ BUTTONPRESSED**</dt> </dl> | [Version 4,70](common-control-versions.md). L’élément de contrôle onglet est sélectionné. Cet État est significatif uniquement si l’indicateur de style de [**\_ boutons TCS**](tab-control-styles.md) a été défini.<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS \_ mis en surbrillance**</dt> </dl>       | [Version 4,71](common-control-versions.md). L’élément de contrôle d’onglet est mis en surbrillance, et l’onglet et le texte sont dessinés à l’aide de la couleur de surbrillance actuelle. Si vous utilisez 65536 couleurs, il s’agit d’une véritable interpolation, et non d’une couleur dépendante.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





