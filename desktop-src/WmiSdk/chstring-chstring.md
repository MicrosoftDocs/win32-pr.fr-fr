---
description: Chacun des constructeurs suivants Initialise un nouvel objet CHString avec les données spécifiées.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'CHString :: CHString, constructeurs (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203158"
---
# <a name="chstringchstring-constructors"></a>Constructeurs CHString :: CHString

\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

Chacun des constructeurs suivants Initialise un nouvel objet [**CHString**](chstring.md) avec les données spécifiées.

### <a name="overload-list"></a>Liste de surcharge



| Constructeur                                                                        | Description                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CHString()**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | Crée un objet CHString vide.<br/>                 |
| [**CHString (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))                              | Initialise avec la valeur LPCSTR.<br/>                |
| [**CHString (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))                            | Initialise avec la valeur LPCWSTR.<br/>               |
| [**CHString (WCHAR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))                        | Initialise avec des copies int de la valeur WCHAR.<br/>   |
| [**CHString (LPCWSTR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))                    | Initialise avec des copies int de la valeur LPCWSTR.<br/> |
| [**CHString (const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))            | Réplique le paramètre CHString.<br/>                |
| [**CHString (const signed char \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar)) | Initialise avec la valeur pointée par char \* .<br/>  |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>ChString. h (inclure FwCommon. h)</dt> </dl>                                                    |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
