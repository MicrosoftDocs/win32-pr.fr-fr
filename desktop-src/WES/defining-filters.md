---
title: Définition de filtres
description: Un fournisseur peut définir des filtres utilisés par une session pour filtrer les événements en fonction des données d’événement.
ms.assetid: b43912af-0e9c-414b-b3fa-03e7e35e493c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d9d065fe3a46fc22114cfb4aed5b5b51d9a89eafa3280e2e258199e06aad3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056017"
---
# <a name="defining-filters"></a>Définition de filtres

Un fournisseur peut définir des filtres utilisés par une session pour filtrer les événements en fonction des données d’événement. Avec le niveau et les mots clés, ETW détermine si l’événement est écrit dans le journal. Toutefois, avec les filtres, le fournisseur utilise les critères de données de filtre que la session de contrôle transmet (voir la fonction [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) ) pour déterminer s’il écrit l’événement dans cette session. Les filtres s’appliquent uniquement quand une session de suivi ETW active votre fournisseur.

En règle générale, les fournisseurs écrivent simplement des événements et la session identifie les types d’événements qu’il souhaite utiliser au niveau et aux mots clés. Si le fournisseur a défini un filtre de données pour un type d’événement, la session peut l’utiliser pour filtrer les événements pour ce type d’événement en fonction des données d’événement (la sémantique du filtre est définie par le fournisseur). Par exemple, si votre fournisseur génère des événements de processus, vous pouvez définir un filtre de données qui filtrant les événements de processus en fonction d’un identificateur de processus. La session peut ensuite passer un identificateur de processus comme données de filtre au fournisseur et recevoir uniquement les événements de processus pour cet identificateur de processus.

L’exemple suivant montre comment utiliser l’élément **Filter** pour définir un filtre. Vous devez spécifier les attributs **Name** et **value** du filtre. les autres attributs sont facultatifs. L’attribut **TID** est requis si le filtre exige que les données de filtre de la session passent.


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

                <filters>
                    <filter name="Pid"
                            value="1"
                            tid="t1"
                            symbol="FILTER_PID"/>
                </filters>

                <templates>
                    <template tid="t1">
                        <data name="Pid" inType="win:UInt32"/>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```