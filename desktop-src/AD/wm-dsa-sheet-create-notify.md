---
title: Message WM_DSA_SHEET_CREATE_NOTIFY
description: Publié dans le composant logiciel enfichable MMC Active Directory pour créer une feuille de propriétés secondaire.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- Message de WM_DSA_SHEET_CREATE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942206"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>\_Créer un \_ message \_ de \_ notification de la feuille DSA DSA

Le message de notification de création d’une **\_ \_ feuille \_ \_ DSA DSA** est publié dans le composant logiciel enfichable MMC Active Directory pour créer une feuille de propriétés secondaire.

> [!Note]  
> La valeur de ce message n’est pas définie dans un fichier d’en-tête publié. Pour utiliser cette valeur de message, définissez-la dans le format exact indiqué.

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
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

Contient un pointeur vers une structure d' [**\_ informations de \_ page \_ DSA sec**](dsa-sec-page-info.md) qui définit la feuille de propriétés secondaire à créer. Le récepteur du message doit libérer cette mémoire avec la fonction [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) lorsqu’il n’est plus nécessaire.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Non utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> <dt>

[**\_ \_ informations sur la page DSA sec \_**](dsa-sec-page-info.md)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

