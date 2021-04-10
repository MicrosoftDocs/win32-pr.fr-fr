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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210821"
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
| \_modificateur de se \_ CTRL  | La touche de contrôle a été enfoncée. |
| \_modificateur de se \_ ALT   | La touche Alt a été enfoncée.     |
| \_changement de modificateur de se \_ | La touche Maj a été enfoncée.   |



 

Les événements système suivants sont définis pour être utilisés dans le membre **bCursorMode** .



| Valeur              | Description               |
|--------------------|---------------------------|
| \_curseur normal \_ se | Indique l’info-bulle du stylet.    |
| curseur de la \_ gomme se \_ | Indique la gomme du stylet. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IStylusPlugin :: SystemEvent, méthode**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**ITabletEventSink :: SystemEvent, méthode**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




