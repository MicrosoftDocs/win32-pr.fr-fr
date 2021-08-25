---
title: Définition des niveaux de gravité
description: Les niveaux sont utilisés pour regrouper les événements et indiquent généralement la gravité ou le niveau de détail d’un événement.
ms.assetid: dfa4e0a9-4d89-4f50-aef9-1dae0dc11726
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3c3c5e663e476f98bef5c9be3f20cae5e0e88a74a7996f6f515d1d92599eb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863679"
---
# <a name="defining-severity-levels"></a>Définition des niveaux de gravité

Les niveaux sont utilisés pour regrouper les événements et indiquent généralement la gravité ou le niveau de détail d’un événement. Pour définir un niveau, utilisez l’élément **Level** . Le fichier Winmeta.xml définit les niveaux de gravité couramment utilisés suivants :

-   win:Critical
-   win:Error
-   win:Warning
-   win:Informational
-   win:Verbose

Les consommateurs utilisent des niveaux pour rechercher des événements qui contiennent une valeur de niveau spécifique. Une session de suivi ETW peut également utiliser des niveaux pour limiter les événements écrits dans le fichier journal de suivi d’événements ; les événements avec une valeur de niveau inférieure ou égale à la valeur de niveau spécifiée sont écrits dans le fichier journal. Par exemple, si la session spécifiait la valeur de niveau pour Win : Warning, le fichier journal contiendrait des événements d’avertissement, d’erreur et critiques.

L’exemple suivant montre comment définir un niveau. Vous devez spécifier les attributs **Name** et **value** du niveau. La valeur de l’attribut **value** doit être comprise entre 16 et 255. Les attributs **symbol** et **message** sont facultatifs.


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

                . . .

                <levels>
                    <level name="NotValid"
                           value="16"
                           symbol="LEVEL_SAMPLEPROVIDER_NOTVALID"
                           message="$(string.Level.NotValid)"/>
                    <level name="Valid"
                           value="17"
                           symbol="LEVEL_SAMPLEPROVIDER_VALID"
                           message="$(string.Level.Valid)"/>
                </levels>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="Level.Valid" value="Valid"/>
                <string id="Level.NotValid" value="Not Valid"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
