---
title: Ressource DIALOGEX
description: Définit une boîte de dialogue. | Ressource DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menus de ressources DIALOGEX et autres ressources
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211558"
---
# <a name="dialogex-resource"></a>Ressource DIALOGEX

Définit une boîte de dialogue. L’instruction définit la position et les dimensions de la boîte de dialogue sur l’écran, ainsi que le style de la boîte de dialogue. Il définit également les éléments suivants :

-   Les ID d’aide dans la boîte de dialogue elle-même, ainsi que sur les contrôles dans la boîte de dialogue.
-   Utilisation de l’instruction [**ExStyle**](exstyle-statement.md) pour la boîte de dialogue elle-même, ainsi que sur les contrôles de la boîte de dialogue.
-   Paramètres d’épaisseur et d’italique de la police à utiliser dans la boîte de dialogue.
-   Données spécifiques au contrôle pour les contrôles dans la boîte de dialogue.
-   Utilisation des noms de classe système prédéfinis **BEDIT**, **IEDIT** et **HEDIT** .

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nom unique ou valeur d’entier non signé 16 bits unique qui identifie la boîte de dialogue.

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Emplacement à l’écran du côté gauche de la boîte de dialogue, en unités de boîte de dialogue.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Emplacement à l’écran du haut de la boîte de dialogue, en unités de boîte de dialogue.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Largeur*
</dt> <dd>

Largeur de la boîte de dialogue, en unités de boîte de dialogue.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*celle*
</dt> <dd>

Hauteur de la boîte de dialogue, en unités de boîte de dialogue.

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Expression numérique indiquant l’ID utilisé pour identifier la boîte de dialogue lors du traitement de [**\_ l’aide WM**](../shell/wm-help.md) .

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*
</dt> <dd>

Options de la boîte de dialogue. Il peut s’agir de zéro ou plusieurs des instructions suivantes.



| .                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Légende** «*texte*»                                              | Légende de la boîte de dialogue si elle a une barre de titre. Pour plus d’informations, consultez l' [**instruction Caption**](caption-statement.md).                                                                                                                                                                                                                                                                                                                                                            |
| **Caractéristiques** *DWORD*                                       | Valeur **DWORD** définie par l’utilisateur pour une utilisation par les outils de ressources. Cette valeur n’est pas utilisée par le système. Pour plus d’informations, consultez l' [**instruction characteristics**](characteristics-statement.md).                                                                                                                                                                                                                                                                                               |
| _Classe de_ classe                                                  | Entier non signé 16 bits ou chaîne, placé entre guillemets doubles ("), qui identifie la classe de la boîte de dialogue. Pour plus d’informations, consultez [**Class, instruction**](class-statement.md).                                                                                                                                                                                                                                                                                     |
| **EXstyler** =  *styles étendus*                                    | Style de fenêtre étendue de la boîte de dialogue. Pour plus d’informations, consultez l' [**instruction ExStyle**](exstyle-statement.md).                                                                                                                                                                                                                                                                                                                                                                    |
| **Taille** *de la police, "* caractère", *poids*, *italique*, *jeu* de *caractères* | Taille du point et police de la police. Pour le *poids*, utilisez les valeurs **FW \_ \** _ définies dans WinGDI. h. Pour _italic *, spécifiez TRUE pour utiliser une police italique ; sinon, FALSe. Pour *charset*, utilisez la valeur définie dans le membre **lfCharSet** de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Pour obtenir la police définitive pour une boîte de dialogue, une application doit spécifier un *jeu* de caractères avec d’autres propriétés de police. Pour plus d’informations, consultez [**instruction font**](font-statement.md). |
|  *Langue* langue, sous- *langue*                            | Langue de la boîte de dialogue. Pour plus d’informations, consultez [**Language Statement**](language-statement.md).                                                                                                                                                                                                                                                                                                                                                                               |
| Le **menu** *NomMenu*                                               | Menu à utiliser. Cette valeur est soit le nom du menu, soit son identificateur entier. Pour plus d’informations, consultez l' [**instruction menu**](menu-statement.md).                                                                                                                                                                                                                                                                                                                             |
|  *Styles* de style                                                | Styles de la boîte de dialogue. Pour plus d’informations, consultez l' [**instruction style**](style-statement.md).                                                                                                                                                                                                                                                                                                                                                                                       |
| **Version** *DWORD*                                               | Valeur **DWORD** définie par l’utilisateur. Cette instruction est destinée à être utilisée par des outils de ressources supplémentaires et n’est pas utilisée par le système. Pour plus d’informations, consultez [**version, instruction**](version-statement.md).                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*instructions de contrôle*
</dt> <dd>

Le corps de la ressource **DIALOGEX** est constitué d’un nombre quelconque d’instructions de contrôle. Il existe quatre familles d’instructions de contrôle : génériques, statiques, Button et Edit. Pour plus d'informations, consultez la section Notes.

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="remarks"></a>Notes

Les opérations valides qui peuvent être contenues dans les expressions numériques des instructions de **DIALOGEX** sont les suivantes :

-   Add (' + ')
-   Soustraire ('-')
-   Moins unaire ('-')
-   NOT unaire (' ~ ')
-   AND (' & ')
-   OU (' \| ')

Le corps de la ressource est constitué d’instructions génériques, statiques, de bouton et de contrôle de modification. Bien que chacune de ces familles d’instructions utilise une syntaxe différente pour définir des fonctionnalités spécifiques de ses contrôles, elles partagent toutes une syntaxe commune pour définir la position, la taille, les styles étendus, le numéro d’identification de l’aide et les données spécifiques aux contrôles. Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).

### <a name="generic-control-statements"></a>Instructions de contrôle génériques

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texte de la fenêtre pour le contrôle. Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*identifi*
</dt> <dd>

Identificateur de contrôle. Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).

</dd> <dt>

<span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*NomClasse*
</dt> <dd>

Nom de la classe. Il peut s’agir d’une chaîne placée entre guillemets doubles (") ou de l’une des classes système prédéfinies suivantes : **Button**, **static**, **Edit**, **ListBox**, **ScrollBar** ou **ComboBox**.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Les styles de fenêtres (valeurs explicites **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lbs \_ \* *_, _* SBS \_ \* *_ et _* SCC \_ \*** style définis dans winuser. H peuvent être utilisés en ajoutant un include au fichier. RC : `#include "winuser.h"` ). Pour plus d’informations, consultez [styles de fenêtre](/windows/desktop/winmsg/window-styles).

</dd> </dl>

### <a name="static-control-statements"></a>Instructions de contrôle statiques

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*
</dt> <dd>

**LTEXT**, **rtext** ou **CTEXT**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texte de la fenêtre pour le contrôle. Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*identifi*
</dt> <dd>

Identificateur de contrôle. Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).

</dd> </dl>

### <a name="button-control-statements"></a>Instructions de contrôle de bouton

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*
</dt> <dd>

**AUTO3STATE**, **autocase à cocher**, **case d’option, case à** cocher, **PUSHBOX**, **PUSHBUTTON**, **RadioButton**, **STATE3** ou **UserButton**. 

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texte de la fenêtre pour le contrôle. Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*identifi*
</dt> <dd>

Identificateur de contrôle. Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).

</dd> </dl>

### <a name="edit-control-statements"></a>Instructions de contrôle d’édition

``` syntax
editClass id
```

<dl> <dt>

<span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*
</dt> <dd>

**EDITTEXT**, **BEDIT**, **HEDIT** ou **IEDIT**.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*identifi*
</dt> <dd>

Identificateur de contrôle. Pour plus d’informations, consultez [paramètres de contrôle communs](common-control-parameters.md).

</dd> </dl>

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

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[MENUS](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Version**](version-statement.md)
</dt> </dl>

 

 
