---
description: Se produit lorsque l’utilisateur appuie sur une touche et la relâche, tandis que le contrôle InkEdit a le focus.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Événement InkEdit. KeyPress (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523271"
---
# <a name="inkeditkeypress-event"></a>Événement InkEdit. KeyPress

Se produit lorsque l’utilisateur appuie sur une touche et la relâche, tandis que le contrôle [InkEdit](inkedit-control-reference.md) a le focus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Char* 
</dt> <dd>

Entier qui retourne un code de KeyANSI numérique standard. Le paramètre *char* est passé par référence ; la modification de celui-ci envoie un caractère différent au contrôle. La modification du paramètre *char* en 0 annule l’événement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cet événement a la valeur, il retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** . L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeKeyPress.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**KeyOut, événement \[ InkEdit, contrôle\]**](inkedit-keydown.md)
</dt> <dt>

[**Événement KeyUp \[ contrôle InkEdit\]**](inkedit-keyup.md)
</dt> </dl>

 

