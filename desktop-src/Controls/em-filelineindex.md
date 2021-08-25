---
title: Message EM_FILELINEINDEX (CommCtrl. h)
description: Obtient l’index de caractère du premier caractère d’une ligne spécifiée dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c4bd1f21ee6bcdf7bec56828ea9c2996c837def614c0c537ef83ee053ebfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915609"
---
# <a name="em_filelineindex-message-commctrlh"></a>Message EM_FILELINEINDEX (CommCtrl. h)

Obtient l’index de caractère du premier caractère d’une ligne spécifiée dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran. Un index de caractère est l’index de base zéro du caractère à partir du début du contrôle d’édition.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Numéro de ligne de base zéro. La valeur-1 spécifie le numéro de la ligne active (la ligne qui contient le signe insertion).

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de caractère de la ligne spécifiée dans le paramètre *wParam* , indépendamment de la façon dont les lignes sont affichées à l’écran, ou a la valeur-1 si le numéro de ligne spécifié est supérieur au nombre de lignes dans le contrôle d’édition.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, 1809 \[ applications de bureau uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_FILELINEFROMCHAR em**](em-filelinefromchar.md)
</dt> </dl>

 

 





