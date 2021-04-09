---
title: Message TB_SAVERESTORE (commctrl. h)
description: Envoyer ce message pour lancer l’enregistrement ou la restauration de l’état d’une barre d’outils.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- TB_SAVERESTORE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843058"
---
# <a name="tb_saverestore-message"></a>TO \_ SAVERESTORE message

Envoyer ce message pour lancer l’enregistrement ou la restauration de l’état d’une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Enregistrer ou restaurer l’indicateur. Si ce paramètre a la **valeur true**, les informations sont enregistrées. Si la **valeur est false**, les informations sont restaurées.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) qui spécifie la clé de Registre, la sous-clé et le nom de la valeur pour les informations d’état de la barre d’outils.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Pour la version 4,72 et les versions antérieures, afin d’utiliser ce message pour enregistrer ou restaurer une barre d’outils, la fenêtre parente du contrôle ToolBar doit implémenter un gestionnaire pour le code de notification [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) . La barre d’outils émet cette notification pour extraire des informations sur chaque bouton lors de sa restauration.

La version 5,80 comprend une nouvelle option d’enregistrement/restauration. Au début du processus, lorsque chaque bouton est enregistré ou restauré, votre application reçoit une notification [TBN \_ Save](tbn-save.md) ou [TBN \_ Restore](tbn-restore.md) . Pour utiliser cette option, vous devez implémenter des gestionnaires de notification pour fournir à l’interpréteur de commandes la bitmap et les informations d’État dont il a besoin pour enregistrer ou restaurer l’état de la barre d’outils.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ SAVERESTOREW** (Unicode) et **to \_ SAVERESTOREA** (ANSI)<br/>             |



 

 





