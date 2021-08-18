---
title: Message WM_ADSPROP_SHEET_CREATE
description: Envoyé à l’objet de notification pour créer une feuille de propriétés secondaire dans un composant logiciel enfichable MMC Active Directory.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_SHEET_CREATE Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ec88eaed682fd16fecb717b851b902d5ba52ce08d5360aa78b881a4b8cb4f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024197"
---
# <a name="wm_adsprop_sheet_create-message"></a>Créer un message de la \_ feuille ADSPROP WM \_ \_

Le message de création de la **\_ \_ feuille \_ ADSPROP WM** est envoyé à l’objet notification pour créer une feuille de propriétés secondaire dans un composant logiciel enfichable MMC Active Directory.

> [!Note]  
> La valeur de ce message n’est pas définie dans un fichier d’en-tête publié. Pour utiliser cette valeur de message, vous devez la définir vous-même dans le format exact indiqué.

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de l’objet de notification. Pour obtenir ce handle, appelez [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Contient un pointeur vers une structure d' [**\_ informations de \_ page \_ DSA sec**](dsa-sec-page-info.md) qui définit la page secondaire à créer. Une seule feuille de propriétés secondaire peut être créée avec le message de **\_ \_ \_ création de feuille ADSPROP WM** , de sorte que la structure [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) ne peut contenir qu’une seule structure [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé. Doit avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message est toujours égale à zéro.

## <a name="remarks"></a>Remarques

L’appelant doit allouer la structure des informations de la [**\_ \_ page \_ DSA sec**](dsa-sec-page-info.md) , la chaîne de titre et toutes les chaînes [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) à l’aide d’un appel unique à la fonction [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) . Le message de création de la **\_ feuille de ADSPROP \_ \_ WM** est un message asynchrone. il retournera donc avant la création de la feuille secondaire. Pour cette raison, la mémoire doit rester intacte après le retour du message. Le récepteur libère cette mémoire avec un appel unique à la fonction [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) après la création de la feuille secondaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFSTR \_ DS \_ PARENTHWND**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**\_ \_ informations sur la page DSA sec \_**](dsa-sec-page-info.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

