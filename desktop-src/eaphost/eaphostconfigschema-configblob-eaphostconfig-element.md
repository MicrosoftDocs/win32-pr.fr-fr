---
title: Élément ConfigBlob (EapHostConfig)
description: Est utilisé lorsque la configuration de la méthode est sous forme d’objet BLOB binaire plutôt que sous forme de chaîne de texte.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Élément ConfigBlob EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f0d3b928ebc6cd24a6d7102ea37a8d0ae980c54499f568d25ca224b1121a20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021639"
---
# <a name="configblob-eaphostconfig-element"></a>Élément ConfigBlob (EapHostConfig)

L’élément **ConfigBlob (EapHostConfig)** est utilisé lorsque la configuration de la méthode est sous forme d’objet blob binaire plutôt que sous forme de chaîne de texte.

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

L’élément **ConfigBlob** est défini par l’élément [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Remarques

Les éléments [**config**](eaphostconfigschema-config-eaphostconfig-element.md) et **ConfigBlob** ne peuvent pas être utilisés simultanément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





