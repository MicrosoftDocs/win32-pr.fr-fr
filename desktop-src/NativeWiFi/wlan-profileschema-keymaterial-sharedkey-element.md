---
description: Contient une clé réseau ou une phrase secrète.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Élément keyMaterial (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194735"
---
# <a name="keymaterial-sharedkey-element"></a>Élément keyMaterial (sharedKey)

L’élément keyMaterial (sharedKey) contient une clé réseau ou une phrase secrète. Si l’élément [**protégé**](wlan-profileschema-protected-sharedkey-element.md) a la valeur true, ce matériel de clé est chiffré ; dans le cas contraire, le matériel de clé n’est pas chiffré. Le matériel de clé chiffrée est exprimé au format hexadécimal.

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

L’élément est défini par l’élément [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Notes

La plage de valeurs valides pour l’élément keyMaterial varie selon le type d’authentification et le chiffrement utilisés, comme spécifié par les éléments [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) et [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) . Elle varie également en fonction du [**type de frappe**](wlan-profileschema-keytype-sharedkey-element.md).

Le tableau suivant indique les valeurs de **clés** valides pour certaines paires d’authentification et de chiffrement.



| valeur [**d’authentification**](wlan-profileschema-authentication-authencryption-element.md) | valeur de [**chiffrement**](wlan-profileschema-encryption-authencryption-element.md) | valeur de [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) | Valeurs de **clés** valides                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ouvert ou partagé                                                                           | WEP                                                                              | networkKey                                                            | Cet élément contient une clé WEP de 5 ou 13 caractères ANSI, ou de 10 ou 26 caractères hexadécimaux.                                                                                             |
| WPAPSK ou WPA2PSK                                                                        | TKIP ou AES                                                                      | passPhrase                                                            | Cet élément contient une phrase secrète comprise entre 8 et 63 caractères ASCII, soit 8 à 63 caractères ANSI dans la plage de 32 à 126. Les valeurs de clé doivent respecter les exigences spécifiées par la norme 802.11 i. |
| WPAPSK ou WPA2PSK                                                                        | TKIP ou AES                                                                      | networkKey                                                            | Cet élément contient une clé de 64 caractères hexadécimaux.                                                                                                                                      |



 

Des caractères Unicode peuvent être entrés là où les caractères ANSI ou ASCII sont spécifiés ci-dessus. Toutefois, si les caractères Unicode fournis ne peuvent pas être mappés à des caractères ANSI ou ASCII, le matériel de clé fourni est rejeté.

Le matériel de clé retourné par [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) est toujours chiffré. En outre, si le matériel de clé non chiffré est transmis à [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), le matériel de clé est automatiquement chiffré avant d’être stocké dans le magasin de profils.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Le matériel de clé n’est jamais chiffré.

Si votre processus s’exécute dans le contexte du compte LocalSystem, vous pouvez déchiffrer le matériel de clé en appelant [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **keyMaterial** , consultez exemple de [profil de non-diffusion](non-broadcast-profile-sample.md), exemple de [Profil WPA-Personnel](wpa-personal-profile-sample.md)et exemple de profil [WPA2-Personal](wpa2-personal-profile-sample.md).

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

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**sharedKey (sécurité)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
