---
title: Élément instrumentationManifest
description: Nœud racine du manifeste.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- EventLog, élément instrumentationManifest
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7dac9ab8c8aa2a6caeacf43023c4995be69f293affd5dd5a904d7fb96d710266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343718"
---
# <a name="instrumentationmanifest-element"></a>Élément instrumentationManifest

Nœud racine du manifeste.

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                        | Type                                                                               | Description                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Instrumentation**](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [**InstrumentationType**](eventmanifestschema-instrumentationtype-complextype.md) | Cette section définit un ou plusieurs fournisseurs d’événements et les événements qu’ils consignent.<br/>                                                                                                                                                                                                                     |
| [**localiz**](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)       | Cette section définit les chaînes de message localisées que les consommateurs utilisent pour l’affichage. Par exemple, cette section contient la chaîne de message localisée pour le nom de votre fournisseur, les événements que vous définissez et les attributs d’événement que vous définissez, tels que les canaux, les tâches et les OpCodes.<br/> |
| [**Metadata**](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)               | Cette section définit les types de métadonnées que d’autres manifestes peuvent utiliser. pour obtenir un exemple, consultez le fichier Winmeta.xml inclus dans le \\ dossier include du SDK Windows.<br/>                                                                                                                                    |



## <a name="remarks"></a>Remarques

L’élément **instrumentationManifest** doit contenir les espaces de noms suivants :

<dl> xmlns = " https://schemas.microsoft.com/win/2004/08/events "  
xmlns : Win = " https://manifests.microsoft.com/win/2004/08/windows/events "  
xmlns : XS = " https://www.w3.org/2001/XMLSchema "  
</dl>

Un manifeste doit contenir une section instrumentation et une section localization. La section de métadonnées et la section d’instrumentation s’excluent mutuellement (vous ne pouvez pas définir les deux dans le même manifeste). Bien que vous puissiez créer un manifeste qui contient une section de métadonnées, le service ne l’utilise pas. les seules métadonnées reconnues par le service sont les métadonnées trouvées dans le fichier Winmeta.xml.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la structure d’un manifeste d’instrumentation entièrement défini.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





