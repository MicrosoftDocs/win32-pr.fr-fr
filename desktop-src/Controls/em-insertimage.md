---
title: Message EM_INSERTIMAGE (RichEdit. h)
description: Remplace la sélection par un objet BLOB qui affiche une image.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7418a8fe4b7c627d211bce7bf2591ed684d82e42089fbe9bedeb2f76a6b9d3e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437889"
---
# <a name="em_insertimage-message"></a>\_Message INSERTIMAGE em

Remplace la sélection par un objet BLOB qui affiche une image.


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**de \_ \_ paramètres d’image RichEdit**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) qui contient l’objet blob d’image.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou l’un des codes d’erreur suivants.



| Code de retour                                                                                    | Description                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**E \_ ÉCHEC**</dt> </dl>        | Impossible d’insérer l’image. <br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Le paramètre *lParam* a la valeur null ou pointe vers une image non valide. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La mémoire disponible est insuffisante.<br/>                  |



 

## <a name="remarks"></a>Remarques

Si la sélection est un point d’insertion, l’objet blob d’image est inséré au point d’insertion.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_INSERTTABLE em**](em-inserttable.md)
</dt> </dl>

 

 





