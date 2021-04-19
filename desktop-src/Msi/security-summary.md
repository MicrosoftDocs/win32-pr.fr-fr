---
description: La propriété Résumé de sécurité indique si le package doit être ouvert en lecture seule.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Propriété Résumé de sécurité
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542716"
---
# <a name="security-summary-property"></a>Propriété Résumé de sécurité

La propriété **Résumé de sécurité** indique si le package doit être ouvert en lecture seule. L’outil d’édition de base de données ne doit pas modifier une base de données en lecture seule appliquée et doit émettre un avertissement lors des tentatives de modification d’une base de données en lecture seule recommandée. Les valeurs suivantes de cette propriété s’appliquent aux fichiers Windows Installer.



| Valeur | Description           |
|-------|-----------------------|
| 0     | Pas de restriction        |
| 2     | Lecture seule recommandée |
| 4     | En lecture seule forcé    |



 

Cette propriété doit être définie sur lecture seule recommandée (2) pour une base de données d’installation et pour application en lecture seule (4) pour une transformation ou un correctif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Descriptions des propriétés de synthèse](summary-property-descriptions.md)
</dt> </dl>

 

 




