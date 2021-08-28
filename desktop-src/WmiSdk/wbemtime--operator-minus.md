---
description: 'Opérateur de soustraction de classe WBEMTime (&\# 8211 ;) a été surchargé vers :'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'WBEMTime :: Operator-Operators (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7748020c1dcf1e332384c3a29c18b37da53e020f42d6cb608d9bf3233608aaaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120749"
---
# <a name="wbemtimeoperator--operators"></a>WBEMTime :: Operator-, opérateurs

\[La classe [**WBEMTime**](wbemtime.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

L’opérateur de soustraction de classe [**WBEMTime**](wbemtime.md) () a été surchargé vers :

-   Soustraire un intervalle de temps du temps d’un objet pour produire un nouvel objet d’heure qui contient le temps résultant.
-   Soustraire une heure de l’heure de l’objet pour produire un nouvel objet d’intervalle de temps qui contient la différence entre les deux fois.

### <a name="overload-list"></a>Liste de surcharge



| Opérateur                                                                         | Description                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**Operator-(WBEMTime&)**](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | Soustrait un **WBEMTime** d’un **WBEMTime**.<br/>                         |
| [**Operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_)) | Soustrait un [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) d’un **WBEMTime**.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
