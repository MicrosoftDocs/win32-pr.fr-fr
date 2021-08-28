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
ms.openlocfilehash: ba798afaa418e5de49c48abdc8dac242a300a7228ffe27a76241f4cbabed5833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739079"
---
# <a name="config-eaphostconfig-element"></a>Élément config (EapHostConfig)

L’élément **config (EapHostConfig)** est utilisé lorsque la configuration de la méthode est au format texte XML et non pas dans un objet blob binaire.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

L’élément **config** est défini par l’élément [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Remarques

Les éléments **config** et [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) ne peuvent pas être utilisés simultanément.

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

 

 





