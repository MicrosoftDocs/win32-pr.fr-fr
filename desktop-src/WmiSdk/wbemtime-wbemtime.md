---
description: Le constructeur de classe WBEMTime facilite les conversions entre les différents formats d’heure d’exécution de Windows et ANSI C.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'WBEMTime :: WBEMTime, constructeurs (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526962"
---
# <a name="wbemtimewbemtime-constructors"></a>Constructeurs WBEMTime :: WBEMTime

\[La classe [**WBEMTime**](wbemtime.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

Le constructeur de classe **WBEMTime** facilite les conversions entre les différents formats d’heure d’exécution de Windows et ANSI C.

### <a name="overload-list"></a>Liste de surcharge



| Constructeur                                                                 | Description                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                                   | Crée un objet de temps non initialisé.<br/>                          |
| [**WBEMTime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                           | Initialise le nouvel objet d’heure à la valeur du paramètre.<br/> |
| [**WBEMTime (const Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))        | Initialise le nouvel objet d’heure à la valeur du paramètre.<br/> |
| [**WBEMTime (const struct TM)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))    | Initialise le nouvel objet d’heure à la valeur du paramètre.<br/> |
| [**WBEMTime (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))     | Initialise le nouvel objet d’heure à la valeur du paramètre.<br/> |
| [**WBEMTime (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_)) | Initialise le nouvel objet d’heure à la valeur du paramètre.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
