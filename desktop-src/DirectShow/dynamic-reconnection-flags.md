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
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542312"
---
# <a name="dynamic-reconnection-flags"></a>Indicateurs de reconnexion dynamique

\[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

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

 

 




