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
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530261"
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

## <a name="remarks"></a>Notes

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



 

## <a name="requirements"></a>Spécifications



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

 

 




