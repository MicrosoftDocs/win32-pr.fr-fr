---
title: Message TB_SETPRESSEDIMAGELIST (commctrl. h)
description: Définit la liste d’images utilisée par la barre d’outils pour afficher les boutons qui sont dans un état appuyé.
ms.assetid: d0e061ec-3a89-4c2d-b7f7-5f2061098428
keywords:
- TB_SETPRESSEDIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a3c6dafed6dbfdf2a654f4f95f1cef636ba762
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116521"
---
# <a name="tb_setpressedimagelist-message"></a>TO \_ SETPRESSEDIMAGELIST message

Définit la liste d’images utilisée par la barre d’outils pour afficher les boutons qui sont dans un état appuyé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de la liste d’images. Si vous n’utilisez qu’une seule liste d’images, définissez ce paramètre sur zéro. Pour plus d’informations sur l’utilisation de plusieurs listes d’images, consultez la section Notes.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la liste d’images à définir. Si ce paramètre a la **valeur null**, aucune image ne s’affiche dans les boutons.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le handle de la liste d’images utilisée précédemment pour afficher les boutons dans un état appuyé, ou **null** si aucune liste d’images n’a été définie précédemment.

## <a name="remarks"></a>Notes

> [!Note]  
> Votre application est chargée de libérer la liste d’images après la destruction de la barre d’outils.

 

Le **message \_ SETPRESSEDIMAGELIST to** ne peut pas être combiné avec [**to \_ ADDBITMAP**](tb-addbitmap.md). Elle ne peut pas non plus être utilisée avec les barres d’outils créées avec [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), qui appelle **to \_ ADDBITMAP** en interne. Lorsque vous créez une barre d’outils avec **CreateToolbarEx** ou utilisez **to \_ ADDBITMAP** pour ajouter des images, la barre d’outils gère la liste d’images en interne. Toute tentative de modification avec **to \_ SETPRESSEDIMAGELIST** a des conséquences imprévisibles.

Il n’est pas nécessaire que les images de bouton proviennent de la même liste d’images. Pour utiliser plusieurs listes d’images pour vos images de bouton de barre d’outils :

1.  Activez plusieurs listes d’images en envoyant le contrôle ToolBar à un message [**\_ SETVERSION CCM**](ccm-setversion.md) avec *wParam* (le numéro de version) défini sur 5.
2.  Pour chaque liste d’images que vous souhaitez utiliser, envoyez au contrôle ToolBar un message **\_ SETPRESSEDIMAGELIST to** . Affectez à *wParam* une valeur *wParam* définie par l’application qui sera utilisée pour identifier la liste. Affectez à *lParam* la valeur du handle HIMAGELIST de la liste.
3.  Pour chaque bouton, définissez le membre **iBitmap** de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) du bouton sur MAKELONG (*iIndex*, *iImageID*). La valeur *iImageID* est l’ID de la liste d’images appropriée définie à l’étape 2. La valeur *iIndex* est l’index de l’image particulière dans cette liste.
4.  Ajoutez les boutons en envoyant le contrôle de barre d’outils à un message [**\_ ADDBUTTONS to**](tb-addbuttons.md) .

Le fragment de code suivant montre comment ajouter cinq boutons à une barre d’outils, avec des images de trois listes d’images différentes. La prise en charge de plusieurs listes d’images est activée avec un message [**CCM \_ SETVERSION**](ccm-setversion.md) . Les listes d’images sont ensuite définies et les ID attribués de 0-2. Les boutons sont affectés aux images à partir des listes d’images comme suit :

-   Le bouton 0 provient de la liste d’images zéro (ahimd \[ 0 \] ) avec l’index 1.
-   Le bouton 1 est issu de la liste d’images 1 (Ahim \[ 1 \] ) avec un index de 1.
-   Le bouton 2 provient de la liste d’images deux (Ahim \[ 2 \] ) avec un index de 1.
-   Le bouton 3 est issu de la liste d’images zéro (ahimd \[ 0 \] ) avec un index de 2.
-   Le bouton 4 est issu de la liste d’images 1 (Ahim \[ 1 \] ) avec un index de 3.

Enfin, les boutons sont ajoutés au contrôle Toolbar avec un message [**\_ ADDBUTTONS to**](tb-addbuttons.md) .


```
// Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TO \_ GETPRESSEDIMAGELIST**](tb-getpressedimagelist.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))
</dt> </dl>

 

