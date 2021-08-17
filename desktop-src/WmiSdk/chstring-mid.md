---
description: La méthode Mid extrait une sous-chaîne de longueur nCount caractères à partir d’une chaîne CHString, en commençant à la position Npremier (de base zéro). La méthode retourne une copie de la sous-chaîne extraite.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'CHString :: Mid, méthodes (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cbe5b7fc6e3f0d4130e106217c46c82202c230f180dd4c90d09f90073dee08ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319841"
---
# <a name="chstringmid-methods"></a>CHString :: Mid, méthodes

\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La méthode **Mid** extrait une sous-chaîne de longueur *nCount* caractères à partir d’une chaîne [**CHString**](chstring.md) , en commençant à la position *npremier* (de base zéro). La méthode retourne une copie de la sous-chaîne extraite.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                        | Description                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**Mid (int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int)) | Extrait une sous-chaîne de longueur et de point de début spécifiés.<br/> |
| [**Mid (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))         | Extrait une sous-chaîne en commençant par int.<br/>                        |



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
