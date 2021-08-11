---
title: Message WM_DSA_SHEET_CLOSE_NOTIFY
description: Publié dans le composant logiciel enfichable MMC Active Directory lorsqu’une feuille de propriétés secondaire est détruite.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- Message de WM_DSA_SHEET_CLOSE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f840790de51ce712b33fc9a9611934e8be9a76a35a0fc01a4ce0abe4ba040d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181670"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>Message de fermeture de la \_ feuille du DSA WM \_ \_ \_

Le message de fermeture de la feuille de calcul **\_ DSA DSA \_ \_ \_** est publié dans le composant logiciel enfichable MMC Active Directory lorsqu’une feuille de propriétés secondaire est détruite.

> [!Note]  
> La valeur de ce message n’est pas définie dans un fichier d’en-tête publié. Pour utiliser cette valeur de message, vous devez la définir vous-même dans le format exact indiqué.

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de fenêtre de la fenêtre du composant logiciel enfichable qui traitera ce message. Ce handle est obtenu à partir du membre **hwndHidden** de la structure [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Contient une valeur 32 bits définie par l’application. Elle est obtenue à partir du membre **wParamSheetClose** de la structure [**PROPSHEETCFG**](propsheetcfg.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> </dl>

 

 





