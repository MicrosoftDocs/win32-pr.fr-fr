---
title: Message EM_SETCARETINDEX (CommCtrl. h)
description: Définit la valeur d’index de base zéro de la position du signe insertion dans un contrôle d’édition.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETCARETINDEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 8b80202ed5294828441abcfa66a914514e31944902e52926de7fa3af92794b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799959"
---
# <a name="em_setcaretindex-message"></a>\_Message SETCARETINDEX em

Définit la valeur d’index de base zéro de la position du signe insertion dans un contrôle d’édition.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nouvelle valeur d’index de base zéro de la position du signe insertion.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si l’index est en dehors de la plage du texte d’un contrôle d’édition, l’index est ajusté pour s’ajuster à la plage du texte.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, 1809 \[ applications de bureau uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETCARETINDEX em**](em-getcaretindex.md)
</dt> </dl>

 

 





