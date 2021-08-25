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
ms.openlocfilehash: 961f1b6be52da97ada2c230579ac281652a07fcbae67ac32d2399eb2968b1946
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912569"
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

## <a name="requirements"></a>Configuration requise



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

 

 




