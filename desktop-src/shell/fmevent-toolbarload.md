---
description: Envoyé à une DLL d’extension lorsque le gestionnaire de fichiers charge sa barre d’outils. Ce message permet à une DLL d’extension d’ajouter un bouton à la barre d’outils du gestionnaire de fichiers.
title: Message FMEVENT_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: c4195acedbd696679a2deea2f4d6e268717566d1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841270"
---
# <a name="fmevent_toolbarload-message"></a>\_Message FMEVENT TOOLBARLOAD

Envoyé à une DLL d’extension lorsque le gestionnaire de fichiers charge sa barre d’outils. Ce message permet à une DLL d’extension d’ajouter un bouton à la barre d’outils du gestionnaire de fichiers.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lpfmstbl* 
</dt> <dd>

Adresse d’une structure [**FMS \_ TOOLBARLOAD**](fms-toolbarload.md) . Si la DLL d’extension ajoute un bouton à la barre d’outils dans le gestionnaire de fichiers, la DLL doit remplir la structure avec des informations sur le bouton.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Une DLL d’extension doit retourner la **valeur true** pour ajouter le bouton à la barre d’outils. Si la DLL retourne la **valeur false**, le gestionnaire de fichiers n’ajoute pas le bouton.

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

 

 




