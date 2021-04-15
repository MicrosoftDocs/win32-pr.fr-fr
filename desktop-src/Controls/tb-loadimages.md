---
title: Message TB_LOADIMAGES (commctrl. h)
description: Charge les images de bouton définies par le système dans la liste d’images d’un contrôle ToolBar.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466223"
---
# <a name="tb_loadimages-message"></a>TO \_ LOADIMAGES message

Charge les images de bouton définies par le système dans la liste d’images d’un contrôle ToolBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur d’une liste d’images de boutons définie par le système. Ce paramètre peut être défini sur l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                | Signification                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**format d' \_ historique des \_ couleurs de grande taille \_**</dt> </dl> | Bitmaps de l’Explorateur Windows en grande taille.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**\_couleur de \_ petite taille \_ de IDB hist**</dt> </dl> | Bitmaps de l’Explorateur Windows en petite taille.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**\_taille STD de la \_ grande \_ couleur**</dt> </dl>    | Images bitmap standard en grande taille.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**\_couleur standard de la \_ petite \_ couleur IDB**</dt> </dl>    | Images bitmap standard de petite taille.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**\_ \_ grande \_ couleur de la vue IDB**</dt> </dl> | Affichez les bitmaps en grandes tailles.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**\_couleur de \_ petite taille \_ de la vue IDB**</dt> </dl> | Affichez les bitmaps dans une petite taille.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**historique des IDB- \_ \_ normal**</dt> </dl>                 | Les boutons de déplacement de l’Explorateur Windows et les bitmaps favoris sont dans un état normal.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**\_historique \_ chaud de IDB**</dt> </dl>                          | Les boutons de déplacement de l’Explorateur Windows et les bitmaps favoris dans un état actif.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**Hist. IDB \_ \_ désactivé**</dt> </dl>           | Les boutons de déplacement et les bitmaps favoris de l’Explorateur Windows sont en état désactivé.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**historique de IDB \_ \_ enfoncé**</dt> </dl>              | Les boutons de déplacement et les bitmaps favoris de l’Explorateur Windows sont en état appuyé.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle d’instance. Ce paramètre doit être défini sur HINST \_ COMMCTRL.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Nombre d’images dans la liste d’images. Retourne zéro si la barre d’outils n’a pas de liste d’images ou si la liste d’images existante est vide.

## <a name="remarks"></a>Notes

Vous devez utiliser les valeurs d’index d’image appropriées lorsque vous préparez des structures [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) avant d’envoyer le message [**to \_ ADDBUTTONS**](tb-addbuttons.md) . Pour obtenir la liste des valeurs d’index d’image pour ces bitmaps prédéfinies, consultez la rubrique [valeurs d’index d’image du bouton standard de la barre d’outils](toolbar-standard-button-image-index-values.md).

## <a name="examples"></a>Exemples

L’exemple de code suivant charge les images de petite couleur système standard.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ ADDBITMAP**](tb-addbitmap.md)
</dt> </dl>

 

 





