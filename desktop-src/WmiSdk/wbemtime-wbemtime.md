---
description: le constructeur de classe WBEMTime facilite les conversions entre différents Windows et les formats d’heure d’exécution C ANSI.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'WBEMTime :: WBEMTime, constructeurs (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ac02e3ee2a7a77ed1cc2cc9157b0d6c191563f234bf594cb53029a76e76f0137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757619"
---
# <a name="wbemtimewbemtime-constructors"></a>Constructeurs WBEMTime :: WBEMTime

\[La classe [**WBEMTime**](wbemtime.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

le constructeur de classe **WBEMTime** facilite les conversions entre différents Windows et les formats d’heure d’exécution C ANSI.

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
| Serveur minimal pris en charge<br/> | Windows Serveur 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
