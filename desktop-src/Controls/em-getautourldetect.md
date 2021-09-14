---
title: Message EM_GETAUTOURLDETECT (RichEdit. h)
description: Indique si la détection d’URL automatique est activée dans le contrôle Rich Edit.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- EM_GETAUTOURLDETECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006501"
---
# <a name="em_getautourldetect-message"></a>\_Message GETAUTOURLDETECT em

Indique si la détection d’URL automatique est activée dans le contrôle Rich Edit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la détection d’URL automatique est active, la valeur de retour est 1.

Si la détection d’URL automatique est inactive, la valeur de retour est 0.

## <a name="remarks"></a>Notes

Lorsque la détection d’URL automatique est activée, la modification riche de Microsoft vérifie constamment le texte tapé pour une URL valide. La modification complète reconnaît les URL qui commencent par ces préfixes :

-   http:
-   file :
-   mailto:
-   FTP
-   https
-   Gopher
-   NNTP
-   prospero:
-   Mission
-   concernant
-   WAIS
-   programme

La modification complète reconnaît également les noms de chemins standard qui commencent par \\ \\ . Quand la modification complète localise une URL, elle modifie la couleur du texte de l’URL, souligne le texte et notifie le client à l’aide de l' [ \_ éditeur de liens](en-link.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[en \_ lien](en-link.md)
</dt> </dl>

 

 





