---
description: Indique si l’authentification 802.1 X est utilisée.
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: Élément useOneX (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cb327be4006e8da0074815a74e49d3ccdc5d3c84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021128"
---
# <a name="useonex-authencryption-element"></a>Élément useOneX (authEncryption)

L’élément useOneX (authEncryption) indique si l’authentification 802.1 X est utilisée.

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

L’élément est défini par l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **useOneX** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**authEncryption (sécurité)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




