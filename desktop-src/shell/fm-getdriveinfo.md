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
ms.openlocfilehash: 39df15a4522e863fada40d3c964d709f40d2a26d01240aaefe51b09924b8c9ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459119"
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

## <a name="remarks"></a>Remarques

Si 0xFFFFFFFF est retourné dans le membre **dwTotalSpace** ou **dwFreeSpace** de la structure [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) , la bibliothèque d’extensions doit calculer la ou les valeurs.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




