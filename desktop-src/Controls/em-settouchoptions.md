---
title: Message EM_SETTOUCHOPTIONS (RichEdit. h)
description: Définit les options tactiles associées à un contrôle RichEdit.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f372d1e59a76ea13667e994534df1088fe1c78c51c30ac54db1b4dfeed2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048009"
---
# <a name="em_settouchoptions-message"></a>\_Message SETTOUCHOPTIONS em

Définit les options tactiles associées à un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Option Touch à définir. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                        | Signification                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | Affichez ou masquez les poignées de la pince tactile, en fonction de la valeur de *lParam*.<br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | Activez ou désactivez les handles de la pince tactile, en fonction de la valeur de *lParam*. Lorsque les descripteurs sont désactivés, ils sont masqués s’ils sont visibles et restent masqués jusqu’à ce qu’un message **\_ SETTOUCHOPTIONS em** change leur état. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Affectez la valeur **true** pour afficher/activer les poignées de sélection tactile, ou **false** pour masquer/désactiver les poignées de sélection tactile.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne la valeur zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTOUCHOPTIONS em**](em-settouchoptions.md)
</dt> </dl>

 

 





