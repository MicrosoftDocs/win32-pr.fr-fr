---
title: Styles étendus de contrôle onglet (CommCtrl. h)
description: Le contrôle onglet prend désormais en charge les styles étendus. Ces styles sont manipulés à l’aide des \_ messages TCM GETEXTENDEDSTYLE et TCM \_ SETEXTENDEDSTYLE et ne doivent pas être confondus avec les styles de fenêtre étendus passés à CreateWindowEx.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532848"
---
# <a name="tab-control-extended-styles"></a>Styles étendus de contrôle onglet

Le contrôle onglet prend désormais en charge les styles étendus. Ces styles sont manipulés à l’aide des messages [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) et [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) et ne doivent pas être confondus avec les styles de fenêtre étendus passés à [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).



| Constante                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**TCS \_ ex \_ FLATSEPARATORS**</dt> </dl> | [Version 4,71](common-control-versions.md). Le contrôle onglet dessine des séparateurs entre les éléments d’onglet. Ce style étendu affecte uniquement les contrôles d’onglet qui ont les [**\_ boutons TCS**](tab-control-styles.md) et les styles [**\_ FLATBUTTONS TCS**](tab-control-styles.md) . Par défaut, la création du contrôle onglet avec le style **\_ FLATBUTTONS TCS** définit ce style étendu. Si vous n’avez pas besoin de séparateurs, vous devez supprimer ce style étendu après avoir créé le contrôle.<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**TCS \_ ex \_ REGISTERDROP**</dt> </dl>       | [Version 4,71](common-control-versions.md). Le contrôle onglet génère des codes de notification [TCN \_ GETOBJECT](tcn-getobject.md) pour demander un objet cible de dépôt lorsqu’un objet est glissé sur les éléments d’onglet dans le contrôle. L’application doit appeler [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) avant de définir ce style. <br/>                                                                                                                                               |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

