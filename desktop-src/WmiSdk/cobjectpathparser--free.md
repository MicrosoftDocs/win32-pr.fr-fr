---
description: Méthode surchargée qui libère la mémoire qui contient le chemin d’accès.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: 'CObjectPathParser :: Free, méthodes (ObjPath. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 0e7e5e366d96d4c8b5c6d82f177a480114c5d6356759c8db46389c809aea7137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819805"
---
# <a name="cobjectpathparserfree-methods"></a>CObjectPathParser :: Free, méthodes

\[La classe [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

Méthode surchargée qui libère la mémoire qui contient le chemin d’accès.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                     | Description                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Gratuit (LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))                     | Libère la mémoire qui contient le chemin d’accès non analysé.<br/>                      |
| [**Gratuit (ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath)) | Libère la mémoire qui contient la structure qui a le chemin d’accès analysé.<br/> |



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>ObjPath. h (inclure ObjPath. h)</dt> </dl>                                                      |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

�

�
