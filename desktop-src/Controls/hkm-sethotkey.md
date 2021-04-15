---
title: Message HKM_SETHOTKEY (commctrl. h)
description: Définit la combinaison de touches d’accès rapide pour un contrôle de touche d’accès rapide.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- HKM_SETHOTKEY les contrôles de message Windows
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508490"
---
# <a name="hkm_sethotkey-message"></a>\_Message hkm SETHOTKEY

Définit la combinaison de touches d’accès rapide pour un contrôle de touche d’accès rapide.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) du [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est le code de la touche virtuelle de la touche d’accès rapide. Le [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) du **LOWORD** est le modificateur de clé qui indique les clés qui définissent une combinaison de touches d’accès rapide. Pour obtenir la liste des valeurs d’indicateur de modification, consultez la description du message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

