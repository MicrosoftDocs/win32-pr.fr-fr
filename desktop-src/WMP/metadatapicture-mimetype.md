---
title: MetadataPicture. mimeType
description: La propriété mimeType récupère le type MIME standard de l’image de métadonnées.
ms.assetid: dde541e3-ddbc-437e-a3a8-64a116e122e0
keywords:
- MetadataPicture. mimeType Lecteur Windows Media
topic_type:
- apiref
api_name:
- MetadataPicture.mimeType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9cfc6607bc121b18b7d8550576b84d251dd7f2812094a51464265e4135fa0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647699"
---
# <a name="metadatapicturemimetype"></a>MetadataPicture. mimeType

La propriété **MimeType** récupère le type MIME standard de l’image de métadonnées.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. **getItemInfoByType**( *nom*, *langue*, *index*). **MimeType**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="remarks"></a>Remarques

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

 

 





