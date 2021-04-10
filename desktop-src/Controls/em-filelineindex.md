---
title: Message EM_FILELINEINDEX (CommCtrl. h)
description: Obtient l’index de caractère du premier caractère d’une ligne spécifiée dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX les contrôles de message Windows
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
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104227"
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
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, 1809 \[ uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2019 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_FILELINEFROMCHAR em**](em-filelinefromchar.md)
</dt> </dl>

 

 





