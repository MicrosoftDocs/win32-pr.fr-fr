---
title: Message EM_SETPAGEROTATE (RichEdit. h)
description: Définit la disposition du texte pour un contrôle RichEdit.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- EM_SETPAGEROTATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006369"
---
# <a name="em_setpagerotate-message"></a>\_Message SETPAGEROTATE em

\[**Em \_ SETPAGEROTATE** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Définit la disposition du texte pour un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur de disposition du texte. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                       | Signification                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <dt>**EPR \_ 0**</dt> </dl>       | Le texte est écrit de gauche à droite et de haut en bas.<br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <dt>**EPR \_ 90**</dt> </dl>    | Le texte est écrit de bas en haut et de gauche à droite.<br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <dt>**EPR \_ 180**</dt> </dl> | Le texte est écrit de droite à gauche et de bas en haut.<br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <dt>**EPR \_ 270**</dt> </dl> | Le texte est écrit de haut en bas et de droite à gauche.<br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <dt>**\_se EPR**</dt> </dl>    | **Windows 8 :** Les flux de texte de haut en bas et de gauche à droite (disposition du texte mongol).<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est la nouvelle valeur de disposition du texte.

## <a name="remarks"></a>Notes

Ce message définit la disposition du texte pour l’ensemble du document. Toutefois, le contenu incorporé n’est pas pivoté et doit être pivoté séparément par l’application.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETPAGEROTATE em**](em-getpagerotate.md)
</dt> </dl>

 

 





