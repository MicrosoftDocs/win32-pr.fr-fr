---
title: Ressource de boîte de dialogue
description: Définit une boîte de dialogue. | Ressource de boîte de dialogue
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Menus des ressources de la boîte de dialogue et autres ressources
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a821bb6890a9aee8dd74c5412556bf45ca0b739a6eb12cf5d582fbb91463c2f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034347"
---
# <a name="dialog-resource"></a>Ressource de boîte de dialogue

Définit une boîte de dialogue. L’instruction définit la position et les dimensions de la boîte de dialogue sur l’écran, ainsi que le style de la boîte de dialogue.

> [!Note]  
> La **boîte de dialogue** est un ID de ressource obsolète. Les nouvelles applications doivent utiliser [**DIALOGEX**](dialogex-resource.md).

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nom unique ou valeur d’entier non signé 16 bits unique qui identifie la boîte de dialogue.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*
</dt> <dd>

Options de la boîte de dialogue. Il peut s’agir de zéro ou plusieurs des instructions suivantes.



| .                                                        | Description                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Légende**](caption-statement.md) «*texte*»                    | Légende de la boîte de dialogue si elle a une barre de titre. Pour plus d’informations, consultez [**Caption**](caption-statement.md).                                                                             |
| [**Caractéristiques**](characteristics-statement.md) *DWORD*     | Valeur **DWORD** définie par l’utilisateur pour une utilisation par les outils de ressources. Cette valeur n’est pas utilisée par le système. Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md).                |
| [](class-statement.md) *Classe de* classe                         | Entier non signé 16 bits ou chaîne, placé entre guillemets doubles ("), qui identifie la classe de la boîte de dialogue. Pour plus d’informations, consultez la [**classe**](class-statement.md).      |
| **ExStyle =** *styles étendus*                                   | Style de fenêtre étendue de la boîte de dialogue. Pour plus d’informations, consultez [**ExStyle**](exstyle-statement.md).                                                                                     |
| **Taille** *de la* police *,* police                                 | Taille du point et police de la police. Pour plus d’informations, consultez [**font**](font-statement.md).                                                                                              |
| [](language-statement.md) *Langue* langue, sous- *langue* | Langue de la boîte de dialogue. Pour plus d’informations, consultez [**Language**](language-statement.md).                                                                                                |
| Le **menu** *NomMenu*                                              | Menu à utiliser. Cette valeur est soit le nom du menu, soit son identificateur entier.                                                                                                        |
| [](style-statement.md) *Styles* de style                        | Styles de la boîte de dialogue. Pour plus d’informations, consultez [**style**](style-statement.md).                                                                                                        |
| [**Version**](version-statement.md) *DWORD*                     | Valeur **DWORD** définie par l’utilisateur. Cette instruction est destinée à être utilisée par des outils de ressources supplémentaires et n’est pas utilisée par le système. Pour plus d’informations, consultez [**version**](version-statement.md). |



 

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="remarks"></a>Remarques

La fonction [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) retourne les unités de base de la boîte de dialogue en pixels. La signification exacte des coordonnées dépend du style défini par l’instruction option de [**style**](style-statement.md) . Pour les boîtes de dialogue de style enfant, les coordonnées sont relatives à l’origine de la fenêtre parente, sauf si la boîte de dialogue a le style **DS \_ ABSALIGN**; dans ce cas, les coordonnées sont relatives à l’origine de l’écran d’affichage.

N’utilisez pas le style **WS \_ Child** avec une boîte de dialogue modale. La fonction [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) désactive toujours le parent/propriétaire de la boîte de dialogue nouvellement créée. Quand une fenêtre parente est désactivée, ses fenêtres enfants sont implicitement désactivées. Étant donné que la fenêtre parente de la boîte de dialogue de style enfant est désactivée, la boîte de dialogue de style enfant est également activée.

Si une boîte de dialogue a le style **DS \_ ABSALIGN** , les coordonnées de son angle supérieur gauche sont relatives à l’origine de l’écran et non à l’angle supérieur gauche de la fenêtre parente. En général, vous utilisez ce style lorsque vous souhaitez que la boîte de dialogue démarre dans une partie spécifique de l’affichage, quel que soit l’endroit où la fenêtre parente peut se trouver à l’écran.

La **boîte de dialogue** nom peut également être utilisée comme paramètre de nom de classe de la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour créer une fenêtre avec des attributs de boîte de dialogue.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **Dialog** :

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des boîtes de dialogue](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**ACCÉLÉRATEURS**](accelerators-resource.md)
</dt> <dt>

[**ATTRIBUTS**](characteristics-statement.md)
</dt> <dt>

[**RÉGULATION**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**SOUS**](language-statement.md)
</dt> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**VERSION**](version-statement.md)
</dt> </dl>

 

 
