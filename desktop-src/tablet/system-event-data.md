---
description: Contient des informations sur un événement du système de tablette.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: Structure SYSTEM_EVENT_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 58e153da2695990f74d1268aa3e861bb9011b108ebdd1ea2d5128ff6f8e40a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708209"
---
# <a name="system_event_data-structure"></a>Structure des données d' \_ événement système \_

Contient des informations sur un événement du système de tablette.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**bModifier**
</dt> <dd>

Valeurs de bit pour les modificateurs. Pour plus d’informations, consultez la section Notes.

</dd> <dt>

**wKey**
</dt> <dd>

Analyser le code du caractère de clavier.

</dd> <dt>

**xPos**
</dt> <dd>

Position X de l’événement.

</dd> <dt>

**PosY**
</dt> <dd>

Position Y de l’événement.

</dd> <dt>

**bCursorMode**
</dt> <dd>

Type de curseur qui a provoqué l’événement. Pour plus d’informations, consultez la section Notes.

</dd> <dt>

**dwButtonState**
</dt> <dd>

État des boutons au moment de l’événement système.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les événements système suivants sont définis pour être utilisés dans le membre **bModifier** .



| Valeur               | Description                  |
|---------------------|------------------------------|
| SE \_ MODIFICATeur \_ CTRL  | La touche de contrôle a été enfoncée. |
| SE \_ MODIFICATeur \_ ALT   | La touche Alt a été enfoncée.     |
| SE \_ MODIFIER le \_ décalage | La touche Maj a été enfoncée.   |



 

Les événements système suivants sont définis pour être utilisés dans le membre **bCursorMode** .



| Valeur              | Description               |
|--------------------|---------------------------|
| SE \_ \_curseur normal | Indique l’info-bulle du stylet.    |
| SE \_ curseur de gomme \_ | Indique la gomme du stylet. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IStylusPlugin :: SystemEvent, méthode**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**ITabletEventSink :: SystemEvent, méthode**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




