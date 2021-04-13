---
title: DLGTEMPLATEEX, structure
description: Un modèle de boîte de dialogue étendu commence par un en-tête DLGTEMPLATEEX qui décrit la boîte de dialogue et spécifie le nombre de contrôles dans la boîte de dialogue.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Boîtes de dialogue de la structure DLGTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508958"
---
# <a name="dlgtemplateex-structure"></a>DLGTEMPLATEEX, structure

Un modèle de boîte de dialogue étendu commence par un en-tête **DLGTEMPLATEEX** qui décrit la boîte de dialogue et spécifie le nombre de contrôles dans la boîte de dialogue. Pour chaque contrôle d’une boîte de dialogue, un modèle de boîte de dialogue étendue contient un bloc de données qui utilise le format [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) pour décrire le contrôle.

La structure **DLGTEMPLATEEX** n’est définie dans aucun fichier d’en-tête standard. La définition de structure est fournie ici pour expliquer le format d’un modèle étendu pour une boîte de dialogue.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a>Membres

<dl> <dt>

**dlgVer**
</dt> <dd>

Type : **Word**

</dd> <dd>

Numéro de version du modèle de boîte de dialogue étendue. Ce membre doit avoir la valeur 1.

</dd> <dt>

**signature**
</dt> <dd>

Type : **Word**

</dd> <dd>

Indique si un modèle est un modèle de boîte de dialogue étendue. Si la **signature** est 0xFFFF, il s’agit d’un modèle de boîte de dialogue étendue. Dans ce cas, le membre **dlgVer** spécifie le numéro de version du modèle. Si la **signature** correspond à une valeur autre que 0xFFFF, il s’agit d’un modèle de boîte de dialogue standard qui utilise les structures [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) et [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) .

</dd> <dt>

**helpID**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Identificateur de contexte d’aide pour la fenêtre de boîte de dialogue. Lorsque le système envoie un [**message \_ d’aide WM**](../shell/wm-help.md) , il transmet cette valeur dans le membre **WContextId** de la structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .

</dd> <dt>

**exStyle**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Styles Windows étendus. Ce membre n’est pas utilisé lors de la création de boîtes de dialogue, mais les applications qui utilisent des modèles de boîte de dialogue peuvent l’utiliser pour créer d’autres types de fenêtres. Pour obtenir la liste des valeurs, consultez [**styles de fenêtre étendus**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Style de la boîte de dialogue. Ce membre peut être une combinaison de [valeurs de style de fenêtre](/windows/desktop/winmsg/window-styles) et de [valeurs de style de boîte de dialogue](dialog-box-styles.md).

Si **style** inclut le style de boîte de dialogue **DS \_ SetFont** ou **DS \_ SHELLFONT** , l’en-tête **DLGTEMPLATEEX** du modèle de boîte de dialogue étendue contient quatre membres **supplémentaires (taille**, **épaisseur**, **italique** et **police**) qui décrivent la police à utiliser pour le texte dans la zone cliente et les contrôles de la boîte de dialogue. Si possible, le système crée une police en fonction des valeurs spécifiées dans ces membres. Le système envoie ensuite un message [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) à la boîte de dialogue et à chaque contrôle pour fournir un handle à la police.

Pour plus d’informations, consultez polices de boîte de [dialogue](about-dialog-boxes.md).

</dd> <dt>

**cDlgItems**
</dt> <dd>

Type : **Word**

</dd> <dd>

Nombre de contrôles dans la boîte de dialogue.

</dd> <dt>

**x**
</dt> <dd>

Type : **short**

</dd> <dd>

Coordonnée x, en unités de boîte de dialogue, de l’angle supérieur gauche de la boîte de dialogue.

</dd> <dt>

**y**
</dt> <dd>

Type : **short**

</dd> <dd>

Coordonnée y, en unités de boîte de dialogue, de l’angle supérieur gauche de la boîte de dialogue.

</dd> <dt>

**adéquat**
</dt> <dd>

Type : **short**

</dd> <dd>

Largeur, en unités de boîte de dialogue, de la boîte de dialogue.

</dd> <dt>

**CY**
</dt> <dd>

Type : **short**

</dd> <dd>

Hauteur, en unités de boîte de dialogue, de la boîte de dialogue.

</dd> <dt>

**menus**
</dt> <dd>

Type : **SZ \_ ou \_ ORD**

</dd> <dd>

Tableau de longueur variable d’éléments 16 bits qui identifie une ressource de menu pour la boîte de dialogue. Si le premier élément de ce tableau est 0x0000, la boîte de dialogue n’a pas de menu et le tableau n’a pas d’autres éléments. Si le premier élément est 0xFFFF, le tableau a un élément supplémentaire qui spécifie la valeur ordinale d’une ressource de menu dans un fichier exécutable. Si le premier élément a une autre valeur, le système traite le tableau comme une chaîne Unicode terminée par le caractère null qui spécifie le nom d’une ressource de menu dans un fichier exécutable.

</dd> <dt>

**windowClass**
</dt> <dd>

Type : **SZ \_ ou \_ ORD**

</dd> <dd>

Tableau de longueur variable d’éléments 16 bits qui identifie la classe de fenêtre de la boîte de dialogue. Si le premier élément du tableau est 0x0000, le système utilise la classe de boîte de dialogue prédéfinie pour la boîte de dialogue et le tableau n’a pas d’autres éléments. Si le premier élément est 0xFFFF, le tableau a un élément supplémentaire qui spécifie la valeur ordinale d’une classe de fenêtre système prédéfinie. Si le premier élément a une autre valeur, le système traite le tableau comme une chaîne Unicode terminée par le caractère null qui spécifie le nom d’une classe de fenêtre inscrite.

</dd> <dt>

**title**
</dt> <dd>

Type : **WCHAR \[ titleLen \]**

</dd> <dd>

Titre de la boîte de dialogue. Si le premier élément de ce tableau est 0x0000, la boîte de dialogue n’a pas de titre et le tableau n’a pas d’autres éléments.

</dd> <dt>

**pointsize**
</dt> <dd>

Type : **Word**

</dd> <dd>

Taille en points de la police à utiliser pour le texte dans la boîte de dialogue et ses contrôles.

Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.

</dd> <dt>

**weight**
</dt> <dd>

Type : **Word**

</dd> <dd>

Poids de la police. Notez que, bien qu’il peut s’agir de l’une des valeurs énumérées pour le membre **lfWeight** de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , toute valeur utilisée sera automatiquement remplacée par le **FW \_ normal**.

Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.

</dd> <dt>

**italique**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Indique si la police est en italique. Si cette valeur est **true**, la police est en italique.

Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.

</dd> <dt>

**caractères**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Jeu de caractères à utiliser. Pour plus d’informations, consultez le membre **lfCharSet** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).

Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.

</dd> <dt>

**certain**
</dt> <dd>

Type : **WCHAR \[ stringLen \]**

</dd> <dd>

Nom de la police de la police.

Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez utiliser un modèle de boîte de dialogue étendu à la place d’un modèle de boîte de dialogue standard dans les fonctions [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)et [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .

Le fait de suivre l’en-tête **DLGTEMPLATEEX** dans un modèle de boîte de dialogue étendue est une ou plusieurs structures [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) qui décrivent les contrôles de la boîte de dialogue. Le membre **cDlgItems** de la structure **DLGITEMTEMPLATEEX** spécifie le nombre de structures **DLGITEMTEMPLATEEX** qui suivent dans le modèle.

Chaque structure [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) du modèle doit être alignée sur une limite **DWORD** . Si le membre de **style** spécifie le style **DS \_ SetFont** ou **DS \_ SHELLFONT** , la première structure **DLGITEMTEMPLATEEX** commence sur la première limite **DWORD** après la chaîne de **police** . Si ces styles ne sont pas spécifiés, la première structure commence sur la première limite **DWORD** après la chaîne de **titre** .

Les tableaux **menu**, **WindowClass**, **title** et **Typeface** doivent être alignés sur les limites de **mots** .

Si vous spécifiez des chaînes de caractères dans les tableaux **menu**, **WindowClass**, **title** et **Typeface** , vous devez utiliser des chaînes Unicode. Utilisez la fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) pour générer ces chaînes Unicode à partir de chaînes ANSI.

Les membres **x**, **y**, **CX** et **CY** spécifient des valeurs dans les unités de la boîte de dialogue. Vous pouvez convertir ces valeurs en unités d’écran (pixels) à l’aide de la fonction [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**\_SetFont WM**](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Boîtes de dialogue](dialog-boxes.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

