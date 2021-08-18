---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer des informations sur un fichier sélectionné à partir de la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche).
title: Message FM_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: a801b22fd23b4a67eaf01efbbef574e24a74a2e1304f3a65678c4197517a4a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094184"
---
# <a name="fm_getfilesel-message"></a>\_Message FM GETFILESEL

Envoyé par une extension du gestionnaire de fichiers pour récupérer des informations sur un fichier sélectionné à partir de la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* 
</dt> <dd>

Index de base zéro du fichier sélectionné à récupérer.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

Adresse d’une structure [**\_ GETFILESEL FMS**](fms-getfilesel.md) qui reçoit des informations sur la sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de base zéro du fichier sélectionné qui a été récupéré.

## <a name="remarks"></a>Remarques

Une extension peut utiliser le message [**FM \_ GETSELCOUNT**](fm-getselcount.md) pour récupérer le nombre de fichiers sélectionnés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**\_GETFILESELLFN FM**](fm-getfilesellfn.md)
</dt> <dt>

[**\_GETSELCOUNTLFN FM**](fm-getselcountlfn.md)
</dt> </dl>

 

 




