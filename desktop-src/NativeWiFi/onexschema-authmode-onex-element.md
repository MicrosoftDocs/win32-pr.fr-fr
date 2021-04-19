---
description: Spécifie le type d’informations d’identification utilisées pour l’authentification.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: Élément authMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517694"
---
# <a name="authmode-onex-element"></a>Élément authMode (OneX)

L’élément authMode (OneX) spécifie le type d’informations d’identification utilisées pour l’authentification. Le tableau suivant décrit les valeurs possibles.



| Valeur         | Description                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| machineOrUser | Utilisez les informations d’identification de l’ordinateur ou de l’utilisateur. Lorsqu’un utilisateur a ouvert une session, les informations d’identification de l’utilisateur sont utilisées pour l’authentification. Quand aucun utilisateur n’est connecté, les informations d’identification de l’ordinateur sont utilisées. |
| ordinateur       | Utiliser uniquement les informations d’identification de l’ordinateur.                                                                                                                                           |
| utilisateur          | Utiliser uniquement les informations d’identification de l’utilisateur.                                                                                                                                              |
| guest         | Utilisez uniquement les informations d’identification invité (vide).                                                                                                                                     |



 

Cet élément est facultatif. Quand authMode n’est pas spécifié dans un profil, la valeur `machineOrUser` est utilisée.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **authmode** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

## <a name="remarks"></a>Notes

Ce paramètre peut être défini sur la ligne de commande à l’aide de la commande **netsh wlan set profileparameter** . Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> </dl>

 

 
