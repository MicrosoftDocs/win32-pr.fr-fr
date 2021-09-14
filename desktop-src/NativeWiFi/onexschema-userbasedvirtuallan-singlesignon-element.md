---
description: Spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Élément userBasedVirtualLan (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009441"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>Élément userBasedVirtualLan (singleSignOn)

L’élément userBasedVirtualLan (singleSignOn) spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur. Certains périphériques NAS (Network Access Server) modifient le réseau local virtuel après l’authentification d’un utilisateur. Quand userBasedVirtualLan a la valeur TRUE, le NAS peut modifier le réseau local virtuel d’un appareil après l’authentification d’un utilisateur.

Cet élément est facultatif. Quand userBasedVirtualLan n’est pas spécifié dans un profil, la valeur FALSe est utilisée.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

L’élément **userBasedVirtualLan** est défini par l’élément [**singleSignOn**](onexschema-singlesignon-onex-element.md) .

## <a name="remarks"></a>Remarques

Ce paramètre peut être défini sur la ligne de commande à l’aide de la commande **netsh wlan set profileparameter** . Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
