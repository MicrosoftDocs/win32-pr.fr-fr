---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer les informations de lecteur dans la fenêtre du gestionnaire de fichiers active.
title: Message FM_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991076"
---
# <a name="fm_getdriveinfo-message"></a>\_Message FM GETDRIVEINFO

Envoyé par une extension du gestionnaire de fichiers pour récupérer les informations de lecteur dans la fenêtre du gestionnaire de fichiers active.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

Adresse d’une structure [**\_ GETDRIVEINFO FMS**](fms-getdriveinfo.md) qui reçoit des informations sur le lecteur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro.

## <a name="remarks"></a>Notes

Si 0xFFFFFFFF est retourné dans le membre **dwTotalSpace** ou **dwFreeSpace** de la structure [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) , la bibliothèque d’extensions doit calculer la ou les valeurs.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




