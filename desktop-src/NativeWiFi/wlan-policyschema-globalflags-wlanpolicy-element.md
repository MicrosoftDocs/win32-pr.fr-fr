---
description: Contient les paramètres globaux du module d’auto-configuration (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Élément globalFlags (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110450"
---
# <a name="globalflags-wlanpolicy-element"></a>Élément globalFlags (WLANPolicy)

L’élément globalFlags (WLANPolicy) contient les paramètres globaux du module d’auto-configuration (ACM). Cet élément est obligatoire.

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:element name="showDeniedNetwork"
                type="boolean"
             />
            <xs:element name="allowEveryoneToCreateAllUserProfiles"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **globalFlags** est défini par l’élément [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                                    | Type    | Description                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean | Spécifie si un utilisateur peut créer un profil tous les utilisateurs. <br/>                                                               |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean | Spécifie si les ordinateurs utilisent le service de configuration automatique intégré (AutoConfig) pour gérer les connexions sans fil. <br/> |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean | spécifie si les réseaux refusés s’affichent dans le **Connecter à un assistant réseau** . <br/>                                         |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




