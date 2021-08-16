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
ms.openlocfilehash: c51fc850504eb4455a41b881aed1109554d0482a8f889fafa2eaf7050488e450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024187"
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

 

