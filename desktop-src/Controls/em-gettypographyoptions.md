---
title: Message EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Retourne l’état actuel des options typographiques d’un contrôle RichEdit.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- EM_GETTYPOGRAPHYOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105106"
---
# <a name="em_gettypographyoptions-message"></a>\_Message GETTYPOGRAPHYOPTIONS em

Retourne l’état actuel des options typographiques d’un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne les options typographiques actuelles. Pour obtenir la liste des options, consultez [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).

## <a name="remarks"></a>Notes

Vous pouvez activer le saut de ligne avancé en envoyant le message [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) . Le saut de ligne avancé et normal peut également être activé automatiquement par le contrôle Rich Edit s’il est nécessaire pour certaines langues.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETTYPOGRAPHYOPTIONS em**](em-settypographyoptions.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[À propos des contrôles RichEdit](about-rich-edit-controls.md)
</dt> </dl>

 

 





