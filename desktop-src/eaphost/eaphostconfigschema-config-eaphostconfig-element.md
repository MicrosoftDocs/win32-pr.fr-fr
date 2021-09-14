---
title: Élément config (EapHostConfig)
description: Est utilisé lorsque la configuration de la méthode est au format texte XML au lieu d’un objet BLOB binaire.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Élément config EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118385"
---
# <a name="config-eaphostconfig-element"></a>Élément config (EapHostConfig)

L’élément **config (EapHostConfig)** est utilisé lorsque la configuration de la méthode est au format texte XML et non pas dans un objet blob binaire.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

L’élément **config** est défini par l’élément [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Notes

Les éléments **config** et [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) ne peuvent pas être utilisés simultanément.

## <a name="requirements"></a>Spécifications



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

 

 





