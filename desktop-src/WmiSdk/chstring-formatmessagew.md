---
description: La méthode FormatMessageW surchargée met en forme une chaîne de message.
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: 'CHString :: FormatMessageW, méthodes (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 53f8a9663994ffbc6b50aebddc7d9877c17c1067a074bcdddbe2fc79bc525e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050937"
---
# <a name="chstringformatmessagew-methods"></a>CHString :: FormatMessageW, méthodes

\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La méthode **FormatMessageW** surchargée met en forme une chaîne de message.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                              | Description                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**FormatMessageW (UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))       | Met en forme ce message en fonction de l’identificateur de ressource spécifié par **uint**.<br/> |
| [**FormatMessageW (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---)) | Met en forme cette chaîne de message en fonction du format spécifié par **LPCWSTR**.<br/>    |



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
