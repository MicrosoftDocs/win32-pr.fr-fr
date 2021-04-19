---
title: AcceptServerName (PeapExtensionsType), élément (EAPHost)
description: Indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément ServerNames (ServerValidationParameters). | Élément AcceptServerName (PeapExtensionsType)
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- élément EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba4874b7c8761f35fa93387b23eaf5463a31bcf4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314602"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a>AcceptServerName (PeapExtensionsType), élément (EAPHost)

L’élément **AcceptServerName (PeapExtensionsType)** indique si le nom du serveur est validé par rapport à la chaîne de nom spécifiée dans l’élément [**serverNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

L’élément est défini par l’élément [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .

## <a name="remarks"></a>Notes

L’élément **AcceptServerName** est facultatif.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



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

[Schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[**AcceptServerName**](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





