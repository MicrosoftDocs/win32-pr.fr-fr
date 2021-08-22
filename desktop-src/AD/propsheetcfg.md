---
title: PROPSHEETCFG, structure
description: Utilisé pour contenir les données de configuration de la feuille de propriétés.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory de la structure PROPSHEETCFG
- Active Directory pointeur de structure PPROPSHEETCFG
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 971296e1e269e977919f142d1efe24426b9c83f19ac26da2e2362ab48da0aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025437"
---
# <a name="propsheetcfg-structure"></a>PROPSHEETCFG, structure

La structure **PROPSHEETCFG** est utilisée pour contenir les données de configuration de la feuille de propriétés. Cette structure est contenue dans le format de presse-papiers [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) .

> [!Note]  
> Cette structure n’est pas définie dans un fichier d’en-tête publié. Pour utiliser cette structure, vous devez la définir vous-même dans le format exact indiqué.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a>Membres

<dl> <dt>

**lNotifyHandle**
</dt> <dd>

Contient le handle de notification. Il est identique au handle passé pour le paramètre de *handle* dans la méthode [**IExtendPropertySheet2 :: CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .

</dd> <dt>

**hwndParentSheet**
</dt> <dd>

Contient le handle de fenêtre de la feuille de propriétés parente.

</dd> <dt>

**hwndHidden**
</dt> <dd>

Contient le handle de la fenêtre masquée.

</dd> <dt>

**wParamSheetClose**
</dt> <dd>

Contient une valeur 32 bits définie par l’application. Cette valeur est renvoyée à l’application dans le *wParam* du message de fermeture de la feuille de calcul [**WM \_ DSA \_ \_ \_**](wm-dsa-sheet-close-notify.md) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[**notification de fermeture de la \_ feuille du DSA WM \_ \_ \_**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

