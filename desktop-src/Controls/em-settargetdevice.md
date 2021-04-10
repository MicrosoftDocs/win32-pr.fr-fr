---
title: Message EM_SETTARGETDEVICE (RichEdit. h)
description: Définit l’appareil cible et la largeur de ligne utilisés pour \ 0034 ; ce que vous voyez est ce que vous obtenez \ 0034 ; (WYSIWYG) mise en forme dans un contrôle RichEdit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104215"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





