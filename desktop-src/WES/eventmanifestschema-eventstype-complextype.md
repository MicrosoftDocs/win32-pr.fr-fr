---
title: Type complexe EventsType
description: Contient une liste de fournisseurs définis dans le manifeste. | Type complexe EventsType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventsType type complexe EventLog
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531282"
---
# <a name="eventstype-complex-type"></a>Type complexe EventsType

Contient une liste de fournisseurs définis dans le manifeste.

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants

| Élément | Type | Description |
|---------|------|-------------|
| message |      | Définit une chaîne de message. |
| messageTable | | Définit une liste de chaînes de message. Vous ne devez pas être obligé d’utiliser une table de messages, sauf dans les cas suivants où vous devez définir une table de messages pour assigner explicitement des numéros de ressource aux chaînes de message. <ul><li>Vous effectuez une migration à partir d’un fichier texte de message (. MC) vers un manifeste, mais vous écrivez toujours des événements sur les canaux de l’application et du système, afin que les consommateurs hérités continuent de consommer les événements. Pour que cela fonctionne, les identificateurs de ressource pour les chaînes de message définies dans le manifeste doivent être les mêmes que les identificateurs d’événements. Toutefois, le compilateur de message affecte automatiquement des identificateurs de ressource aux chaînes de message. Pour remplacer le compilateur, utilisez la table de messages et affectez à l’attribut value la valeur de l’identificateur d’événement et l’attribut de message pour faire référence à une chaîne dans la table de chaînes de la section localization du manifeste.</li><li>Si vous souhaitez identifier plus de 16 fournisseurs, vous devez inclure la table de messages que les fournisseurs dix-septième et sur doivent utiliser pour assigner des valeurs de ressource pour les chaînes de message qu’ils définissent. Si le fournisseur fait référence à des chaînes de message que les fournisseurs 1 à 16 sont définies, vous n’incluez pas ces chaînes de message dans la table des messages.</li></ul>|
| [**moteur**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Liste des fournisseurs que vous souhaitez définir. |

## <a name="attributes"></a>Attributs

| Nom    | Type                                                             | Description                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Référence à la chaîne localisée dans la table de chaînes.                               |
| mid     | xs:string                                                        | Non utilisé.                                                                              |
| symbole  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Nom symbolique que vous souhaitez que le compilateur de message crée pour cette chaîne de message.|
| value   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Nombre à utiliser comme identificateur de message pour ce message.                          |


## <a name="remarks"></a>Notes

La limite pratique du nombre de fournisseurs que vous pouvez définir dans un manifeste est de 16 fournisseurs. Si vous spécifiez plus de 16 fournisseurs, vous devez utiliser une table de messages pour assigner explicitement des numéros de ressource aux chaînes de message auxquelles le fournisseur fait référence. Pour plus d’informations, consultez l’élément message ci-dessus.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|-------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows Vista uniquement\]       |
| Serveur minimal pris en charge | Applications de bureau Windows Server 2008 \[ uniquement\] |
