---
title: Message EM_SETIMEMODEBIAS (RichEdit. h)
description: Définissez le décalage du mode de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465710"
---
# <a name="em_setimemodebias-message"></a>\_Message SETIMEMODEBIAS em

Définissez le décalage du mode de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur de décalage du mode IME. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                        | Signification                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**\_SMODE IMF \_ PLAURALCLAUSE**</dt> </dl> | Définit le décalage du mode IME sur Name.<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**\_SMODE IMF \_ aucun**</dt> </dl>                            | Aucun décalage.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Il doit s’agir de la même valeur que *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne le nouveau paramètre de décalage du mode IME.

## <a name="remarks"></a>Notes

Lorsque l’IME génère une liste de choix alternatifs pour un jeu de caractères, ce message définit les critères selon lesquels certains des choix s’affichent en haut de la liste.

Pour définir le décalage du mode Text Services Framework (TSF), utilisez [**em \_ SETCTFMODEBIAS**](em-setctfmodebias.md).

L’application doit appeler [**em \_ ISIME**](em-isime.md) avant d’appeler cette fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_ISIME em**](em-isime.md)
</dt> <dt>

[**\_SETCTFMODEBIAS em**](em-setctfmodebias.md)
</dt> </dl>

 

 





