---
title: Message EM_INSERTIMAGE (RichEdit. h)
description: Remplace la sélection par un objet BLOB qui affiche une image.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE les contrôles de message Windows
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
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464535"
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



 

## <a name="remarks"></a>Notes

Si la sélection est un point d’insertion, l’objet blob d’image est inséré au point d’insertion.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_INSERTTABLE em**](em-inserttable.md)
</dt> </dl>

 

 





