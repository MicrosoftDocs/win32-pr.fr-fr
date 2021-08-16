---
description: 'La méthode CInstance :: GetWBEMINT64 définit une propriété d’entier 64 bits.'
audience: developer
ms.assetid: a1789091-ddb6-44f7-bc02-82e7c0209bf9
ms.tgt_platform: multiple
title: 'Méthodes CInstance :: SetWBEMINT64 (instance. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: dd13f10fb42c7b93ab7b86d6c8d940ee07b332b12667058006a5868f8fd21fe7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319695"
---
# <a name="cinstancesetwbemint64-methods"></a>CInstance :: SetWBEMINT64, méthodes

\[La classe [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La méthode [**CInstance :: GetWBEMINT64**](cinstance-getwbemint64.md) définit une propriété d’entier 64 bits.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                               | Description                                |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------|
| [**SetWBEMINT64 (LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))    | Définit une propriété de type entier 64 bits.<br/> |
| [**SetWBEMINT64 (LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong)) | Définit une propriété de type entier 64 bits.<br/> |
| [**SetWBEMINT64 (LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))  | Définit une propriété de type entier 64 bits.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>Instance. h (inclure FwCommon. h)</dt> </dl>                                                    |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CInstance**](/windows/win32/api/instance/nl-instance-cinstance)
</dt> </dl>

�

�
