---
title: Écriture d’un manifeste d’instrumentation
description: Les applications et les DLL utilisent un manifeste d’instrumentation pour identifier leurs fournisseurs d’instrumentation et les événements que les fournisseurs écrivent.
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381993"
---
# <a name="writing-an-instrumentation-manifest"></a>Écriture d’un manifeste d’instrumentation

Les applications et les DLL utilisent un manifeste d’instrumentation pour identifier leurs fournisseurs d’instrumentation et les événements que les fournisseurs écrivent. Un manifeste est un fichier XML qui contient les éléments qui identifient votre fournisseur. La Convention consiste à utiliser. Man comme extension pour votre manifeste. Le manifeste doit être conforme au fichier XSD du manifeste d’événements. Pour plus d’informations sur le schéma, consultez [schéma EventManifest](eventmanifestschema-schema.md).

Un fournisseur d’instrumentation est une application ou une DLL qui appelle les fonctions [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)ou [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) pour écrire des événements dans une session de suivi de [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) ou un canal de journal des événements. Une application peut définir un fournisseur d’instrumentation unique qui couvre tous les événements qu’elle écrit ou elle peut définir un fournisseur pour l’application et un fournisseur pour chacune de ses dll. Le nombre de fournisseurs que l’application définit dans le manifeste dépend uniquement de la façon dont l’application souhaite organiser les événements qu’elle écrit.

L’avantage de spécifier un fournisseur pour chaque DLL est que vous pouvez ensuite activer et désactiver les fournisseurs individuels et donc les événements qu’ils génèrent. Cet avantage s’applique uniquement si le fournisseur est activé par une session de suivi ETW. Tous les événements qui spécifient un canal du journal des événements sont toujours écrits sur ce canal.

Le manifeste doit identifier le fournisseur et les événements qu’il écrit, mais les autres métadonnées, telles que les canaux, les niveaux et les mots clés, sont facultatives. la définition des métadonnées facultatives dépend de la personne qui utilisera les événements. Par exemple, si les administrateurs ou le personnel du support technique consomment les événements à l’aide d’un outil tel que le observateur d’événements Windows qui lit les événements à partir de canaux du journal des événements, vous devez définir les canaux sur lesquels les événements sont écrits. Toutefois, si le fournisseur est activé uniquement par une session de suivi ETW, vous n’avez pas besoin de définir de canaux.

Bien que les métadonnées des niveaux, des tâches, des OpCodes et des mots clés soient facultatives, vous devez les utiliser pour regrouper ou compartir les événements de manière logique. Le regroupement des événements permet aux consommateurs de consommer uniquement les événements intéressants. Par exemple, le consommateur peut interroger tous les événements où le niveau est « critique » et le mot clé « écriture », ou interroger tous les événements écrits par une tâche spécifique.

En plus des consommateurs utilisant le niveau et les mots clés pour utiliser des types spécifiques d’événements, une session de suivi ETW peut utiliser les métadonnées de niveau et de mot clé pour indiquer à ETW de limiter les événements écrits dans le journal de suivi d’événements. Par exemple, la session peut limiter les événements aux événements où le niveau est « erreur » ou « critique » et le mot clé est « lecture ».

Un fournisseur peut définir des filtres utilisés par une session pour filtrer les événements en fonction des données d’événement. Avec le niveau et les mots clés, ETW détermine si l’événement est écrit dans le journal, mais avec des filtres, le fournisseur utilise les critères de données de filtre pour déterminer s’il écrit l’événement dans cette session. Les filtres s’appliquent uniquement quand une session de suivi ETW active votre fournisseur.

Les sections suivantes montrent comment définir les composants du manifeste :

-   [Identification du fournisseur](identifying-the-provider.md)
-   [Définition des canaux à l’endroit où les événements sont écrits](defining-channels.md)
-   [Définition des niveaux de gravité des événements écrits par le fournisseur](defining-severity-levels.md)
-   [Définition des tâches et des opérations effectuées par votre fournisseur](defining-tasks-and-opcodes.md)
-   [Définition des mots clés qui classent les événements écrits par le fournisseur](defining-keywords-used-to-classify-types-of-events.md)
-   [Définition des filtres que le fournisseur utilise pour filtrer les événements qu’il écrit](defining-filters.md)
-   [Définition des mappages nom/valeur référencés par vos données de modèle](defining-name-value-mappings.md)
-   [Définition des modèles qui définissent les données spécifiques aux événements](defining-event-data-templates.md)
-   [Définition des événements que le fournisseur écrit](defining-events.md)

Bien que vous puissiez créer un manifeste d’instrumentation manuellement, vous devez envisager d’utiliser l’outil ECManGen.exe inclus dans le \\ dossier bin du SDK Windows. L’outil ECManGen.exe utilise une interface utilisateur graphique qui vous guide tout au long de la création d’un manifeste sans jamais avoir à utiliser des balises XML. La connaissance des informations contenues dans cette section et dans la section [schéma EventManifest](eventmanifestschema-schema.md) vous aidera lors de l’utilisation de l’outil.

Si vous utilisez Visual Studio comme éditeur XML, vous pouvez ajouter le schéma [EventManifest](eventmanifestschema-schema.md) au projet (consultez le menu XML) pour tirer parti d’IntelliSense, de la validation de schéma inline et d’autres fonctionnalités pour faciliter l’écriture du manifeste.

Après avoir écrit votre manifeste, utilisez le compilateur de message pour valider le manifeste et générer les fichiers de ressources et d’en-tête que vous incluez dans votre fournisseur. Pour plus d’informations, consultez [compilation d’un manifeste d’instrumentation](compiling-an-instrumentation-manifest.md).

L’exemple suivant illustre la structure d’un manifeste d’événements entièrement défini.


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
                    <importChannel .../>
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



 

 