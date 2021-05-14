---
description: Envoyé par une extension du gestionnaire de fichiers pour récupérer le type de fenêtre du gestionnaire de fichiers qui a le focus d’entrée.
title: Message FM_GETFOCUS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841410"
---
# <a name="fm_getfocus-message"></a>\_Message FM getFocus

Envoyé par une extension du gestionnaire de fichiers pour récupérer le type de fenêtre du gestionnaire de fichiers qui a le focus d’entrée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le type de fenêtre du gestionnaire de fichiers qui a le focus d’entrée. Il peut avoir l’une des valeurs suivantes.



| Code de retour                                                                                    | Description                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**FMFOCUS \_ dir**</dt> </dl>    | Partie répertoire d’une fenêtre de répertoire.<br/> |
| <dl> <dt>**\_arbre FMFOCUS**</dt> </dl>   | Partie de l’arborescence d’une fenêtre de répertoire.<br/>      |
| <dl> <dt>**\_lecteurs FMFOCUS**</dt> </dl> | Barre de lecteur d’une fenêtre de répertoire.<br/>         |
| <dl> <dt>**\_recherche FMFOCUS**</dt> </dl> | Fenêtre des résultats de la recherche.<br/>                   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



 

 




