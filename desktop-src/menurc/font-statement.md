---
title: FONT (instruction)
description: Définit la police avec laquelle le système dessinera du texte dans la boîte de dialogue. La police doit avoir été précédemment chargée ; par exemple, en appelant la fonction LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menus d’instructions de police et autres ressources
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad289923503866ba2bcd9338bb59a556d0e37cd0a839d4eede0f95a0bec5fd76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972068"
---
# <a name="font-statement"></a>FONT (instruction)

Définit la police avec laquelle le système dessinera du texte dans la boîte de dialogue. La police doit avoir été précédemment chargée ; par exemple, en appelant la fonction [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*
</dt> <dd>

Taille de la police, en points.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*certain*
</dt> <dd>

Nom de la police. Ce paramètre doit être placé entre guillemets (").

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*poids*
</dt> <dd>

Poids de la police dans la plage comprise entre 0 et 1000. Par exemple, 400 est normal et 700 est en gras. Si cette valeur est égale à 0, le poids par défaut est utilisé. Pour obtenir la liste des valeurs prédéfinies, consultez les valeurs **FW \_ \*** définies dans WinGDI. h.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*italique*
</dt> <dd>

Indique une police en italique si la valeur est TRUE.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*caractères*
</dt> <dd>

Jeu de caractères. Pour obtenir la liste des valeurs, consultez le membre **lfCharSet** de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> </dl>

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **font** :

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 