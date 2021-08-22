---
description: Les indicateurs suivants spécifient le niveau de reconnexion dynamique à utiliser pendant le rendu.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Indicateurs de reconnexion dynamique (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f7bd2ff28c0928c59c632df501e6545b50707cfd948dd57e4ff1bd1cf01d1721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966239"
---
# <a name="dynamic-reconnection-flags"></a>Indicateurs de reconnexion dynamique

\[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

Les indicateurs suivants spécifient le niveau de reconnexion dynamique à utiliser pendant le rendu.



| Constante/valeur                                                                                                                                                                                                                                            | Description                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_ DYNAMIQUE \_ aucun**</dt> <dt>0x00</dt> </dl>          | Aucune reconnexion dynamique. Chargez tout avant de restituer le projet.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_ \_Sources dynamiques**</dt> <dt>0x01</dt> </dl> | Chargez les sources uniquement si nécessaire.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_ \_Effets dynamiques**</dt> <dt>0x02</dt> </dl> | Réservé. Ne pas utiliser.<br/>                                                  |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




