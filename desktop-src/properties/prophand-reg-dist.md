---
description: cet article explique comment inscrire et distribuer des gestionnaires de propriétés pour travailler avec le système de propriétés Windows.
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: Inscription et distribution des gestionnaires de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6a21ba1ae45848fd319d68bfee0624cf5686d3324cc4a3dff039dc94691cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867401"
---
# <a name="registering-and-distributing-property-handlers"></a>Inscription et distribution des gestionnaires de propriétés

cette rubrique explique comment créer et inscrire des gestionnaires de propriétés pour travailler avec le système de propriétés Windows.

Cette rubrique est organisée comme suit :

-   [Inscription et distribution des gestionnaires de propriétés](#registering-and-distributing-property-handlers)
-   [Considérations relatives aux performances et à la fiabilité pour les gestionnaires de propriétés](#performance-and-reliability-considerations-for-property-handlers)
    -   [Instructions relatives aux performances et à la fiabilité](#guidelines-for-performance-and-reliability)
-   [Rubriques connexes](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>Inscription et distribution des gestionnaires de propriétés

Une fois le gestionnaire de propriétés implémenté, il doit être inscrit et son extension de nom de fichier doit être associée au gestionnaire. L’exemple suivant qui utilise l’extension. Recipe illustre les entrées de Registre requises pour ce faire.

```
HKEY_CLASSES_ROOT
   CLSID
      {50d9450f-2a80-4f08-93b9-2eb526477d1a}
         (Default) = Recipe Property Handler
         ManualSafeSave [REG_DWORD] = 00000001
         InProcServer32
            (Default) = C:\\SDK\\PropertyHandlerSample\\bin\\RecipeHandlers.dll
            ThreadingModel = Apartment
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     .recipe
                        (Default) = {50d9450f-2a80-4f08-93b9-2eb526477d1a}
```

Les gestionnaires de propriétés pour un type de fichier particulier sont généralement distribués avec les applications qui créent ou manipulent des fichiers de ce type. Toutefois, vous devez également envisager de rendre vos gestionnaires de propriétés accessibles indépendamment de ces applications pour prendre en charge l’indexation de votre type de fichier dans les scénarios de serveur où les gestionnaires de propriétés sont utilisés par l’indexeur, mais leurs applications associées ne sont pas requises. Si vous créez un package d’installation autonome pour votre gestionnaire de propriétés, assurez-vous qu’il comprend les éléments suivants :

-   Détails d’inscription du gestionnaire de propriétés spécifiés dans la rubrique [inscription et distribution des gestionnaires de propriétés]().
-   L’inscription de votre type de fichier et de tous les fichiers de schéma qui doivent être installés, pour permettre aux clients d’accéder à toutes les fonctionnalités de votre gestionnaire de propriétés.

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>Considérations relatives aux performances et à la fiabilité pour les gestionnaires de propriétés

Les gestionnaires de propriétés sont appelés pour chaque fichier sur un ordinateur particulier. Elles sont généralement appelées dans les circonstances suivantes :

-   Lors de l’indexation du fichier. Cette opération est effectuée hors processus, dans un processus isolé avec des droits restreints.
-   lorsque l’accès aux fichiers s’effectue dans Windows Explorer afin de lire et d’écrire des valeurs de propriété. Cette opération est effectuée dans le processus.

### <a name="guidelines-for-performance-and-reliability"></a>Instructions relatives aux performances et à la fiabilité

À tout moment, un utilisateur peut avoir des dizaines de milliers de fichiers d’un type spécifique (y compris le vôtre) sur ses ordinateurs, et peut accéder à tout ou partie de ces fichiers à tout moment. Étant donné que les gestionnaires de propriétés sont souvent appelés pour prendre en charge ces opérations d’accès et de modification, les caractéristiques de performances et de fiabilité de votre gestionnaire de propriétés dans les environnements occupés et hautement simultanés revêtent une importance capitale.

Gardez à l’esprit les recommandations suivantes lors du développement et du test de votre gestionnaire de propriétés.

-   **Énumération des propriétés**

    Les gestionnaires de propriétés doivent avoir un temps de réponse très rapide dans l’énumération de leurs propriétés. Les calculs gourmands en mémoire des valeurs de propriété, les recherches sur le réseau ou la recherche de ressources autres que le fichier lui-même doivent être évités pour garantir des temps de réponse rapides.

-   **Écriture de propriété sur place**

    Si possible, si vous traitez des fichiers de taille moyenne ou grande (plusieurs centaines de Ko ou plus), le format de fichier doit être organisé afin que les valeurs de propriété de lecture ou d’écriture ne requièrent pas la lecture de l’ensemble du fichier sur le disque. même si le fichier doit être recherché, il ne doit pas être lu en mémoire dans son intégralité, car cela augmente la plage de travail de Windows Explorer ou de l’indexeur de recherche Windows lorsqu’il tente d’accéder à ces fichiers ou de les indexer. Pour plus d’informations, consultez [initialisation des gestionnaires de propriétés](./building-property-handlers-property-handlers.md).

    Pour ce faire, une technique utile consiste à remplir l’en-tête du fichier avec de l’espace supplémentaire afin que la valeur soit écrite à la prochaine fois qu’une valeur de propriété doit être écrite, sans qu’il soit nécessaire de réécrire la totalité du fichier. Cela nécessite la fonctionnalité ManualSafeSave. Cette approche implique un risque supplémentaire que l’opération d’écriture de fichier puisse être interrompue lorsque l’écriture est en cours (en raison d’un incident système ou d’une panne de courant), mais comme la taille des propriétés est généralement faible, la probabilité d’une telle interruption est similaire, et les gains de performance qui peuvent être réalisés par le biais de l’écriture de propriété sur place sont considérés comme Même dans ce cas, vous devez veiller à tester votre implémentation de manière intensive pour vous assurer que vos fichiers ne sont pas endommagés dans le cas où une défaillance survient au cours d’une opération d’écriture.

    Enfin, lors de l’implémentation de l’écriture de propriété sur place avec ManualSafeSave, il arrive que l’opération ne puisse pas être effectuée sur place et que le flux entier doive être réécrit de toute façon. Pour faciliter la réécriture, le flux fourni pendant l’initialisation du gestionnaire prend en charge l’interface [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) . L’interface **IDestinationStreamFactory** permet aux implémentations de gestionnaire d’obtenir un flux temporaire pour l’écriture. Lorsque toutes les écritures sont terminées et que la méthode [**IDestinationStreamFactory :: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) est appelée, ce flux est utilisé pour remplacer entièrement le flux de fichier d’origine. Lorsque le flux de destination est utilisé, le flux de fichier d’origine doit être traité en lecture seule, car il sera remplacé par le flux de destination après l’appel de la méthode **IDestinationStreamFactory :: GetDestinationStream** .

-   **Choix de votre modèle de thread COM**

    Pour optimiser l’efficacité de votre gestionnaire de propriétés, vous devez spécifier qu’il utilise le modèle de thread COM `Both` . cela permet un accès direct à partir des cloisonnements STA (Windows Explorer, par exemple) et des cloisonnements de l’agent de transfert des messages (MTA) (le processus SearchProtocolHost dans Windows Search, par exemple), ce qui évite la surcharge liée au marshaling dans ces environnements. Pour tirer pleinement parti du modèle de `Both` thread, tous les services dont dépend votre gestionnaire doivent également être désignés comme `Both` pour éviter tout marshaling dans les appels à ces composants. Consultez la documentation de ces services pour vérifier s’ils utilisent ce modèle de thread.

-   **Concurrence du gestionnaire de propriétés**

    Les gestionnaires de propriétés et l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sont conçus pour la série plutôt que pour l’accès simultané. Windows l’explorateur, l’indexeur de recherche Windows et tous les autres appels de gestionnaire de propriétés de la base de code Windows garantissent cette utilisation. Il n’y a aucune raison pour les tiers d’utiliser un gestionnaire de propriétés simultanément, mais ce comportement ne peut pas être garanti. De même, même si le modèle d’appel est supposé être série, les appels peuvent se trouver sur des threads différents (par exemple, lorsque l’objet est appelé à distance via COM RPC, comme dans l’indexeur). Par conséquent, les implémentations de gestionnaire de propriétés doivent prendre en charge l’appel de sur des threads différents. idéalement, ils ne doivent pas subir d’effets incorrects lorsqu’ils sont appelés simultanément. Étant donné que le modèle d’appel prévu est en série, une implémentation trivial à l’aide d’une section critique doit être suffisante pour répondre à ces exigences dans la plupart des cas. Il est acceptable d’éviter les blocages sur les appels simultanés à l’aide de la fonction [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) pour détecter et faire échouer les appels simultanés.

-   **Accès concurrentiel aux fichiers**

    Les gestionnaires de propriétés sont souvent utilisés dans les scénarios où plusieurs applications accèdent simultanément à un fichier. Par conséquent, le gestionnaire et les applications doivent gérer la concurrence en spécifiant les modes de partage appropriés lors de l’ouverture du fichier. Ils doivent également être conscients de l’accès que les autres applications spécifient et pour gérer les cas où l’accès n’est pas autorisé. Il est préférable que tous les consommateurs spécifient des modes de partage libérés pour permettre à d’autres utilisateurs d’accéder simultanément au fichier, mais dans ce cas, les problèmes de cohérence doivent être gérés. Les décisions sur les modes de partage les plus appropriés à utiliser doivent être établies dans le contexte de la communauté des applications qui accèdent au fichier.

    Les systèmes de fichiers permettent aux applications d’ouvrir des fichiers d’une façon qui leur permet de contrôler si d’autres applications peuvent ou non ouvrir le fichier. Les modes de partage permettent l’accès en lecture, en écriture et en suppression. Le système de propriétés prend en charge un sous-ensemble de ces modes de partage, décrits dans le tableau suivant.

    

    | Mode d’accès                     | Mode de partage                             |
    |---------------------------------|------------------------------------------|
    | Write                           | Refuser d’autres lecteurs et Writers           |
    | Écriture (EnableShareDenyWrite)    | Activation d’autres lecteurs, refus d’autres enregistreurs |
    | Lecture seule (par défaut)             | Activation d’autres lecteurs, refus d’autres enregistreurs |
    | Lecture seule (EnableShareDenyNone) | Activer d’autres lecteurs et Writers         |

    

     

    Les gestionnaires de propriétés ouverts pour l' **écriture** (GPS \_ ReadWrite) refusent d’autres lecteurs et enregistreurs. Les gestionnaires peuvent s’abonner à un comportement qui permet aux lecteurs de spécifier l' `EnableShareDenyWrite` indicateur (en impliquant l’activation de la lecture) dans son inscription.

    Les gestionnaires de propriétés ouverts en **lecture** (GPS \_ par défaut) activent par défaut d’autres lecteurs, mais refusent d’autres enregistreurs. Les gestionnaires peuvent choisir d’activer d’autres enregistreurs en spécifiant l' `EnableShareDenyNone` indicateur dans son inscription. Cela signifie qu’un gestionnaire peut gérer avec succès une situation dans laquelle le contenu d’un fichier change pendant que le gestionnaire lit le fichier.

    Pour les définitions d’indicateurs, consultez [**GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnement des gestionnaires de propriétés](./building-property-handlers-properties.md)
</dt> <dt>

[Utilisation des noms de genres](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Utilisation des listes de propriétés](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisation des gestionnaires de propriétés](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Meilleures pratiques pour le gestionnaire de propriétés et FAQ](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
