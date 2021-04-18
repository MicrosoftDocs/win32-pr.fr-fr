---
description: Indique si une clé partagée est chiffrée.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: Élément protected (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515991"
---
# <a name="protected-sharedkey-element"></a>Élément protected (sharedKey)

L’élément protected (sharedKey) indique si une clé partagée est chiffrée.

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

L’élément est défini par l’élément [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Notes

Pour Windows Vista et Windows Server 2008, **protected** a toujours la valeur true si le profil a été récupéré à partir du magasin de profils (par exemple, en appelant [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).

Pour les profils destinés à être utilisés sur Windows XP avec Service Pack 3 (SP3) ou sur l’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2), **protected** doit avoir la valeur false.

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **protégé** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**sharedKey (sécurité)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




