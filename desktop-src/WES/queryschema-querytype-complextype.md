---
title: QueryType (type complexe)
description: Définit un ensemble de requêtes de sélecteur et de suppresseur utilisées pour inclure des événements dans ou exclure des événements du jeu de résultats.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- TypeRequête type complexe EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103576"
---
# <a name="querytype-complex-type"></a>QueryType (type complexe)

Définit un ensemble de requêtes de sélecteur et de suppresseur utilisées pour inclure des événements dans ou exclure des événements du jeu de résultats.

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                    | Type | Description                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sélectionner**](queryschema-select-querytype-element.md)     |      | Requête XPath qui identifie les événements à inclure dans le jeu de résultats de la requête. Spécifiez le XPath dans le corps de texte de cet élément. Le XPath est limité à 32 expressions.<br/>   |
| [**Suppress**](queryschema-suppress-querytype-element.md) |      | Requête XPath qui identifie les événements à exclure du jeu de résultats de la requête. Spécifiez le XPath dans le corps de texte de cet élément. Le XPath est limité à 32 expressions.<br/> |



## <a name="attributes"></a>Attributs



| Nom | Type   | Description                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id   | long   | Identificateur qui identifie de façon unique cette requête dans votre liste de requêtes. L’identificateur est de base zéro. Vous devez spécifier un identificateur si votre liste de requêtes contient plus d’une requête.<br/> |
| Chemin d’accès | anyURI | Nom du canal ou chemin d’accès au fichier journal qui contient les événements.<br/>                                                                                                            |
| Chemin d’accès | anyURI | Nom du canal ou chemin d’accès au fichier journal qui contient les événements.<br/>                                                                                                            |
| Chemin d’accès | anyURI | Non utilisé.<br/>                                                                                                                                                                                |



## <a name="remarks"></a>Notes

La requête doit avoir au moins une instruction SELECT. Pour chaque instruction de suppression, il doit y avoir au moins une instruction SELECT qui spécifie le même chemin d’accès. Si la requête SELECT et Suppress renvoient les mêmes événements, l’instruction de suppression est prioritaire. Si vous sélectionnez des événements de plusieurs sources, les événements sont retournés dans l’ordre des horodatages. Si vous utilisez l’horodatage du système et que le taux d’événements est élevé, il est possible que plusieurs événements aient le même horodatage. Dans ce cas, l’ordre des événements devient ambigu et les événements peuvent apparaître dans le désordre.

Si vous spécifiez un chemin d’accès pour l’une des requêtes de la liste des requêtes, toutes les requêtes doivent spécifier un chemin d’accès. Si vous ne spécifiez pas de chemin d’accès pour toutes les requêtes, vous devez spécifier le chemin d’accès lors de l’appel de la fonction [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





