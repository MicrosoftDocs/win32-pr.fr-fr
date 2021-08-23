---
description: Spécifie la durée maximale, en secondes, pendant laquelle un client attend une réponse de l’authentificateur.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: Élément authPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ccaef08f65baffa0d7b9a921afd9db78a6ac6c6dd1d0bf4fd8075454fe38be21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684858"
---
# <a name="authperiod-onex-element"></a>Élément authPeriod (OneX)

L’élément authPeriod (OneX) spécifie la durée maximale, en secondes, pendant laquelle un client attend une réponse de l’authentificateur. Si aucune réponse n’est reçue pendant la période spécifiée, le client part du principe qu’aucun authentificateur n’est présent sur le réseau.

Cet élément est facultatif. Quand authPeriod n’est pas spécifié dans un profil, une valeur de 18 secondes est utilisée.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="authPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **authPeriod** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 




