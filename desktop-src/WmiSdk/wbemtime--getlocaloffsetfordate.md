---
description: La méthode GetLocalOffsetForDate retourne le décalage en minutes (+ ou &\# 8211 ;) entre l’heure GMT et l’heure locale pour l’heure fournie dans l’argument.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'WBEMTime :: GetLocalOffsetForDate, méthodes (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866861"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a>WBEMTime :: GetLocalOffsetForDate, méthodes

\[La classe [**WBEMTime**](wbemtime.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La méthode **GetLocalOffsetForDate** retourne le décalage en minutes (+ ou) entre l’heure GMT et l’heure locale pour l’heure fournie dans l’argument.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                           | Description                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| [**GetLocalOffsetForDate (heure \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))         | L’argument est une référence à une **heure \_ t**.<br/>  |
| [**GetLocalOffsetForDate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))     | L’argument est un pointeur vers **fileTime**.<br/>   |
| [**GetLocalOffsetForDate (struct TM \* )**](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | L’argument est un pointeur vers la structure **TM** .<br/> |
| [**GetLocalOffsetForDate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime)) | L’argument est un pointeur vers un **SystemTime**.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
