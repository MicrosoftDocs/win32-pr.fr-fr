---
title: DLGITEMTEMPLATEEX, structure
description: Bloc de texte utilisé par un modèle de boîte de dialogue étendu pour décrire la boîte de dialogue étendue. Pour obtenir une description du format d’un modèle de boîte de dialogue étendue, consultez DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Boîtes de dialogue de la structure DLGITEMTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad2bf1795f5059ec1fdda00ddb6a93cfe396dae5b4119d392eff42382fa978b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785865"
---
# <a name="dlgitemtemplateex-structure"></a>DLGITEMTEMPLATEEX, structure

Bloc de texte utilisé par un modèle de boîte de dialogue étendu pour décrire la boîte de dialogue étendue. Pour obtenir une description du format d’un modèle de boîte de dialogue étendue, consultez [**DLGTEMPLATEEX**](dlgtemplateex.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a>Membres

<dl> <dt>

**helpID**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Identificateur du contexte d’aide pour le contrôle. Lorsque le système envoie un [**message \_ d’aide WM**](../shell/wm-help.md) , il transmet la valeur **HelpID** dans le membre **dwContextId** de la structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .

</dd> <dt>

**exStyle**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Styles étendus pour une fenêtre. Ce membre n’est pas utilisé pour créer des contrôles dans les boîtes de dialogue, mais les applications qui utilisent des modèles de boîte de dialogue peuvent l’utiliser pour créer d’autres types de fenêtres. Pour obtenir la liste des valeurs, consultez [**styles de fenêtre étendus**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Style du contrôle. Ce membre peut être une combinaison de [valeurs de style de fenêtre](/windows/desktop/winmsg/window-styles) (par exemple, **WS \_ Border**) et une ou plusieurs des [valeurs de style de contrôle](/windows/desktop/Controls/common-control-styles) (par exemple, **BS \_ PUSHBUTTON** et es restantes). **\_**

</dd> <dt>

**x**
</dt> <dd>

Type : **short**

</dd> <dd>

Coordonnée x, en unités de boîte de dialogue, du coin supérieur gauche du contrôle. Cette coordonnée est toujours relative à l’angle supérieur gauche de la zone cliente de la boîte de dialogue.

</dd> <dt>

**y**
</dt> <dd>

Type : **short**

</dd> <dd>

Coordonnée y, en unités de boîte de dialogue, de l’angle supérieur gauche du contrôle. Cette coordonnée est toujours relative à l’angle supérieur gauche de la zone cliente de la boîte de dialogue.

</dd> <dt>

**adéquat**
</dt> <dd>

Type : **short**

</dd> <dd>

Largeur, en unités de boîte de dialogue, du contrôle.

</dd> <dt>

**CY**
</dt> <dd>

Type : **short**

</dd> <dd>

Hauteur, en unités de boîte de dialogue, du contrôle.

</dd> <dt>

**id**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Identificateur du contrôle.

</dd> <dt>

**windowClass**
</dt> <dd>

Type : **SZ \_ ou \_ ORD**

</dd> <dd>

Tableau de longueur variable d’éléments 16 bits qui spécifie la classe de fenêtre du contrôle. Si le premier élément de ce tableau a une valeur autre que 0xFFFF, le système traite le tableau comme une chaîne Unicode terminée par le caractère null qui spécifie le nom d’une classe de fenêtre inscrite.

Si le premier élément est 0xFFFF, le tableau a un élément supplémentaire qui spécifie la valeur ordinale d’une classe système prédéfinie. L’ordinal peut être l’une des valeurs Atom suivantes.



| Valeur                                                                             | Signification               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>0x0080</dt> </dl> | Bouton<br/>     |
| <dl> <dt>0x0081</dt> </dl> | Modifier<br/>       |
| <dl> <dt>0x0082</dt> </dl> | statique<br/>     |
| <dl> <dt>0x0083</dt> </dl> | Zone de liste<br/>   |
| <dl> <dt>0x0084</dt> </dl> | Scroll bar<br/> |
| <dl> <dt>0x0085</dt> </dl> | Combo box<br/>  |



 

</dd> <dt>

**title**
</dt> <dd>

Type : **SZ \_ ou \_ ORD**

</dd> <dd>

Tableau de longueur variable d’éléments 16 bits qui contient le texte initial ou l’identificateur de ressource du contrôle. Si le premier élément de ce tableau est 0xFFFF, le tableau a un élément supplémentaire qui spécifie la valeur ordinale d’une ressource, telle qu’une icône, dans un fichier exécutable. Vous pouvez utiliser un identificateur de ressource pour les contrôles, tels que les contrôles d’icône statique, qui chargent et affichent une icône ou une autre ressource plutôt que du texte. Si le premier élément est une valeur autre que 0xFFFF, le système traite le tableau comme une chaîne Unicode terminée par le caractère null qui spécifie le texte initial.

</dd> <dt>

**extraCount**
</dt> <dd>

Type : **Word**

</dd> <dd>

Nombre d’octets de données de création qui suivent ce membre. Si cette valeur est supérieure à zéro, les données de création commencent à la limite de **mot** suivante. Ces données de création peuvent avoir n’importe quelle taille et n’importe quel format. La procédure de fenêtre du contrôle doit être en mesure d’interpréter les données. Lorsque le système crée le contrôle, il passe un pointeur vers ces données dans le paramètre *lParam* du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) qu’il envoie au contrôle.

</dd> </dl>

## <a name="remarks"></a>Remarques

Un modèle étendu pour une boîte de dialogue se compose d’un en-tête [**DLGTEMPLATEEX**](dlgtemplateex.md) suivi d’une structure **DLGITEMTEMPLATEEX** pour chaque contrôle dans la boîte de dialogue.

Chaque structure **DLGITEMTEMPLATEEX** doit être alignée sur une limite **DWORD** . Les tableaux de **WindowClass** de longueur variable et de **titre** doivent être alignés sur les limites de **mots** . Le tableau de données de création, le cas échéant, doit être aligné sur une limite de **mot** .

Si vous spécifiez des chaînes de caractères dans les tableaux **WindowClass** et **title** , vous devez utiliser des chaînes Unicode. Utilisez la fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) pour générer des chaînes Unicode à partir de chaînes ANSI.

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

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATEEX**](dlgtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**création de WM \_**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Boîtes de dialogue](dialog-boxes.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**\_aide WM**](../shell/wm-help.md)
</dt> </dl>

 

