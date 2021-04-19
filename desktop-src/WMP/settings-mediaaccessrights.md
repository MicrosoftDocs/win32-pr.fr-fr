---
title: Paramètres. mediaAccessRights
description: La propriété mediaAccessRights récupère une valeur indiquant les droits actuellement octroyés pour l’accès à la bibliothèque.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Settings. mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528492"
---
# <a name="settingsmediaaccessrights"></a>Paramètres. mediaAccessRights

La propriété **mediaAccessRights** récupère une valeur indiquant les droits actuellement octroyés pour l’accès à la bibliothèque.

## <a name="syntax"></a>Syntaxe

Player. Settings. mediaAccessRights

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.



| Valeur | Description                      |
|-------|----------------------------------|
| aucun  | Droits d’accès à l’élément actuel uniquement. |
| lire  | Droits d’accès en lecture uniquement.         |
| complet  | Droits d’accès en lecture/écriture.        |



 

## <a name="remarks"></a>Notes

Une page Web doit tout d’abord demander l’autorisation à l’utilisateur de lire des informations ou d’écrire des données dans la bibliothèque. Cela signifie que certaines méthodes, propriétés et événements seront inaccessibles à partir du code si les droits d’accès appropriés n’ont pas été accordés. Pour obtenir les droits d’accès, l’application appelle des *paramètres*. **requestMediaAccessRights**, en passant un paramètre qui spécifie le niveau de droits d’accès souhaité.

**Windows Media Player 10 Mobile**: cette propriété retourne toujours **Full**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Settings (objet)**](settings-object.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





