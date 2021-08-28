---
title: Message EM_FILELINEFROMCHAR (CommCtrl. h)
description: Obtient l’index de la ligne qui contient l’index de caractère spécifié dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_FILELINEFROMCHAR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d238117a9f2ba18ae838eec32d7dc2fa12ba0833f9cdee54ce2d1a2c998944
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915629"
---
# <a name="em_filelinefromchar-message"></a>\_Message FILELINEFROMCHAR em

Obtient l’index de la ligne qui contient l’index de caractère spécifié dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran. Un index de caractère est l’index de base zéro du caractère à partir du début du contrôle d’édition.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de caractère du caractère contenu dans la ligne dont le nombre doit être récupéré. Si ce paramètre a la valeur-1, **em \_ FILELINEFROMCHAR** récupère le numéro de ligne de la ligne active (la ligne qui contient le signe insertion) ou, s’il y a une sélection, le numéro de ligne de la ligne contenant le début de la sélection.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le numéro de ligne de base zéro de la ligne contenant l’index de caractère spécifié par *wParam*, indépendamment de la façon dont les lignes sont affichées à l’écran.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, 1809 \[ applications de bureau uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_FILELINEINDEX em**](em-filelineindex.md)
</dt> </dl>

 

 





