---
title: Message EM_LINELENGTH (winuser. h)
description: Récupère la longueur, en caractères, d’une ligne dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_LINELENGTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844045"
---
# <a name="em_linelength-message"></a>\_Message LINELENGTH em

Récupère la longueur, en caractères, d’une ligne dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de caractère d’un caractère de la ligne dont la longueur doit être récupérée. Si ce paramètre est supérieur au nombre de caractères dans le contrôle, la valeur de retour est zéro.

Ce paramètre peut être-1. Dans ce cas, le message retourne le nombre de caractères non sélectionnés sur les lignes contenant les caractères sélectionnés. Par exemple, si la sélection est étendue à partir du quatrième caractère d’une ligne jusqu’au huitième caractère à partir de la fin de la ligne suivante, la valeur de retour est 10 (trois caractères sur la première ligne et sept sur la suivante).

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour les contrôles d’édition multiligne, la valeur de retour est la longueur, dans **TCHAR** s, de la ligne spécifiée par le paramètre *wParam* . Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères. Elle n’inclut pas le caractère de retour chariot à la fin de la ligne.

Pour les contrôles d’édition sur une seule ligne, la valeur de retour est la longueur, dans **TCHAR** s, du texte dans le contrôle d’édition.

Si *wParam* est supérieur au nombre de caractères dans le contrôle, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Utilisez le message [**em \_ LINEINDEX**](em-lineindex.md) pour récupérer un index de caractère pour un numéro de ligne donné au sein d’un contrôle d’édition multiligne.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LINEINDEX em**](em-lineindex.md)
</dt> </dl>

 

 





