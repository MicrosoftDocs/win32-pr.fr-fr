---
description: Spécifie si le chargeur de topologie énumère les types de médias fournis par la source du média.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: Attribut MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318301"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a>\_Attribut de l' \_ énumération \_ des \_ types de source de la topologie MF

Spécifie si le chargeur de topologie énumère les types de médias fournis par la source du média.

## <a name="data-type"></a>Type de données

**UINT32**

Utilisez l’une des valeurs suivantes.



| Valeur                                                                                                                                    | Signification                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSe * * * * *</dt> </dl> | N’énumère pas les types de médias sources.<br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VRAI * * * * *</dt> </dl>    | Énumérer les types de médias sources.<br/>        |



 

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Notes

Chaque flux sur une source de média peut offrir plusieurs types de média. La liste de types est énumérée via l’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) sur le descripteur de flux.

L’ordre dans lequel le chargeur de topologie tente d’obtenir les types de média d’une source multimédia est contrôlé par deux attributs :

-   L' \_ \_ attribut de topologie MF énumérer les \_ \_ types de sources sur la topologie.
-   Attribut [**de \_ \_ \_ méthode de connexion MF TOPONODE**](mf-toponode-connect-method-attribute.md) sur le nœud source.

Si l’attribut de la \_ topologie MF \_ énumérer les \_ \_ types de source est **false** ou non défini, le chargeur de topologie utilise le type de média actuel du flux. Elle n’énumère pas la liste des types possibles. Si le type de média actuel n’est pas compatible avec le nœud de topologie en aval et qu’aucune combinaison de décodeurs/convertisseurs ne peut être trouvée, la résolution de la topologie échoue.

Si l’attribut de la \_ topologie MF \_ énumérer les \_ \_ types de sources a la **valeur true**, le chargeur de topologie énumère les types de médias de la source jusqu’à ce qu’il trouve un type compatible. Dans ce cas, l’ordre exact des opérations varie selon que l’attribut [**de \_ \_ \_ méthode MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) sur le nœud source comprend l’indicateur **MF \_ Connect \_ Resolve \_ Independent \_ sortie OutputTypes** .

Si \_ la topologie MF \_ énumérer \_ \_ les types de sources a la **valeur true** et que l’indicateur **MF \_ Connect \_ Resolve \_ Independent \_ sortie OutputTypes** est défini, le chargeur de topologie épuise chaque type de média avant de passer au suivant, comme suit :

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

Si \_ la topologie MF \_ \_ d’énumération \_ des types de source est **vraie** mais que la résolution de la **\_ connexion MF \_ \_ \_ sortie OutputTypes** n’est pas définie, le chargeur de topologie tente une connexion directe avec chaque type de média, puis tente chaque type de média avec des convertisseurs, et enfin essaie chaque type de média avec des décodeurs :

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

Si \_ la topologie MF \_ énumérer \_ \_ les types de sources a la **valeur false**, l’indicateur de **\_ \_ résolution \_ \_ sortie OutputTypes de la connexion MF MF** est ignoré.

La valeur par défaut de la \_ topologie MF \_ énumérer les types de \_ source \_ est **false**, pour la compatibilité avec les applications existantes.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

### <a name="example"></a>Exemple

Voici un exemple qui illustre l’indicateur de **\_ résolution de \_ \_ \_ sortie OutputTypes indépendant de la connexion MF** . Supposons que la topologie a l' \_ attribut de la topologie MF \_ énumérer les \_ \_ types de source défini sur **true**.

La source du média offre les types suivants :

-   T1, T2, T3

Le récepteur multimédia accepte les types suivants :

-   T3, T4

Cas 1 : l’indicateur de **\_ résolution de \_ \_ \_ sortie OutputTypes indépendant de la connexion MF** est défini.

1.  Le chargeur de topologie tente une connexion directe avec T1. Le récepteur rejette T1.
2.  Le chargeur de topologie insère un décodeur qui accepte T1 et des sorties T4. Le récepteur accepte T4.
3.  La topologie finale contient : source du média → décodeur → récepteur multimédia.

Cas 2 : l’indicateur n’est pas défini.

1.  Le chargeur de topologie tente une connexion directe avec T1. Le récepteur rejette T1.
2.  Le chargeur de topologie tente une connexion directe avec T2. Le récepteur rejette T2.
3.  Le chargeur de topologie tente une connexion directe avec T3. Le récepteur accepte T3.
4.  La topologie finale contient : source du média → récepteur multimédia.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> </dl>

 

 




