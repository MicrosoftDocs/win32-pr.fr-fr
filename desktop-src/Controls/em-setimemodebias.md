---
title: Message EM_SETIMEMODEBIAS (RichEdit. h)
description: Définissez le décalage du mode de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS les contrôles de Windows de message
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
ms.openlocfilehash: b4812c21558fba07be2709c0fd1a011f31d79fad17e0b4146fa0c7d65843a087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672669"
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

## <a name="remarks"></a>Remarques

Lorsque l’IME génère une liste de choix alternatifs pour un jeu de caractères, ce message définit les critères selon lesquels certains des choix s’affichent en haut de la liste.

Pour définir le décalage du mode Text Services Framework (TSF), utilisez [**em \_ SETCTFMODEBIAS**](em-setctfmodebias.md).

L’application doit appeler [**em \_ ISIME**](em-isime.md) avant d’appeler cette fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_ISIME em**](em-isime.md)
</dt> <dt>

[**\_SETCTFMODEBIAS em**](em-setctfmodebias.md)
</dt> </dl>

 

 





