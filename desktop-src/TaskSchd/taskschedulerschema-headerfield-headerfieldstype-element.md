---
title: Élément HeaderField (headerFieldsType)
description: Contient un champ pour un en-tête dans un message électronique.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Élément HeaderField Planificateur de tâches
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510580"
---
# <a name="headerfield-headerfieldstype-element"></a>Élément HeaderField (headerFieldsType)

Contient un champ pour un en-tête dans un message électronique.

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

L’élément **HeaderField** est défini par le type complexe [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                        | Dérivé de                                                                 | Description                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                            | Type                                                                    | Description                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Nom**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Spécifie le nom du champ d’en-tête dans un message électronique.<br/> |
| [**Valeur**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Spécifie la valeur d’un champ d’en-tête dans un message électronique.<br/>  |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Pour le développement de scripts, consultez [**EmailAction. HeaderFields**](emailaction-headerfields.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





