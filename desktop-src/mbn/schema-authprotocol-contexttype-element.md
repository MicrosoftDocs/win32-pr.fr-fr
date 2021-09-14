---
description: Spécifie le protocole d’authentification à utiliser pour l’activation d’un contexte PDP (Packet Data Protocol).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Élément AuthProtocol (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118109"
---
# <a name="authprotocol-contexttype-element"></a>Élément AuthProtocol (contextType)

L’élément **AuthProtocol (ContextType)** spécifie le protocole d’authentification à utiliser pour l’activation d’un contexte PDP (Packet Data Protocol).

L’élément peut avoir l’une des valeurs suivantes.

| Valeur      | Signification                                                                 |
|------------|-------------------------------------------------------------------------|
| None     | Aucun protocole d’authentification.                                             |
| Protocole      | Authentification par mot de passe non chiffrée.                                    |
| CHAP     | Protocole CHAP (Challenge Handshake Authentication Protocol).                      |
|  MsCHAPV2 | Utilisez le protocole CHAP (Microsoft s Challenge Handshake Authentication Protocol) v 2.0. |



 

Cet élément est facultatif et n’est utilisé que pour les profils GSM. Si l’élément n’est pas spécifié et que le profil est destiné à un appareil GSM, le service haut débit mobile utilise **« None »**.

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **AuthProtocol** est défini par le type complexe [**ContextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**Contexte (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




