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
ms.openlocfilehash: 2d9a3cd4e59f3800b91fedee446e927ab0ec39988474752561a04dace5572ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697589"
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

## <a name="return-value"></a>Valeur retournée

La valeur de retour est égale à zéro si l’opération échoue, ou différente de zéro si elle réussit.

## <a name="remarks"></a>Remarques

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





