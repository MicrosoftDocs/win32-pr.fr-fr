---
description: Indique si le mode FIPS est activé.
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Élément FIPSMode (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752301"
---
# <a name="fipsmode-authencryption-element"></a>Élément FIPSMode (authEncryption)

L’élément **FipsMode** (authEncryption) indique si le mode FIPS (Federal Information Processing Standards) est activé. Lorsqu’une connexion sans fil fonctionne en mode FIPS, le niveau de sécurité de la connexion est conforme à la norme FIPS 140-2. Pour plus d’informations sur FIPS, consultez la [page d’hébergement de FIPS](https://www.itl.nist.gov/fipspubs/).

Cet élément est facultatif. Si cet élément n’est pas spécifié dans un profil, le mode FIPS n’est pas activé.

**FipsMode** peut avoir la valeur true uniquement lorsque les conditions suivantes sont remplies :

-   L’élément [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) a la valeur `ESS` (autrement dit, la connexion est une connexion d’infrastructure).
-   L’élément [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) a la valeur `WPA2` ou `WPA2PSK` .
-   L’élément de [**chiffrement**](wlan-profileschema-encryption-authencryption-element.md) a la valeur `AES` .

Contrairement à la plupart des éléments du \_ schéma de profil WLAN, cet élément se trouve dans l' `https://www.microsoft.com/networking/WLAN/profile/v2` espace de noms.

La valeur de l’élément **FipsMode** est ignorée si le pilote de miniport de l’interface sans fil ne prend pas en charge le mode FIPS.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge. Si **FipsMode** est présent dans un profil, l’élément est ignoré.

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

L’élément est défini par l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Notes

Ce paramètre peut être défini sur la ligne de commande à l’aide de la commande **netsh wlan set profileparameter** . Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="examples"></a>Exemples

Pour afficher un exemple de profil qui utilise l’élément **FipsMode** , consultez [exemple de profil FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



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

 

 
