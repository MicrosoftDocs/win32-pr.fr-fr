---
description: Spécifie si l’appareil haut débit mobile se connecte automatiquement à un réseau.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Élément AutoConnectOnInternet (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: 3a10804e91ee34125c25c320a49b5f7251f720ed9ce6c770c2aa4af5167a8511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881474"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>Élément AutoConnectOnInternet (MBNProfile)

L’élément **AutoConnectOnInternet (MBNProfile)** spécifie si l’appareil haut débit mobile se connecte automatiquement à un réseau.

Si la valeur est **false**, la logique de connexion automatique du service haut débit mobile n’est pas utilisée si une autre connectivité réseau est disponible pour le système. Si la valeur est **true**, le service haut débit mobile tente de connecter automatiquement l’appareil au réseau en fonction du paramètre de connexion automatique défini dans l’élément [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) .

**Windows 8 et versions ultérieures :** Cet élément est déconseillé. Utilisez la méthode [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) avec le paramètre *Property* défini sur **WCM \_ global \_ Property \_ Minimize \_ Policy** à la place.

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

L’élément **AutoConnectOnInternet** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

