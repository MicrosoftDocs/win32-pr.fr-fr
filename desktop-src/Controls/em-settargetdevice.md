---
title: Message EM_SETTARGETDEVICE (RichEdit. h)
description: Définit l’appareil cible et la largeur de ligne utilisés pour \ 0034 ; ce que vous voyez est ce que vous obtenez \ 0034 ; (WYSIWYG) mise en forme dans un contrôle RichEdit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006349"
---
# <a name="em_settargetdevice-message"></a>\_Message SETTARGETDEVICE em

Définit l’appareil cible et la largeur de ligne utilisés pour la mise en forme de type « que vous obtenez » (WYSIWYG) dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

HDC pour l’appareil cible.

</dd> <dt>

*lParam* 
</dt> <dd>

Largeur de ligne à utiliser pour la mise en forme.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est égale à zéro si l’opération échoue, ou différente de zéro si elle réussit.

## <a name="remarks"></a>Notes

Le HDC pour l’imprimante par défaut peut être obtenu comme suit.


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



Si *lParam* est égal à zéro, aucun saut de ligne n’est créé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





