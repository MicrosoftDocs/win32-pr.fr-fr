---
description: Spécifie si un utilisateur peut créer un profil tous les utilisateurs.
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: Élément allowEveryoneToCreateAllUserProfiles (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525767"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a>Élément allowEveryoneToCreateAllUserProfiles (globalFlags)

L’élément **allowEveryoneToCreateAllUserProfiles** (globalFlags) spécifie si un utilisateur peut créer un profil All-User. Un profil tous les utilisateurs peut être utilisé par n’importe quel utilisateur sur l’ordinateur pour se connecter au réseau sans fil associé au profil.

Si **allowEveryoneToCreateAllUserProfiles** a la valeur true, les utilisateurs peuvent créer un profil All-User. Si **allowEveryoneToCreateAllUserProfiles** a la valeur false, tous les utilisateurs ne peuvent pas créer un profil All-User, et il existe une liste DACL associée à l' \_ objet de sécurité WLAN Secure \_ Add \_ New \_ All \_ User \_ Profiles qui spécifie les utilisateurs ou les groupes d’utilisateurs autorisés à créer des profils tous les utilisateurs. La liste DACL par défaut spécifie que seuls les utilisateurs ayant ouvert une session en tant que membre du groupe administrateurs peuvent créer un profil utilisateur. Les paramètres de sécurité par défaut peuvent être modifiés en appelant [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings). Pour accéder aux paramètres de sécurité actuels, appelez [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Cet élément est obligatoire. Lorsqu’un profil est créé par le service de configuration automatique, cet élément a la valeur par défaut TRUE.

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

L’élément **allowEveryoneToCreateAllUserProfiles** est défini par l’élément [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




