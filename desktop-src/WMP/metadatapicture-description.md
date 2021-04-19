---
title: MetadataPicture. Description
description: La propriété Description récupère une description de l’image de métadonnées.
ms.assetid: 7a07a8a0-d50a-4951-95a8-c1285a1be737
keywords:
- MetadataPicture. Description du lecteur Windows Media
topic_type:
- apiref
api_name:
- MetadataPicture.description
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbacd8f2fbded3501100809de166651ca56cca8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539630"
---
# <a name="metadatapicturedescription"></a>MetadataPicture. Description

La propriété **Description** récupère une description de l’image de métadonnées.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. **getItemInfoByType**( *nom*, *langue*, *index*). **Description**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="remarks"></a>Notes

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





