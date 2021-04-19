---
title: Type complexe ChannelPublishingType
description: Définit les propriétés de journalisation pour la session utilisée par le canal. | Type complexe ChannelPublishingType
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- ChannelPublishingType type complexe EventLog
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106529569"
---
# <a name="channelpublishingtype-complex-type"></a>Type complexe ChannelPublishingType

Définit les propriétés de journalisation pour la session utilisée par le canal.

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                              | Type                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Tampon**](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Quantité de mémoire, en kilo-octets, à allouer pour chaque mémoire tampon. Si vous vous attendez à un taux d’événements relativement faible, la taille de la mémoire tampon doit être définie sur la taille de la page de mémoire. Si le taux d’événements est supposé être relativement élevé, vous devez spécifier une plus grande taille de mémoire tampon et augmenter le nombre maximal de mémoires tampons.<br/> La taille de la mémoire tampon affecte la vitesse à laquelle les tampons sont remplis et doivent être vidés. Bien qu’une petite taille de mémoire tampon nécessite moins de mémoire, elle augmente la vitesse à laquelle les tampons doivent être vidés.<br/> La taille de la mémoire tampon par défaut pour les canaux d’analyse et de débogage est de 4 Ko, et pour admin et opérationnel, il s’agit de 64 Ko.<br/>                                                                                                                |
| [**clockType**](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | Résolution d’horloge à utiliser lors de la journalisation de l’horodatage pour chaque événement. Vous pouvez spécifier SystemTime ou QPC. SystemTime fournit un horodatage de faible résolution (10 millisecondes), mais est relativement moins onéreux à récupérer. La valeur par défaut est SystemTime. <br/> Le compteur de performance des requêtes (QPC) fournit un horodatage à haute résolution (nanosecondes 100), mais il est relativement coûteux à récupérer. Vous devez QPC si vous avez des taux d’événements élevés ou si le consommateur fusionne les événements à partir de mémoires tampons différentes.<br/>                                                                                                                                                                                                                                 |
| [**controlGuid**](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | Identifie le GUID de session pour une session ETW qui contient des événements WPP. Ce paramètre est autorisé uniquement pour les canaux de type Debug. Ces canaux ne peuvent pas être entièrement activés avec les mots clés définis sur zéro (0x0000000000000000). Ils doivent être activés avec les mots clés définis sur 0xFFFFFFFFFFFFFFFF.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **fileMax**                                                                          | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Nombre maximal de fois où vous souhaitez que le service crée un nouveau fichier journal lorsque le canal est activé (y compris lorsque l’ordinateur est redémarré). Si la valeur est 0 ou 1, le service remplacera le fichier journal chaque fois que le canal est activé et que les événements précédents seront perdus. Si la valeur est supérieure à 1, le service crée un nouveau fichier journal chaque fois que le canal est activé afin de conserver les événements. La valeur par défaut est 1 et la valeur maximale que vous pouvez spécifier est 16.<br/> Le service ajoute un nombre décimal à trois chiffres compris entre 0 et fileMax 1 à chaque nom de fichier. Par exemple, *nom de fichier*. etl.xxx, où xxx est le nombre décimal à trois chiffres. Les fichiers se trouvent dans les journaux% windir% \\ system32 \\ winevt \\ .<br/> |
| [**mot**](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Masque de réécriture qui détermine la catégorie des événements écrits dans le canal. Si la valeur de l’attribut **Keywords** est 0, tous les événements écrits par le fournisseur sont écrits dans le canal ; Sinon, seuls les événements qui ont défini un mot clé inclus dans le masque de masque des **Mots clés** sont écrits dans le canal. La valeur par défaut est 0.<br/> Les canaux de débogage dont l’attribut controlGuid est défini doivent définir l’attribut **Keywords** sur 0xFFFFFFFFFFFFFFFF.<br/> La session transmet la valeur des mots clés au fournisseur lorsqu’il active le fournisseur.<br/>                                                                                                                                                                            |
| [**latence**](eventmanifestschema-latency-channelpublishingtype-element.md)         | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Délai d’attente avant le vidage des mémoires tampons, en millisecondes. Si la valeur est zéro, ETW vide les mémoires tampons dès qu’elles sont complètes. Si la valeur est différente de zéro, ETW vide toutes les mémoires tampons qui contiennent des événements basés sur la valeur même si la mémoire tampon n’est pas saturée. En règle générale, vous souhaitez vider les mémoires tampons uniquement lorsqu’elles sont complètes. Forcer le vidage des mémoires tampons peut augmenter la taille du fichier journal avec un espace de mémoire tampon non rempli. La valeur par défaut est 1 seconde pour les journaux d’administration et les journaux des opérations et 5 secondes pour les journaux d’analyse et de débogage.<br/>                                                                                                                                                                                                                               |
| [**niveau**](eventmanifestschema-level-channelpublishingtype-element.md)             | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Niveau de gravité des événements à écrire dans le canal. Le service écrit des événements dans le canal qui ont une valeur de niveau inférieure ou égale à la valeur spécifiée. La valeur par défaut est 0, ce qui signifie que enregistre les événements avec n’importe quelle valeur de niveau.<br/> La session transmet la valeur de niveau au fournisseur lorsqu’il active le fournisseur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**maxBuffers**](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Nombre maximal de mémoires tampons à allouer pour la session. En général, cette valeur est le nombre minimal de mémoires tampons plus vingt. Cette valeur doit être supérieure ou égale à la valeur spécifiée pour minBuffers.<br/> Le nombre maximal par défaut de mémoires tampons pour les canaux d’analyse et de débogage est de 10 Ko, et pour admin et opérationnel, il s’agit de 64 Ko.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**minBuffers**](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Nombre minimal de mémoires tampons à allouer pour la session. La valeur par défaut est zéro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**sidType**](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | Détermine s’il faut inclure un identificateur de sécurité (SID) du principal avec chaque événement écrit dans le canal. Pour inclure le SID avec l’événement, définissez cet attribut sur « publication ». Le SID est défini en fonction de l’identité du thread au moment de l’écriture de l’événement. Si vous ne souhaitez pas inclure le SID avec l’événement, définissez cet attribut sur « None ». La valeur par défaut est « publication ».<br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Notes

Vous pouvez spécifier ces informations de publication pour les types de canaux d’analyse et de débogage, ou pour n’importe quel canal qui spécifie l’isolation personnalisée.

Bien que vous puissiez spécifier le niveau et les mots clés, vous devez considérer qu’il s’agit des seuls événements que vous recevrez du fournisseur pour ce canal.

Quand une mémoire tampon est saturée, ETW vide la mémoire tampon dans le fichier journal. Si les mémoires tampons sont remplies plus rapidement qu’elles ne peuvent être vidées, de nouvelles mémoires tampons sont allouées et ajoutées au pool de mémoires tampons de la session, jusqu’au nombre maximal spécifié. Au-delà de cette limite, la session ignore les événements entrants jusqu’à ce qu’une mémoire tampon soit disponible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





