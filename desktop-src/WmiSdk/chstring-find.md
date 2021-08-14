---
description: La méthode Find recherche dans une chaîne la première correspondance d’une sous-chaîne.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: 'CHString :: Find, méthodes (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a7f326b202d107dc192683517508446b3c785266c675e5cf27d92577311d453a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319993"
---
# <a name="chstringfind-methods"></a>CHString :: Find, méthodes

\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La méthode **Find** recherche dans une chaîne la première correspondance d’une sous-chaîne.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                          | Description                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| [**Rechercher (WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))     | Recherche les **WSTR** dans cette chaîne.<br/>    |
| [**Rechercher (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr)) | Recherche les **LPCWSTR** dans cette chaîne.<br/> |



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
