---
title: Message LM_HITTEST (commctrl. h)
description: Détermine si l’utilisateur a cliqué sur le lien spécifié.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- LM_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843101"
---
# <a name="lm_hittest-message"></a>\_Message LM HITTEST

Détermine si l’utilisateur a cliqué sur le lien spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit avoir la **valeur null**.</dd> <dt>

*lParam* 
</dt> <dd>Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> à remplir avec des informations sur le lien sur lequel l’utilisateur a cliqué, le cas échéant. </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’utilisateur a cliqué sur un lien ; sinon, retourne **false**.

## <a name="remarks"></a>Notes

Si le message **LM \_ HITTEST** est correctement exécuté, le système se remplit en [**litem. iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) et en **litem. szID**. Si le message **LM \_ HITTEST** échoue, ne supposez pas que toutes les informations contenues dans **litem** sont valides.

> [!Note]  
> Pour utiliser cette API, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





