---
description: Spécifie, en secondes, le délai maximal avant que la tentative de connexion d’authentification unique échoue.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Élément maxDelay (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864813"
---
# <a name="maxdelay-singlesignon-element"></a>Élément maxDelay (singleSignOn)

L’élément maxDelay (singleSignOn) spécifie, en secondes, le délai maximal avant que la tentative de connexion d’authentification unique échoue.

Cet élément est facultatif. Quand maxDelay n’est pas spécifié dans un profil, une valeur de 10 secondes est utilisée.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **maxDelay** est défini par l’élément [**singleSignOn**](onexschema-singlesignon-onex-element.md) .

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

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
