---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer le nombre de fichiers sélectionnés dans la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche). Le nombre comprend les fichiers qui ont des noms de fichiers longs.
title: Message FM_GETSELCOUNTLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: ff0884e1b80e4a5a7e6c295bd449c8e1f6d069ced6c988f584108318a98c6891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094174"
---
# <a name="fm_getselcountlfn-message"></a>\_Message FM GETSELCOUNTLFN

Envoyé par une extension du gestionnaire de fichiers pour récupérer le nombre de fichiers sélectionnés dans la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche). Le nombre comprend les fichiers qui ont des noms de fichiers longs.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de fichiers sélectionnés.

## <a name="remarks"></a>Remarques

Seules les extensions qui prennent en charge les noms de fichiers longs (par exemple, les extensions prenant en charge le réseau) doivent utiliser ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETFILESEL FM**](fm-getfilesel.md)
</dt> <dt>

[**\_GETFILESELLFN FM**](fm-getfilesellfn.md)
</dt> <dt>

[**\_GETSELCOUNT FM**](fm-getselcount.md)
</dt> </dl>

 

 




