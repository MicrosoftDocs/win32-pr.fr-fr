---
title: Message EM_SETTOUCHOPTIONS (RichEdit. h)
description: Définit les options tactiles associées à un contrôle RichEdit.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS les contrôles de message Windows
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
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465702"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTOUCHOPTIONS em**](em-settouchoptions.md)
</dt> </dl>

 

 





