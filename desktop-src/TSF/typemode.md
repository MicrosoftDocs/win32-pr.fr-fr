---
title: Énumération TYPEMODE (Softkbdc. h)
description: Les éléments de l’énumération TYPEMODE sont utilisés pour spécifier les modes de type disponibles pour un clavier conditionnel.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- TYPEMODE énumération Text Services Framework
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511745"
---
# <a name="typemode-enumeration"></a>Énumération TYPEMODE

Les éléments de l’énumération **TYPEMODE** sont utilisés pour spécifier les modes de type disponibles pour un clavier conditionnel.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**
</dt> <dd>

L’utilisateur peut cliquer sur les touches à l’écran pour taper du texte.

</dd> <dt>

<span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Pointez**
</dt> <dd>

L’utilisateur peut pointer vers une touche pour une période prédéfinie, et le caractère sélectionné est tapé automatiquement.

</dd> <dt>

<span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Cour**
</dt> <dd>

Le clavier logiciel balaie continuellement la zone d’entrée et met en surbrillance les régions où l’utilisateur peut appuyer sur une touche de raccourci ou utiliser un périphérique d’entrée de commutateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





