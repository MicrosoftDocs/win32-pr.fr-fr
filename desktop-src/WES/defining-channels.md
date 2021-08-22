---
title: Définition des canaux
description: Les événements peuvent être écrits dans des canaux de journaux des événements, des fichiers journaux de suivi des événements ou les deux. Un canal est fondamentalement un récepteur qui collecte des événements.
ms.assetid: 3c2f39ee-fbc0-40ae-8279-566905250f47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c2f932616a131e478c100996fd0b76034b3cccdebf4e3714fd5b9b38ba9678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032479"
---
# <a name="defining-channels"></a>Définition des canaux

Les événements peuvent être écrits dans des canaux de journaux des événements, des fichiers journaux de suivi des événements ou les deux. Un canal est fondamentalement un récepteur qui collecte des événements. si le public cible de vos événements utilise des consommateurs d’événements tels que le Windows observateur d’événements, vous devez définir de nouveaux canaux pour collecter vos événements ou importer un canal existant défini par un autre fournisseur.

Pour définir vos propres canaux, utilisez l’élément **Channel** . Pour définir un canal importé, utilisez l’élément **importChannel** . Vous pouvez spécifier jusqu’à huit canaux dans n’importe quelle combinaison de canaux ou de canaux importés que vous définissez.

Le canal doit être de l’un des quatre types suivants : admin, opérationnel, analyse et débogage. Chaque type de canal a une audience prévue, qui détermine le type d’événements que vous écrivez sur le canal. Pour obtenir une description de chaque type, consultez le type complexe [**ChannelType**](eventmanifestschema-channeltype-complextype.md) .

Pour spécifier le canal sur lequel un événement est écrit, affectez à l’attribut de **canal** de la définition de l’événement la même valeur que l’attribut **enfants** de la définition de canal. Les événements peuvent uniquement être écrits sur un canal à la fois, mais ils peuvent également être collectés simultanément jusqu’à 7 autres sessions ETW.

L’exemple suivant montre comment importer un canal. Vous devez définir les attributs **enfants** et **Name** . L’attribut **enfants** identifie de façon unique le canal : chaque identificateur de canal dans votre liste de canaux doit être unique. Affectez à l’attribut **Name** le même nom que celui utilisé lors de la définition du canal.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider" 
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}" 
                symbol="PROVIDER_GUID" 
                resourceFileName="<path to the exe or dll that contains the metadata resources>" 
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                <channels>
                    <channel chid="c1"
                             name="Microsoft-Windows-BaseProvider/Admin"
                             symbol="CHANNEL_BASEPROVIDER_ADMIN"
                             type="Admin"/>
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```

Bien que Winmeta.xml définisse des canaux hérités que vous pouvez importer, vous ne devez pas les utiliser, sauf si vous prenez en charge des consommateurs hérités qui consomment des événements hors des canaux hérités (par exemple, une application ou un système). le fichier Winmeta.xml est inclus dans le SDK Windows.

L’exemple suivant montre comment définir un canal. Vous devez définir les attributs **enfants**, **Name** et **type** . L’attribut **enfants** identifie de façon unique le canal : chaque identificateur de canal dans votre liste de canaux doit être unique. Affectez à l’attribut **enfants** une valeur unique pour les canaux que votre fournisseur répertorie ; l’identificateur de canal est référencé dans une ou plusieurs de vos définitions d’événements. La Convention pour nommer le canal consiste à utiliser le nom et le type de canal du fournisseur sous la forme, *providerName* / *channelType*.

```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                <channels>
                    <importChannel chid="c1"
                                   name="Microsoft-Windows-BaseProvider/Admin"
                                   symbol="CHANNEL_BASEPROVIDER_ADMIN"
                                   />

                    <channel chid="c2"
                             name="Microsoft-Windows-SampleProvider/Operational"
                             type="Operational"
                             enabled="true"
                             />
                </channels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Microsoft-Windows-SampleProvider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
