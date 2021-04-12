---
description: Les opérateurs d’assignation de la classe WBEMTime sont surchargés pour faciliter les conversions entre les différents formats d’heure d’exécution de Windows et ANSI C. Les différentes signatures surchargées sont répertoriées ci-dessous.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'WBEMTime :: Operator =, opérateurs (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320821"
---
# <a name="wbemtimeoperator-operators"></a>Opérateurs WBEMTime :: Operator =

\[La classe [**WBEMTime**](wbemtime.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

Les opérateurs d’assignation de la classe [**WBEMTime**](wbemtime.md) sont surchargés pour faciliter les conversions entre les différents formats d’heure d’exécution de Windows et ANSI C. Les différentes signatures surchargées sont répertoriées ci-dessous.

### <a name="overload-list"></a>Liste de surcharge



| Opérateur                                                                     | Description                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**opérateur = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Convertit un **BSTR** au format **WBEMTime** .<br/>         |
| [**Operator = (heure \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Convertit l' **heure \_ t** au format **WBEMTime** .<br/>        |
| [**Operator = (FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Convertit **fileTime** au format **WBEMTime** .<br/>       |
| [**Operator = (struct TM&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Convertit une structure **TM** au format **WBEMTime** .<br/> |
| [**Operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Convertit **SystemTime** au format **WBEMTime** .<br/>     |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
