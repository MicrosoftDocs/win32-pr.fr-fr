---
description: La méthode format met en forme et stocke une série de caractères et de valeurs dans une chaîne CHString.
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: 'CHString :: format, méthodes (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5432ac16b3e59b3f5e56d862a5bf66f5b23f732f74d586066584b6b937327830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319938"
---
# <a name="chstringformat-methods"></a>CHString :: format, méthodes

\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La méthode **format** met en forme et stocke une série de caractères et de valeurs dans une chaîne [**CHString**](chstring.md) .

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                              | Description                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Format (UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))       | Met en forme ce CHString en fonction de l’identificateur de ressource spécifié par **uint**.<br/> |
| [**Format (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---)) | Met en forme ce CHString en fonction du format spécifié par **LPCWSTR**.<br/>           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>ChString. h (inclure FwCommon. h)</dt> </dl>                                                    |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
