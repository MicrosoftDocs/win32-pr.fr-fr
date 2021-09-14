---
title: Signature racine version 1.1
description: L’objectif de la version de signature racine 1,1 est de permettre aux applications d’indiquer aux pilotes quand les descripteurs d’un tas de descripteur ne changeront pas ou que les descripteurs de données ne changeront pas.
ms.assetid: 8FE42C1C-7F1D-4E70-A7EE-D5EC67237327
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a7a32576efa4d93a8d26aa57282f06e0d5a02f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012885"
---
# <a name="root-signature-version-11"></a>Signature racine version 1.1

L’objectif de la version de signature racine 1,1 est de permettre aux applications d’indiquer aux pilotes quand les descripteurs d’un tas de descripteur ne changeront pas ou que les descripteurs de données ne changeront pas. Cela permet aux pilotes d’effectuer des optimisations qui peuvent être possibles, sachant qu’un descripteur ou la mémoire vers laquelle il pointe est statique pendant un certain temps.

-   [Vue d'ensemble](#overview)
-   [Indicateurs statiques et volatiles](#static-and-volatile-flags)
    -   [descripteurs \_ volatils](#descriptors_volatile)
    -   [DONNÉES \_ volatiles](#data_volatile)
    -   [données \_ statiques quand elles sont \_ \_ définies \_ lors de l' \_ exécution](#data_static_while_set_at_execute)
    -   [DONNÉES \_ statiques](#data_static)
    -   [Combinaison d’indicateurs](#combining-flags)
    -   [Résumé de l’indicateur](#flag-summary)
-   [Résumé de l’API version 1,1](#version-11-api-summary)
    -   [Énumérations](#enums)
    -   [Structures](#helper-structures)
    -   [Fonctions](#functions)
    -   [Méthodes](#methods)
    -   [Structures d’assistance](#helper-structures)
-   [Conséquences de la violation des indicateurs de caractère statique](#consequences-of-violating-static-ness-flags)
-   [Gestion des versions](#version-management)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

La version de signature racine 1,0 autorise le contenu des tas de descripteurs et la mémoire qu’ils pointent à être librement modifiés par les applications chaque fois que les listes de commandes/regroupements qui les référencent sont potentiellement en vol sur le GPU. Très souvent, cependant, les applications n’ont pas besoin de la flexibilité nécessaire pour modifier les descripteurs ou la mémoire une fois que les commandes qui les référencent ont été enregistrées.

Les applications sont souvent en mesure de :

-   Configurez les descripteurs (et éventuellement la mémoire à laquelle ils pointent) avant de lier les tables de descripteurs ou les descripteurs racine sur une liste de commandes ou un bundle.
-   Veillez à ce que ces descripteurs ne changent pas jusqu’à ce que la liste de commandes/bundles qui les référence aient fini de s’exécuter pour la dernière fois.
-   Vérifiez que les données vers lesquelles pointent les descripteurs ne changent pas pour la même durée complète.

En guise d’alternative, une application peut uniquement être en mesure de faire en sorte que les données ne changent pas pour une durée plus petite dans le temps. En particulier, les données peuvent être statiques pour la fenêtre dans le temps lors de l’exécution de la liste de commandes qu’une liaison de paramètre racine (table de descripteurs ou descripteur racine) pointe actuellement vers les données. En d’autres termes, une application peut souhaiter exécuter l’exécution sur la chronologie GPU qui met à jour des données entre les périodes où elles sont définies via un paramètre racine, sachant que lorsqu’elle est définie, elle est statique.

Si les descripteurs ou les descripteurs de données pointent vers, ne changeront pas, les pilotes d’optimisations spécifiques peuvent être spécifiques à un fabricant de matériel et, de manière importante, ils ne modifient pas le comportement, sauf pour améliorer les performances. Conserver le plus grand nombre d’informations sur l’intention de l’application que possible n’entraîne pas de charge sur les applications.

L’une des optimisations est que de nombreux pilotes peuvent produire des accès mémoire plus efficaces par les nuanceurs s’ils savent les promesses qu’une application peut faire sur la nature statique des descripteurs et des données. Par exemple, les pilotes peuvent supprimer un niveau d’indirection pour accéder à un descripteur dans un segment de mémoire en le convertissant en descripteur racine si le matériel particulier n’est pas sensible à la taille de l’argument racine.

La tâche supplémentaire pour le développeur qui utilise la version 1,1 consiste à faire des promesses quant à la volatilité et à la nature statique des données, dans la mesure du possible, afin que les pilotes puissent effectuer les optimisations nécessaires. Les développeurs n’ont pas à prendre de promesses quant à la nature statique.

La version de signature racine 1,0 continue à fonctionner sans modification, bien que les applications qui recompilent les signatures racines aient la signature racine 1,1 maintenant (avec une option permettant de forcer la version 1,0, si vous le souhaitez).

## <a name="static-and-volatile-flags"></a>Indicateurs statiques et volatiles

Les indicateurs suivants font partie de la signature racine pour permettre aux pilotes de choisir une stratégie permettant de mieux gérer les arguments racine individuels lorsqu’ils sont définis, et d’incorporer également les mêmes hypothèses dans les objets d’état de pipeline (objets PSO) quand ils sont compilés à l’origine, car la signature racine fait partie d’un objet PSO.

Les indicateurs suivants sont définis par l’application et s’appliquent aux descripteurs ou aux données.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_FLAGS
{
    D3D12_DESCRIPTOR_RANGE_FLAG_NONE    = 0,
    D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE    = 0x1,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE   = 0x2,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE    = 0x4,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC = 0x8
} D3D12_DESCRIPTOR_RANGE_FLAGS;

typedef enum D3D12_ROOT_DESCRIPTOR_FLAGS
{
    D3D12_ROOT_DESCRIPTOR_FLAG_NONE = 0,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE    = 0x2,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE = 0x4,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC  = 0x8
} D3D12_ROOT_DESCRIPTOR_FLAGS;
```

### <a name="descriptors_volatile"></a>descripteurs \_ volatils

Avec cet indicateur défini, les descripteurs d’un tas de descripteurs vers lequel pointe une table de descripteurs racine peuvent être modifiés par l’application à tout moment, sauf pendant que la liste de commandes/bottes qui lient la table de descripteur ont été soumises et n’ont pas terminé leur exécution. Par exemple, l’enregistrement d’une liste de commandes et la modification des descripteurs dans un tas de descripteurs auquel elle fait référence *avant* d’envoyer la liste de commandes pour qu’elle soit exécutée sont valides. Il s’agit du seul comportement pris en charge pour la signature racine version 1,0.

Si l' \_ indicateur volatiles DEscripteurs n’est *pas* défini, les descripteurs sont statiques. Il n’existe aucun indicateur pour ce mode. Les descripteurs statiques signifient que les descripteurs d’un tas de descripteur désigné par une table de descripteurs racine ont été initialisés au moment où la table du descripteur est définie sur une liste de commandes/un bundle (lors de l’enregistrement), et les descripteurs ne peuvent pas être modifiés tant que l’exécution de la liste de commandes/Bundle *Pour la signature racine version 1,1, les descripteurs statiques sont l’hypothèse par défaut*, et l’application doit spécifier l’indicateur volatil descripteurs lorsque cela est \_ nécessaire.

Pour les regroupements utilisant des tables de descripteurs avec des descripteurs statiques, les descripteurs doivent être prêts à partir du moment où l’offre groupée est enregistrée (par opposition au fait que le bundle est appelé), et non changer jusqu’à ce que l’offre groupée ait fini de s’exécuter pour la dernière fois. Les tables de descripteurs qui pointent vers des descripteurs statiques doivent être définies lors de l’enregistrement de Bundle et ne pas être héritées dans le bundle. Il est possible pour une liste de commandes d’utiliser une table de descripteur avec des descripteurs statiques qui a été définie dans un bundle et renvoyée à la liste de commandes.

Lorsque les descripteurs sont statiques, il existe un autre changement de comportement qui requiert la \_ définition de l’indicateur volatil DEscripteurs. Les accès hors limites aux vues de mémoire tampon (par opposition aux affichages Texture1D/2D/3D/cube) ne sont pas valides et produisent des résultats indéfinis, y compris la réinitialisation d’appareil possible, au lieu de retourner des valeurs par défaut pour les écritures de lecture ou de suppression. L’objectif de la suppression de la capacité des applications à dépendre du matériel en dehors des limites d’accès est de permettre aux pilotes de choisir de promouvoir les accès au descripteur statique en accès au descripteur racine s’ils estiment qu’ils sont plus efficaces. Les descripteurs racine ne prennent pas en charge la vérification hors limites.

Si les applications dépendent du comportement d’accès à la mémoire en dehors des limites lors de l’accès aux descripteurs, ils doivent marquer les plages du descripteur qui accèdent à ces descripteurs en tant que descripteurs \_ volatils.

### <a name="data_volatile"></a>DONNÉES \_ volatiles

Lorsque cet indicateur est défini, les données vers lesquelles pointent les descripteurs peuvent être modifiées par l’UC à tout moment, sauf lorsque la liste de commandes/les offres groupées qui lient la table de descripteur ont été soumises et n’ont pas terminé leur exécution. Il s’agit du seul comportement pris en charge pour la signature racine version 1,0.

L’indicateur est disponible dans les indicateurs de plage de descripteurs et les indicateurs de descripteur racine.

### <a name="data_static_while_set_at_execute"></a>données \_ statiques quand elles sont \_ \_ définies \_ lors de l' \_ exécution

Lorsque cet indicateur est défini, les données pointées par les descripteurs ne peuvent pas changer à partir du moment où le descripteur racine ou la table de descripteur sous-jacent est défini sur une liste de commandes/un bundle lors de l’exécution sur la chronologie GPU, et se termine lorsque les tirages/distributions suivants ne font plus référence aux données.

Pour qu’un descripteur ou une table de descripteur racine ait été défini sur le GPU, ces données *peuvent* être modifiées même par la même liste de commandes/regroupement. Les données peuvent également être modifiées lorsqu’un descripteur ou une table de descripteur racine pointant sur celle-ci est toujours défini sur la liste de commandes/le bundle, à condition que les dessins/distributions qui y font référence soient terminés. Toutefois, cette opération nécessite que la table de descripteurs soit à nouveau reliée à la liste de commandes avant la prochaine déréférencement du descripteur racine ou de la table de descripteur. Cela permet au pilote de savoir que les données vers lesquelles pointe un descripteur racine ou une table de descripteur ont été modifiées.

La principale différence entre les données \_ statiques lorsque celles- \_ ci sont définies lors de l' \_ \_ \_ exécution et la \_ volatilité des données est avec des données \_ volatiles. un pilote ne peut pas déterminer si les copies de données dans une liste de commandes ont modifié les données pointées par un descripteur, sans effectuer de suivi d’État supplémentaire. Par conséquent, si, par exemple, un pilote peut insérer une sorte de commandes de pré-extraction de données dans sa liste de commandes (pour améliorer l’accès des nuanceurs aux données connues, par exemple, \_ les données statiques \_ quand elles sont définies au moment de l' \_ \_ \_ exécution permettent au pilote de savoir qu’il n’a besoin d’effectuer la prérécupération des données qu’au moment où il est défini via [**SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable), [**SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) ou l’une des méthodes permettant de définir la vue de la mémoire tampon constante, la vue des ressources du nuanceur ou la vue d’accès non triée.

Pour les offres groupées, la promesse selon laquelle les données sont statiques lorsqu’elles sont définies lors de l’exécution s’applique de façon unique à chaque exécution de l’offre groupée.

L’indicateur est disponible dans les indicateurs de plage de descripteurs et les indicateurs de descripteur racine.

### <a name="data_static"></a>DONNÉES \_ statiques

Si cet indicateur est défini, les données pointées par descripteurs ont été initialisées au moment où une table de descripteurs ou un descripteur racine référençant la mémoire a été définie sur une liste de commandes/un bundle lors de l’enregistrement, et les données ne peuvent pas être modifiées tant que l’exécution de la liste de commandes/Bundle n’a pas été terminée.

Pour les offres groupées, la durée statique commence au descripteur racine ou au paramètre de table du descripteur lors de l’enregistrement du bundle, par opposition à l’enregistrement d’une liste de commandes appelante. En outre, une table de descripteurs pointant vers des données statiques doit être définie dans le bundle et non héritée. Il est possible pour une liste de commandes d’utiliser une table de descripteurs pointant vers des données statiques qui a été définie dans un bundle et renvoyée à la liste de commandes.

L’indicateur est disponible dans les indicateurs de plage de descripteurs et les indicateurs de descripteur racine.

### <a name="combining-flags"></a>Combinaison d’indicateurs

Au plus l’un des indicateurs de données peut être spécifié à la fois, à l’exception des plages de descripteurs d’échantillonnage qui ne prennent pas en charge les indicateurs de données, car les échantillonneurs ne pointent pas vers les données.

L’absence de tout indicateur de données pour les plages de descripteurs SRV et CBV signifie qu’il s’agit d’une valeur par défaut de DATA \_ static \_ alors que \_ Set \_ at \_ Execute Behavior est supposé. La raison pour laquelle cette valeur par défaut est choisie au lieu de données \_ statiques est que les données \_ statiques définies lors de l' \_ \_ \_ \_ exécution sont bien plus susceptibles d’être une valeur par défaut sécurisée pour la plupart des cas, tout en continuant à améliorer l’opportunité d’optimisation par rapport aux données \_ volatiles par défaut.

L’absence d’indicateurs de données pour les plages de descripteurs UAV signifie qu’une valeur par défaut de données \_ volatiles est supposée, étant donné que les UAVs sont écrits en général.

Les descripteurs \_ volatiles *ne peuvent pas* être associés à des données \_ statiques, mais *peuvent* être combinés avec d’autres indicateurs de données. Les descripteurs \_ de raison volatile peuvent être combinés avec des données \_ statiques \_ alors qu’ils sont définis lors de l’exécution. \_ \_ \_ les descripteurs volatils requièrent toujours que les descripteurs soient prêts pendant l’exécution de la liste de commandes/de l’offre groupée, et les données \_ statiques \_ quand elles sont définies au moment de l’exécution ne \_ \_ \_ sont que des promesses sur le caractère statique

### <a name="flag-summary"></a>Résumé de l’indicateur

Les tableaux suivants résument les combinaisons d’indicateurs qui peuvent être utilisées.



| Paramètres valides des \_ indicateurs de plage du descripteur D3D12 \_ \_                                                               | Description                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aucun indicateur défini                                                   | Les descripteurs sont statiques (valeur par défaut). Hypothèses par défaut pour les données : pour SRV/CBV : données \_ statiques définies lors de l' \_ \_ \_ \_ exécution, et pour UAV : données \_ volatiles. Ces valeurs par défaut pour SRV/CBV s’adaptent en toute sécurité aux modèles d’utilisation pour la majorité des signatures racines.                                                                                              |
| DONNÉES \_ statiques                                                   | Les descripteurs et les données sont statiques. Cela optimise le potentiel d’optimisation du pilote.                                                                                                                                                                                                                                                          |
| DONNÉES \_ volatiles                                                 | Les descripteurs sont statiques et les données sont volatiles.                                                                                                                                                                                                                                                                                                     |
| données \_ statiques quand elles sont \_ \_ définies \_ lors de l' \_ exécution                          | Les descripteurs sont statiques et les données sont statiques quand elles sont définies lors de l’exécution.                                                                                                                                                                                                                                                                                      |
| descripteurs \_ volatils                                          | Les descripteurs sont volatiles, et les hypothèses par défaut sont effectuées sur les données : pour SRV/CBV : données statiques quand elles sont définies lors de l' \_ \_ \_ \_ \_ exécution, et pour UAV : données \_ volatiles.                                                                                                                                                                                              |
| descripteurs \_ volatiles \| données \_ volatiles                        | Les descripteurs et les données sont volatils, ce qui équivaut à la signature racine 1,0.                                                                                                                                                                                                                                                                            |
| descripteurs \_ volatiles \| Data \_ static \_ quand elles sont \_ définies \_ lors de l' \_ exécution | Les descripteurs sont volatiles, mais notez qu’ils ne peuvent toujours pas changer au cours de l’exécution de la liste de commandes. Par conséquent, il est possible de combiner la déclaration supplémentaire selon laquelle les données sont statiques quand elles sont définies via la table de descripteurs racine au cours de l’exécution. les descripteurs sous-jacents sont effectivement statiques pendant plus longtemps que les données sont promis d’être statiques. |



 



| Paramètres valides des \_ \_ indicateurs de descripteurs racine D3D12 \_                                                  |  Description                                                                                                                                                                                                                 |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aucun indicateur défini                                      | Hypothèses par défaut pour les données : pour SRV/CBV : données \_ statiques définies lors de l' \_ \_ \_ \_ exécution, et pour UAV : données \_ volatiles. Ces valeurs par défaut pour SRV/CBV s’adaptent en toute sécurité aux modèles d’utilisation pour la majorité des signatures racines. |
| DONNÉES \_ statiques                                      | Les données sont statiques, ce qui constitue le meilleur risque pour l’optimisation des pilotes.                                                                                                                                                       |
| données \_ statiques quand elles sont \_ \_ définies \_ lors de l' \_ exécution             | Les données sont statiques lorsqu’elles sont définies lors de l’exécution.                                                                                                                                                                              |
| DONNÉES \_ volatiles                                    | Équivalent à la signature racine 1,0.                                                                                                                                                                                 |



 

## <a name="version-11-api-summary"></a>Résumé de l’API version 1,1

Les appels d’API suivants activent la version 1,1.

### <a name="enums"></a>Énumérations

Ces énumérations contiennent les indicateurs de clé pour spécifier le descripteur et la volatilité des données.

-   [**D3D \_ \_ \_ Version de la signature racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version) : ID de version.
-   [**D3D12 \_ \_ \_ Indicateurs de plage du descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) : plage d’indicateurs déterminant si les descripteurs ou les données sont volatiles ou statiques.
-   [**D3D12 \_ \_ \_ Indicateurs de descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) : une plage similaire d’indicateurs aux [**indicateurs de \_ \_ plage \_ de descripteurs D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags), sauf que seuls les indicateurs de données s’appliquent aux descripteurs racine.

### <a name="structures"></a>Structures

Les structures mises à jour (à partir de la version 1,0) contiennent des références aux indicateurs volatiles/statiques.

-   [**D3D12 \_ \_ \_ \_ Signature**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature) de la racine des données de fonctionnalité : transmettez cette structure à [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) pour vérifier la prise en charge de la version 1,1 de la signature racine.
-   [**D3D12 \_ Description de \_ la \_ signature \_ racine avec version**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) : peut contenir n’importe quelle version d’une description de signature racine et est conçue pour être utilisée avec les fonctions de sérialisation/désérialisation listées ci-dessous.
-   Ces structures sont équivalentes à celles utilisées dans la version 1,0, avec l’ajout de nouveaux champs d’indicateurs pour les plages de descripteurs et les descripteurs racines :

    -   [**\_Signature racine \_ D3D12 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)
    -   [**\_Descripteur D3D12 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
    -   [**\_Descripteur racine D3D12 \_ \_ table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
    -   [**D3D12 \_ racine \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
    -   [**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

### <a name="functions"></a>Fonctions

Les méthodes répertoriées ici remplacent les fonctions [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) et [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) d’origine, car elles sont conçues pour fonctionner sur n’importe quelle version de signature racine. La forme sérialisée est celle qui est transmise à l’API [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) . Si un nuanceur a été créé avec une signature racine dans celui-ci, le nuanceur compilé contient déjà une signature racine sérialisée.

-   [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) : si une application génère de manière procédurale la structure des données de [**\_ \_ \_ signature racine avec version D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) , elle doit faire de la forme sérialisée à l’aide de cette fonction.
-   [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) : génère une interface qui peut retourner la structure de données désérialisée, via [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).

### <a name="methods"></a>Méthodes

L’interface [**ID3D12VersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) est créée pour désérialiser la structure de données de la signature racine.

-   [**GetRootSignatureDescAtVersion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion) : convertit les structures de description de signature racine en une version demandée.
-   [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) : retourne un pointeur vers une [**structure \_ \_ \_ \_ desc de signature racine avec version D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

### <a name="helper-structures"></a>Structures d’assistance

Des structures d’assistance ont été ajoutées pour faciliter l’initialisation de certaines structures de la version 1,1.

-   \_Descripteur CD3DX12 \_ RANGE1
-   CD3DX12 \_ racine \_ paramètre1
-   CD3DX12 \_ statique \_ SAMPLER1
-   Description de la \_ signature racine avec version CD3DX12 \_ \_ \_ desc

Reportez-vous aux [structures et fonctions d’assistance pour D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="consequences-of-violating-static-ness-flags"></a>Conséquences de la violation des indicateurs de caractère statique

Les indicateurs de descripteur et de données décrits ci-dessus (ainsi que les valeurs par défaut implicites en l’absence d’indicateurs particuliers) définissent une promesse par l’application au pilote sur la manière dont il va se comporter. Si une application ne respecte pas la promesse, le comportement n’est pas valide : les résultats ne sont pas définis et peuvent être différents sur différents pilotes et matériels.

La couche de débogage offre des options pour valider que les applications respectent leurs promesses, y compris les promesses par défaut qui sont fournies avec l’utilisation de la signature racine version 1,1 sans définir d’indicateurs.

## <a name="version-management"></a>Gestion des versions

Lors de la compilation des signatures racines attachées aux nuanceurs, les nouveaux compilateurs HLSL compilent par défaut la signature racine à la version 1,1, alors que les anciens compilateurs HLSL prennent uniquement en charge 1,0. Notez que les signatures racines 1,1 ne fonctionneront pas sur les systèmes d’exploitation qui ne prennent pas en charge la signature racine 1,1.

La version de signature racine compilée avec un nuanceur peut être forcée à une version particulière à l’aide de `/force_rootsig_ver <version>` . Forcer la version échoue si le compilateur peut conserver le comportement de la signature racine qui est compilée dans la version forcée, par exemple en supprimant les indicateurs non pris en charge dans la signature racine qui servent uniquement à des fins d’optimisation, mais n’affectent pas le comportement.

Ainsi, une application peut, par exemple, compiler une signature racine 1,1 à 1,0 et 1,1 lors de la génération de l’application et sélectionner la version appropriée au moment de l’exécution en fonction du niveau de prise en charge du système d’exploitation. Toutefois, l’espace est plus efficace pour une application de compiler des signatures racines individuellement (surtout si plusieurs versions sont nécessaires), séparément des nuanceurs. Même si les nuanceurs ne sont pas initialement compilés avec une signature racine jointe, l’avantage de la validation par le compilateur de la compatibilité de signature racine avec un nuanceur peut être préservé à l’aide de l' `/verifyrootsignature` option du compilateur. Plus tard, lors de l’exécution, objets PSO peut être créé à l’aide de nuanceurs qui n’ont pas de signature racine dans ces derniers, tout en transmettant la signature racine souhaitée (peut-être la version appropriée prise en charge par le système d’exploitation) en tant que paramètre distinct.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une signature racine](creating-a-root-signature.md)
</dt> <dt>

[Signatures racine](root-signatures.md)
</dt> <dt>

[Spécification de signatures racine en langage HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 




