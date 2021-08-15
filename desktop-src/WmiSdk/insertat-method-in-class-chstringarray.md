---
description: La méthode InsertAt insère un élément (ou plusieurs copies d’un élément) ou tous les éléments d’un autre tableau à un index spécifié.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: 'CHStringArray :: InsertAt, méthodes (ChStrArr. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 75332e300987233c0a6f3d6755d27fd7c305a7d86fb6cd9a6143c417222c0dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097249"
---
# <a name="chstringarrayinsertat-methods"></a>CHStringArray :: InsertAt, méthodes

\[La classe [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La méthode **InsertAt** insère un élément (ou plusieurs copies d’un élément) ou tous les éléments d’un autre tableau à un index spécifié.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                               | Description                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**InsertAt (int, LPCWSTR, int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))       | Insère un ou plusieurs éléments à un index spécifié dans un tableau.<br/>                                               |
| [**InsertAt (int, CHStringArray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray)) | Insère tous les éléments d’un autre [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) à un index spécifié dans un tableau.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>ChStrArr. h (inclure FwCommon. h)</dt> </dl>                                                    |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

�

�
