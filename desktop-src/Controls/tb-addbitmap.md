---
title: Message TB_ADDBITMAP (commctrl. h)
description: Ajoute une ou plusieurs images à la liste des images de bouton disponibles pour une barre d’outils.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- TB_ADDBITMAP les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743972"
---
# <a name="tb_addbitmap-message"></a>TO \_ ADDBITMAP message

Ajoute une ou plusieurs images à la liste des images de bouton disponibles pour une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre d’images de bouton dans l’image bitmap. Si *lParam* spécifie une image bitmap définie par le système, ce paramètre est ignoré.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) qui contient l’identificateur d’une ressource bitmap et le handle vers l’instance de module avec le fichier exécutable qui contient la ressource bitmap.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de la première nouvelle image en cas de réussite, ou-1 dans le cas contraire.

## <a name="remarks"></a>Notes

Si la barre d’outils a été créée à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , vous devez envoyer le message [**to \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) à la barre d’outils avant d’envoyer **to \_ ADDBITMAP**.

## <a name="examples"></a>Exemples

L’exemple suivant crée une image bitmap à partir d’une ressource (IDB \_ bitmap1), mappe la couleur d’arrière-plan (noir dans ce cas) à la couleur de la face du bouton système et l’ajoute à la barre d’outils.


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

