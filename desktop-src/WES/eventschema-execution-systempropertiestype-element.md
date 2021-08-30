---
title: Élément Execution (SystemPropertiesType)
description: Contient des informations sur le processus et le thread qui a consigné l’événement.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- Élément d’exécution EventLog
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e4b38c5f0fbdbb95925ad6e65aa2ae3ef79f650459210d6bb38a1b917353704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904929"
---
# <a name="execution-systempropertiestype-element"></a>Élément Execution (SystemPropertiesType)

Contient des informations sur le processus et le thread qui a consigné l’événement.

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L’élément d' **exécution** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom          | Type         | Description                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| KernelTime    | unsignedInt  | Durée d’exécution écoulée pour les instructions en mode noyau, en unités de temps processeur.<br/>                        |
| ProcessID     | unsignedInt  | Identifie le processus qui a généré l’événement.<br/>                                               |
| ProcessorID   | unsignedByte | Numéro d’identification du processeur qui a traité l’événement.<br/>                          |
| ProcessorTime | unsignedInt  | Pour les sessions privées ETW, le temps d’exécution écoulé pour les instructions en mode utilisateur, en graduations de l’UC.<br/> |
| SessionID     | unsignedInt  | Numéro d’identification de la session Terminal Server dans laquelle l’événement s’est produit.<br/>         |
| ThreadID      | unsignedInt  | Identifie le thread qui a généré l’événement.<br/>                                                |
| UserTime      | unsignedInt  | Durée d’exécution écoulée pour les instructions en mode utilisateur, en unités de temps processeur.<br/>                          |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**Système (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





