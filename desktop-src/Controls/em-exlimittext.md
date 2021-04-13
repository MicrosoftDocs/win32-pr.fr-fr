---
title: Message EM_EXLIMITTEXT (RichEdit. h)
description: Définit une limite supérieure de la quantité de texte que l’utilisateur peut taper ou coller dans un contrôle RichEdit.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465895"
---
# <a name="em_exlimittext-message"></a>\_Message EXLIMITTEXT em

Définit une limite supérieure de la quantité de texte que l’utilisateur peut taper ou coller dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie la quantité maximale de texte qui peut être entrée. Si ce paramètre est égal à zéro, la valeur maximale par défaut est utilisée, qui est de 64 000 caractères. Un objet COM compte comme un caractère unique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La limite de texte définie par le message **em \_ EXLIMITTEXT** ne limite pas la quantité de texte que vous pouvez diffuser dans un contrôle RichEdit en utilisant le message de [**\_ flux em**](em-streamin.md) avec *lParam* défini sur le \_ texte DF. Toutefois, elle limite la quantité de texte que vous pouvez diffuser dans un contrôle RichEdit à l’aide du message de **\_ flux em** avec *lParam* défini sur DF \_ RTF.

Avant l’appel de **em \_ EXLIMITTEXT** , la limite par défaut de la quantité de texte qu’un utilisateur peut entrer est de 32 767 caractères.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_flux em**](em-streamin.md)
</dt> </dl>

 

 





