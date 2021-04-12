---
description: 'La méthode CInstance :: GetWBEMINT64 récupère une propriété de type entier 64 bits.'
ms.assetid: b51d0c51-3b72-4358-8fc3-d1dbc298b4d9
ms.tgt_platform: multiple
title: 'Méthodes CInstance :: GetWBEMINT64 (instance. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 3d7b7a9f4091125bd722aea197c1670defb0c21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319686"
---
# <a name="cinstancegetwbemint64-methods"></a>CInstance :: GetWBEMINT64, méthodes

\[La classe [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La méthode **CInstance :: GetWBEMINT64** récupère une propriété de type entier 64 bits.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                   | Description                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------|
| [**GetWBEMINT64 (LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))   | Récupère une propriété de type entier 64 bits.<br/> |
| [**GetWBEMINT64 (LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_)) | Récupère une propriété de type entier 64 bits.<br/> |
| [**GetWBEMINT64 (LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_)) | Récupère une propriété de type entier 64 bits.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>Instance. h (inclure FwCommon. h)</dt> </dl>                                                    |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

