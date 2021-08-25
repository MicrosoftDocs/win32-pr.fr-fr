---
title: Message EM_FORMATRANGE (RichEdit. h)
description: Met en forme une plage de texte dans un contrôle RichEdit pour un appareil spécifique.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941aceb8c8f91657c7f78aba3d83a627fc413ed20d71217c933c6fba9b6f39e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049349"
---
# <a name="em_formatrange-message"></a>\_Message FormatRange em

Met en forme une plage de texte dans un contrôle RichEdit pour un appareil spécifique.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie s’il faut restituer le texte. Si ce paramètre n’est pas égal à zéro, le texte est rendu. Dans le cas contraire, le texte est uniquement mesuré.

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) contenant des informations sur le périphérique de sortie, ou **null** pour libérer des informations mises en cache par le contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne l’index du dernier caractère qui tient dans la région, plus 1.

## <a name="remarks"></a>Remarques

Ce message est généralement utilisé pour mettre en forme le contenu d’un contrôle RichEdit pour un périphérique de sortie tel qu’une imprimante.

Après avoir utilisé ce message pour mettre en forme une plage de texte, il est important de libérer les informations mises en cache en renvoyant **\_ FormatRange em** , mais avec *lParam* défini sur **null**; sinon, une fuite de mémoire se produit. De même, après avoir utilisé ce message pour un appareil, vous devez libérer les informations mises en cache avant de l’utiliser à nouveau pour un autre appareil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_DISPLAYBAND em**](em-displayband.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Impression de contrôles RichEdit](printing-rich-edit-controls.md)
</dt> </dl>

 

 





