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
ms.openlocfilehash: ec7d221e0c352c4b9284ae5fe2d6f80e50da85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864946"
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

## <a name="remarks"></a>Notes

Une extension peut utiliser le message [**FM \_ GETSELCOUNT**](fm-getselcount.md) pour récupérer le nombre de fichiers sélectionnés.

## <a name="requirements"></a>Spécifications



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

 

 




