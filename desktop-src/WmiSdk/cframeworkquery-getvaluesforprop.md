---
description: La méthode GetValuesForProp retourne toutes les valeurs d’une propriété particulière qui sont générées par cette propriété telle qu’elle apparaît dans la requête.
audience: developer
ms.assetid: b5ed4b48-f622-4a55-897d-d800ada0270f
ms.tgt_platform: multiple
title: 'CFrameworkQuery :: GetValuesForProp, méthodes (FrQuery. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b5fd9dbc22289843141c517203809045abbf05a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203973"
---
# <a name="cframeworkquerygetvaluesforprop-methods"></a>CFrameworkQuery :: GetValuesForProp, méthodes

\[La classe [**CFrameworkQuery**](/windows/win32/api/frquery/nl-frquery-cframeworkquery) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La méthode **GetValuesForProp** retourne toutes les valeurs d’une propriété particulière qui sont générées par cette propriété telle qu’elle apparaît dans la requête.

Par exemple, un appel à **GetValuesForProp**(L "Name", sa) retourne le tableau *sa*, qui contient toutes les valeurs de « Name » qui requièrent que les instances soient renvoyées pour satisfaire la requête. Si *sa* contient {"a", "b"}, toutes les instances où "Name = a" et toutes les instances où "Name = b" doivent être renvoyées pour répondre complètement à la requête.

Si les contraintes sur « Name » ne sont pas suffisamment restrictives, un tableau *sa* vide est retourné.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                             | Description                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetValuesForProp (CHStringArray&, LPCWSTR)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_chstringarray_))                      | Retourne toutes les valeurs d’une propriété particulière qui sont générées par cette propriété telle qu’elle apparaît dans la requête.<br/> |
| [**GetValuesForProp (LPCWSTR, std :: Vector &lt; \_ bstr \_ t &gt;&)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_std-vector__bstr_t__)) | Retourne toutes les valeurs d’une propriété particulière qui sont générées par cette propriété telle qu’elle apparaît dans la requête.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>FrQuery. h (inclure FwCommon. h)</dt> </dl>                                                     |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
