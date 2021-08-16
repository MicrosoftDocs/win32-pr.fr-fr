---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer des informations sur un fichier sélectionné à partir de la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche). Le fichier sélectionné peut avoir un nom de fichier long.
title: Message FM_GETFILESELLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: 2074fb1e631edf1795b8f0d15ea9f0d40e90556d527899873ef88195c2367576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860766"
---
# <a name="fm_getfilesellfn-message"></a>\_Message FM GETFILESELLFN

Envoyé par une extension du gestionnaire de fichiers pour récupérer des informations sur un fichier sélectionné à partir de la fenêtre du gestionnaire de fichiers active (la fenêtre répertoire ou la fenêtre résultats de la recherche). Le fichier sélectionné peut avoir un nom de fichier long.

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

Seules les extensions qui prennent en charge les noms de fichiers longs (par exemple, les extensions prenant en charge le réseau) doivent utiliser ce message.

Une extension peut utiliser le message [**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md) pour récupérer le nombre de fichiers sélectionnés.

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

[**\_GETFILESEL FM**](fm-getfilesel.md)
</dt> <dt>

[**\_GETSELCOUNT FM**](fm-getselcount.md)
</dt> </dl>

 

 




