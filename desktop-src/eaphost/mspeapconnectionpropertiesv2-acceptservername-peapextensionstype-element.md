---
title: Élément AcceptServerName (PeapExtensionsType)
description: L’élément AcceptServerName (PeapExtensionsType) indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans les nom_serveur dans le schéma mspeapconnectionpropertiesv2.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Élément AcceptServerName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b608629c9eb9d3e3fb592ead73ddc0ba9545e6b92a642adf4ce76bb0524b57ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086038"
---
# <a name="acceptservername-peapextensionstype-element"></a>Élément AcceptServerName (PeapExtensionsType)

L’élément **AcceptServerName (PeapExtensionsType)** indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément [**serverNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

L’élément **AcceptServerName** est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

## <a name="remarks"></a>Remarques

L’élément **AcceptServerName** est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





