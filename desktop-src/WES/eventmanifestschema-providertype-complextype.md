---
title: Type complexe ProviderType
description: Définit un fournisseur et les métadonnées qu’il utilise pour définir ses événements. | Type complexe ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Type de journal complexe ProviderType
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322325"
---
# <a name="providertype-complex-type"></a>Type complexe ProviderType

Définit un fournisseur et les métadonnées qu’il utilise pour définir ses événements.

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                       | Type                                                                         | Description                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**couche**](eventmanifestschema-channels-providertype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)   | Définit une liste de canaux auxquels les fournisseurs peuvent enregistrer des événements.<br/>                                                                                                                                                                                      |
| [**événements**](eventmanifestschema-events-providertype-element.md)             | [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)     | Définit une liste de définitions d’événements des événements que le fournisseur peut journaliser.<br/>                                                                                                                                                                       |
| **filtres**                                                                   | [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)     | Définit une liste de filtres que votre fournisseur prend en charge. Vous pouvez utiliser les filtres, comme vous le feriez pour le niveau et les mots clés, pour déterminer si vous souhaitez écrire un événement. <br/> **Windows Server 2008 et Windows Vista :** Non pris en charge jusqu’à Windows 7.<br/> |
| [**mot**](eventmanifestschema-keywords-providertype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)   | Définit une liste de mots clés qui classent les événements.<br/>                                                                                                                                                                                                 |
| [**Balance**](eventmanifestschema-levels-providertype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)       | Définit une liste de niveaux qui spécifient la gravité d’un événement.<br/>                                                                                                                                                                                    |
| [**Mount**](eventmanifestschema-maps-providertype-element.md)                 | [**MapType**](eventmanifestschema-maptype-complextype.md)                   | Définit une liste de paires nom/valeur que vous pouvez référencer dans la section de modèle du manifeste.<br/>                                                                                                                                                 |
| [**namedQueries**](eventmanifestschema-namedqueries-providertype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)     | Non utilisé. Définit une liste de requêtes nommées qui interrogent la chaîne de message d’événement pour obtenir une valeur et effectuent une action spécifiée si elle est trouvée.<br/>                                                                                                                 |
| [**OpCodes**](eventmanifestschema-opcodes-providertype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)     | Définit une liste d’OpCodes que vous pouvez utiliser pour regrouper des événements au sein d’une tâche.<br/>                                                                                                                                                                          |
| [**décrites**](eventmanifestschema-tasks-providertype-element.md)               | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)         | Définit une liste de tâches qu’un fournisseur peut utiliser pour regrouper des événements. En général, vous utilisez des tâches pour regrouper des événements pour une fonctionnalité ou un composant du fournisseur.<br/>                                                                                              |
| [**ceux**](eventmanifestschema-templates-providertype-element.md)       | [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md) | Définit une liste de modèles qui spécifient les données à inclure avec les événements.<br/>                                                                                                                                                                      |



## <a name="attributes"></a>Attributs



| Nom                                | Type                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| guid                                | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | GUID qui identifie de façon unique le fournisseur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| helpLink                            | anyURI                                                            | URL ou MS Help lien vers du contenu qui fournit des informations sur les événements déclenchés par le fournisseur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| message                             | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nom complet localisé pour le fournisseur. La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste. <br/>                                                                                                                                                                                                                                                                                                                           |
| messageFileName                     | [**cheminfichier**](eventmanifestschema-filepath-simpletype.md)       | Chemin d’accès complet au fichier qui contient les ressources de message localisées du fournisseur. Le fichier peut être un fichier exécutable ou un fichier DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| name                                | anyURI                                                            | Nom du fournisseur. Le nom doit se présenter sous la forme composant du produit de la *société* -  - .<br/> Le nom ne peut pas comporter plus de 255 caractères et ne peut pas contenir les caractères suivants : ' > ', ' < ', ' & ', ' "', ' ', ' ', ' \| \\ : ', ' ', ' ? ', ' \* 'ou des caractères avec des codes inférieurs à 31. En outre, le nom doit respecter les contraintes générales sur les noms de fichiers et de clés de registre. Ces contraintes se trouvent dans [nommer un fichier](/windows/desktop/FileIO/naming-a-file)et les [limites de taille des éléments du registre](/windows/desktop/SysInfo/registry-element-size-limits).<br/> |
| parameterFileName                   | [**cheminfichier**](eventmanifestschema-filepath-simpletype.md)       | Chemin d’accès complet au fichier qui contient les ressources de chaîne de paramètres du fournisseur. Le fichier peut être un fichier exécutable ou un fichier DLL. Vous pouvez spécifier plusieurs fichiers de paramètres séparés par un point-virgule. Le fichier est recherché lorsque la chaîne de message d’un événement contient une chaîne de paramètres. Les paramètres vous permettent de fournir des chaînes d’insertion localisables. Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                                                |
| resourceFileName                    | [**cheminfichier**](eventmanifestschema-filepath-simpletype.md)       | Chemin d’accès complet au fichier qui contient les ressources de métadonnées du fournisseur. Le fichier peut être un fichier exécutable ou un fichier DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| source                              |                                                                   | À usage interne uniquement.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| symbole                              | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer le GUID du fournisseur dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le GUID du fournisseur dans le fichier d’en-tête généré par le compilateur.<br/>                                                                                                                                                                                                                                                                           |
| warnOnApplicationCompatibilityError | **xs:boolean**                                                    | À usage interne uniquement.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>Notes

Le observateur d’événements Windows (Eventvwr.exe) utilise la chaîne de message localisée si elle est disponible ; dans le cas contraire, elle utilise la chaîne de l’attribut Name.

Les chemins d’accès pour resourceFileName, messageFileName et parameterFileName peuvent contenir des variables d’environnement. Si vous définissez une nouvelle variable d’environnement à utiliser dans le chemin d’accès, vous devez redémarrer l’ordinateur afin que le service journal des événements puisse sélectionner la nouvelle variable. dans le cas contraire, le service ne pourra pas trouver les ressources de votre fournisseur.

La chaîne de message d’un événement peut contenir des chaînes d’insertion et des chaînes de paramètres. Une chaîne d’insertion se présente sous la forme%*n*, où *n* est un index de base un qui identifie un élément de données à partir du modèle de données de l’événement que vous souhaitez insérer dans le message. Une chaîne de paramètres (Voir l’attribut **parameterFileName** ) se présente sous la forme%%*n*, où n est l’identificateur d’un message dans la table des messages. Si la chaîne de message de l’événement contenait « %1% %11 = %2% %12 » et que les valeurs des éléments de données pour %1 et %2 étaient 8 et 2, respectivement, et que les chaînes de paramètres pour% %11 et% %12 étaient respectivement « quarts » et « gallons »

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

