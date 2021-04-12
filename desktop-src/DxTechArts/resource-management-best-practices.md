---
title: Meilleures pratiques pour la gestion des ressources
description: Cet article décrit les meilleures pratiques pour traiter les ressources en général, le comportement des ressources managées et non managées, et fournit des détails sur la façon dont les ressources sont généralement gérées par le runtime et les pilotes.
ms.assetid: 265ae0b2-f268-a4a4-551e-9d3dae886517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cdadb8cee3cb57f4208657054784937ecd1ea2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315857"
---
# <a name="resource-management-best-practices"></a>Meilleures pratiques pour la gestion des ressources

Les textures gérées, également appelées « gestion de texture automatique », sont disponibles dans DirectX depuis la version 6, avec plusieurs révisions et améliorations apportées dans les versions ultérieures. À compter de la sortie de l’API Direct3D 9, la gestion automatique des ressources prend en charge les textures, les mémoires tampons de vertex et les tampons d’index, avec une interface partagée cohérente. À l’aide de Direct3D Resource Manager, les applications peuvent simplifier de manière considérable la gestion des situations de périphériques perdus et peuvent compter sur le système pour gérer une quantité raisonnable de ressources de mémoire vidéo.

Les développeurs ont parfois des difficultés à utiliser les ressources managées, en partie en raison de la nature abstraite du système. Si de nombreux scénarios courants pour les ressources sont adaptés aux ressources managées, certains cas fonctionnent mieux lors de l’utilisation de ressources non managées. Cet article décrit les meilleures pratiques pour traiter les ressources en général, le comportement des ressources managées et non managées, et fournit des détails sur la façon dont les ressources sont généralement gérées par le runtime et les pilotes.

Cet article aborde les concepts suivants :

-   [Mémoire vidéo](#video-memory)
-   [Ressources managées](#managed-resources)
-   [Ressources gérées par le pilote](#driver-managed-resources)
-   [Ressources par défaut](#default-resources)
    -   [Utilisation des ressources gérées et par défaut](#using-both-managed-and-default-resources)
    -   [Ressources dynamiques par défaut](#dynamic-default-resources)
-   [Ressources mémoire système](#system-memory-resources)
-   [Recommandations générales](#general-recommendations)
-   [Rubriques connexes](#related-topics)

## <a name="video-memory"></a>Mémoire vidéo

Pour que le système vidéo utilise une ressource, il doit se trouver dans la mémoire accessible au GPU. La mémoire vidéo locale offre les meilleures performances pour le GPU, et certaines ressources (telles que les cibles de rendu et les tampons de profondeur/stencil) doivent se trouver dans la mémoire vidéo locale. Avec l’avènement de l’AGP, le GPU peut également accéder directement à une partie de la mémoire système. Cette zone mémoire, connue sous le nom d’ouverture AGP, est appelée mémoire vidéo non locale et n’est pas disponible à d’autres fins. La mémoire vidéo non locale peut être lue et écrite par le processeur, ce qui n’a généralement aucun accès hautes performances à la mémoire vidéo locale et est donc idéal pour une utilisation en tant que ressource de mémoire partagée. L’un des éléments clés à retenir au sujet de la mémoire AGP est qu’elle n’est pas validée dans les situations de perte de l’appareil et que les ressources persistantes qu’elle contient doivent être restaurées.

**Figure 1. Relation entre le GPU, le processeur, la RAM vidéo et la RAM système**

![relation entre le GPU, le processeur, la RAM vidéo et la RAM système](images/managingresources1.gif)

Certaines solutions vidéo intégrées utilisent une architecture de mémoire unifiée (UMA), où la mémoire principale est adressable par tous les composants des systèmes. Direct3D prend en charge la UMA sans nécessiter de modification de l’application, en utilisant les mêmes indications que pour les configurations de mémoire vidéo locales. Pour ces systèmes, les ressources se trouvent toujours dans la mémoire système, et le pilote est chargé de s’assurer que les ressources fonctionnent comme dans une architecture plus traditionnelle tout en tirant parti des propriétés de la mémoire UMA et de tout comportement spécifique de l’implémentation matérielle.

**Figure 2. Le GPU et le processeur ont un accès égal à la RAM système dans une architecture de mémoire unifiée**

![le GPU et le processeur ont un accès égal à la RAM système dans une architecture de mémoire unifiée](images/managingresources2.gif)

## <a name="managed-resources"></a>Ressources managées

La majorité de vos ressources doit être créée en tant que ressources managées dans le POOL \_ géré. Toutes vos ressources seront créées dans la mémoire système, puis copiées en fonction des besoins dans la mémoire vidéo. Les situations de périphérique perdu seront gérées automatiquement à partir de la copie de la mémoire système. Étant donné que toutes les ressources managées ne doivent pas être intégrées à la mémoire vidéo en même temps, vous pouvez surcharger la mémoire là où une plus petite plage de travail de mémoire vidéo est nécessaire pour effectuer le rendu dans un frame donné. Notez qu’il est probable que la majeure partie de la mémoire système du magasin de stockage soit paginée sur le disque dans le temps, ce qui explique pourquoi l’opération de réinitialisation peut être lente en raison de la nécessité de repaginer ces données pour restaurer la mémoire vidéo perdue.

Le runtime conserve un horodateur pour la dernière fois qu’une ressource est utilisée, et lorsqu’une allocation de mémoire vidéo échoue pour le chargement d’une ressource managée nécessaire, elle libère les ressources en fonction de cet horodatage de manière LRU. L’utilisation de [**SetPriority**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) est prioritaire sur l’horodatage, donc les ressources les plus couramment utilisées doivent être définies sur une valeur de priorité plus élevée. Direct3D 9,0 a des informations limitées sur la mémoire vidéo gérée par le pilote. par conséquent, le runtime devra peut-être supprimer plusieurs ressources pour créer une région suffisamment grande pour que l’allocation aboutisse. Des priorités appropriées peuvent vous aider à éliminer les situations où un événement est supprimé, puis retenu à peu près après. L’application peut également appeler [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) pour forcer la suppression de toutes les ressources managées. Là encore, cette opération peut prendre du temps pour recharger toutes les ressources requises pour le frame suivant, mais elle est très utile pour les transitions de niveau où la plage de travail change de façon significative et pour la suppression de la fragmentation de la mémoire vidéo.

Un nombre de frames est également conservé pour permettre au runtime de détecter si la ressource qu’il vient de choisir de supprimer a été utilisée au début du frame actuel, ce qui implique une situation de surcharge où davantage de ressources sont utilisées dans une trame unique que dans la mémoire vidéo. Cela déclenche la stratégie de remplacement pour basculer vers un dernier format au lieu d’un LRU pour le reste du cadre, car cela a tendance à s’exécuter légèrement mieux dans de telles conditions. Ce comportement de surcharge aura un impact significatif sur les performances de rendu. Notez que la notion de frame actuel est liée à [**EndScene**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene), de sorte que toute application qui utilise des ressources managées doit effectuer des appels réguliers à cette méthode.

Les développeurs qui cherchent à trouver plus d’informations sur la façon dont les ressources managées se comportent dans leur application peuvent utiliser la requête d’événement RESOURCEMANAGER par le biais de l’interface [**IDirect3DQuery9**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) . Cela ne fonctionne que lorsque vous utilisez les runtimes de débogage. par conséquent, ces informations ne peuvent pas dépendre de l’application, mais elles fournissent des détails détaillés sur les ressources gérées par le Runtime.

Bien que la compréhension du fonctionnement du gestionnaire de ressources puisse vous aider lors du paramétrage et du débogage de vos applications, il est important de ne pas lier trop étroitement votre application aux détails d’implémentation du runtime ou des pilotes actuels. Les révisions du pilote ou les modifications apportées au matériel peuvent considérablement changer le comportement, et les futures versions de Direct3D auront une gestion des ressources considérablement améliorée et sophistiquée.

## <a name="driver-managed-resources"></a>Ressources Driver-Managed

Les pilotes Direct3D sont libres d’implémenter la fonctionnalité de texture gérée par le pilote, indiquée par D3DCAPS2 \_ CANMANAGERESOURCE, qui permet au pilote de gérer la gestion des ressources au lieu du Runtime. Pour le pilote (rare) qui implémente cette fonctionnalité, le comportement exact du gestionnaire de ressources du pilote peut varier considérablement, et vous devez contacter le fournisseur du pilote pour plus d’informations sur la façon dont cela fonctionne pour son implémentation. Vous pouvez également vous assurer que le gestionnaire Runtime est toujours utilisé à la place en spécifiant D3DCREATE \_ désactiver \_ \_ la gestion des pilotes lors de la création de l’appareil.

## <a name="default-resources"></a>Ressources par défaut

Bien que les ressources managées soient simples, efficaces et faciles à utiliser, il peut arriver que l’utilisation directe de la mémoire vidéo soit préférable ou même requise. Ces ressources sont créées dans la \_ catégorie par défaut du pool. L’utilisation de ces ressources entraîne des complications supplémentaires pour votre application. Le code est nécessaire pour faire face à la situation de l’appareil perdu pour toutes les \_ ressources par défaut du pool, et les considérations relatives aux performances doivent être prises en compte lors de la copie des données dans ces derniers. Si vous ne spécifiez pas l’utilisation de \_ WRITEONLY ou si vous rendez une cible de rendu verrouillable, cela peut également entraîner des pénalités graves.

L’appel de **Lock** sur une ressource de pool \_ par défaut est plus susceptible de provoquer l’arrêt du GPU que l’utilisation d’une \_ ressource managée de pool, sauf en cas d’utilisation de certains indicateurs d’indicateur. Selon l’emplacement de la ressource, le pointeur retourné peut être un tampon de mémoire système temporaire ou un pointeur directement dans la mémoire AGP. S’il s’agit d’une mémoire tampon système temporaire, les données doivent être transférées vers la mémoire vidéo après l’appel de **déverrouillage** . Si la ressource vidéo n’est pas en écriture seule, les données doivent être transférées dans la mémoire tampon temporaire pendant le **verrouillage**. S’il s’agit d’une zone de mémoire AGP, les copies temporaires sont évitées, mais le comportement de cache requis peut entraîner un ralentissement des performances.

Vous devez veiller à écrire une ligne de données de cache complète dans n’importe quel pointeur vers la mémoire d’ouverture AGP afin d’éviter la pénalité de l’écriture dans le peigne, ce qui entraîne un cycle de lecture-écriture, et l’accès séquentiel de la zone de mémoire est préférable. Si votre application doit effectuer un accès aléatoire aux données lors de la création, et que vous ne souhaitez pas utiliser une ressource managée pour la mémoire tampon, vous devez utiliser une copie de mémoire système à la place. Une fois les données créées, vous pouvez diffuser le résultat dans la mémoire de ressource verrouillée pour éviter de payer une pénalité importante pour l’opération de combinaison d’écriture dans le cache.

L' \_ indicateur LOCK NOOVERWRITE peut être utilisé pour ajouter des données de manière efficace pour certaines ressources, mais idéalement, plusieurs appels de **verrouillage** et de **déverrouillage** à la même ressource peuvent être évités. L’utilisation correcte des différents indicateurs de verrou est importante pour des performances optimales, tout comme l’utilisation d’un modèle convivial du cache d’accès aux données lors du remplissage de la mémoire verrouillée.

### <a name="using-both-managed-and-default-resources"></a>Utilisation des ressources gérées et par défaut

Le mélange des allocations de ressources par défaut gérées et regroupées \_ peut provoquer une fragmentation de la mémoire vidéo et confondre la vue du runtime de la mémoire vidéo disponible pour les ressources managées. Dans l’idéal, vous devez créer toutes les \_ ressources par défaut du pool avant d’utiliser des \_ ressources gérées par le pool ou utiliser l’appel [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) avant d’allouer des ressources non managées. N’oubliez pas que toutes les allocations effectuées à partir de \_ la valeur par défaut du pool qui résident dans la mémoire vidéo mobilisent de la mémoire pour la durée pendant laquelle les ressources ne peuvent pas être utilisées par le gestionnaire de ressources ou à d’autres fins.

Notez qu’à la différence des versions antérieures de Direct3D, le runtime de la version 9 supprime automatiquement certaines ressources managées avant d’abandonner une allocation de ressources non managées en cas d’échec pour un manque de mémoire vidéo, mais cela peut potentiellement créer une fragmentation supplémentaire et même forcer une ressource dans un emplacement moins optimal (par exemple, en utilisant une texture statique dans la mémoire vidéo non locale). Là encore, il est préférable d’allouer toutes les ressources non managées avant et avant d’utiliser des ressources managées.

### <a name="dynamic-default-resources"></a>Ressources dynamiques par défaut

Les données générées et mises à jour à une fréquence élevée n’ont pas besoin du magasin de stockage, car toutes les informations seront recréées lors de la restauration de l’appareil. Ce type de données est généralement le mieux créé dans \_ le pool par défaut, en spécifiant l’indicateur d’utilisation \_ dynamique, afin que le pilote puisse prendre des décisions d’optimisation lors du placement de la ressource, sachant qu’il sera souvent mis à jour. Cela implique généralement de placer la ressource dans une mémoire vidéo non locale, et par conséquent, il est généralement beaucoup plus lent que le GPU accède à la mémoire vidéo locale. Pour les architectures UMA, le pilote peut choisir un emplacement particulier pour les ressources dynamiques à optimiser pour l’accès en écriture de l’UC.

Cette utilisation est courante pour les solutions de pelures de logiciels et les systèmes de particule basés sur le processeur qui remplissent des tampons de vertex/d’index, et l’indicateur de rejet de verrou \_ garantit que les blocages ne sont pas créés dans les cas où la ressource est toujours utilisée à partir de l’image précédente. Dans ce cas, l’utilisation d’une ressource managée met à jour une mémoire tampon système qui serait ensuite copiée dans la mémoire vidéo, puis utilisée uniquement pour un ou deux frames avant d’être remplacé. Pour les systèmes avec une mémoire vidéo non locale, la copie supplémentaire est éliminée en utilisant correctement ce modèle dynamique.

Les textures standard ne peuvent pas être verrouillées et ne peuvent être mises à jour qu’à l’aide de [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) ou [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture). Certains systèmes prennent en charge les textures dynamiques, qui peuvent être verrouillées et utilisent le modèle de rejet de verrou \_ , mais un bit des fonctionnalités (D3DCAPS2 \_ DYNAMICTEXTURES) doit être vérifié avant d’utiliser ces ressources. Pour les textures hautement dynamiques (vidéo ou procédurale), votre application peut créer des ressources de pool et de SYSTEMMEM de pool correspondantes \_ \_ et gérer les mises à jour de la mémoire vidéo à l’aide de **UpdateTexture**. Pour les mises à jour très fréquentes et partielles, le paradigme **UpdateTexture** est probablement le meilleur choix.

Aussi utile que les ressources dynamiques peuvent l’être, soyez prudent lors de la conception de systèmes qui s’appuient fortement sur l’envoi dynamique. Les ressources statiques doivent être placées dans un POOL \_ géré pour garantir une utilisation correcte de la mémoire vidéo locale et pour utiliser plus efficacement la bande passante de la mémoire centrale et de bus limité. Pour les ressources semi-statiques, vous constaterez peut-être que le coût d’un chargement occasionnel vers la mémoire vidéo locale est bien inférieur au trafic de bus constant généré en les rendant dynamiques.

## <a name="system-memory-resources"></a>Ressources mémoire système

Les ressources peuvent également être créées dans le POOL \_ SYSTEMMEM. Bien qu’ils ne puissent pas être utilisés par le pipeline Graphics, ils peuvent être utilisés comme sources pour la mise à jour des \_ ressources par défaut du pool à l’aide de [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) ou [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture). Leur comportement de verrouillage est simple, mais les blocages peuvent se produire s’ils sont utilisés par l’une des méthodes mentionnées précédemment.

Bien qu’ils résident dans la mémoire système, les \_ ressources SYSTEMMEM de pool sont limitées aux mêmes formats et capacités (par exemple, la taille maximale) pris en charge par le pilote de périphérique. Le \_ type de ressource Scratch du pool est une autre forme de ressource de mémoire système qui peut utiliser tous les formats et fonctionnalités pris en charge par le runtime, mais qui ne sont pas accessibles par l’appareil. Les ressources Scratch sont principalement destinées à être utilisées par les outils de contenu.

**Figure 3. Ressources mémoire dans la RAM vidéo, l’ouverture AGP et la RAM système**

![ressources mémoire dans la RAM vidéo, l’ouverture AGP et la RAM système](images/managingresources3.gif)

## <a name="general-recommendations"></a>Recommandations générales

L’obtention des détails de l’implémentation technique de la gestion des ressources va vous aider à atteindre vos objectifs en matière de performances pour votre application. La planification de la présentation des ressources à Direct3D et la conception architecturale pour l’obtention des données en temps opportun sont une tâche plus complexe. Nous vous recommandons d’utiliser un certain nombre de meilleures pratiques pour prendre ces décisions pour votre application :

-   Prétraitez toutes vos ressources. Le fait de s’appuyer sur une conversion et une optimisation des ressources au moment du chargement pour vos ressources est pratique pendant le développement, mais cela permet d’obtenir une charge considérable en matière de performances sur les ordinateurs des utilisateurs. Les ressources prétraitées sont plus rapides à charger, plus rapides à utiliser et vous donnent la possibilité d’effectuer des tâches hors ligne sophistiquées.
-   Évitez de créer de nombreuses ressources par frame. Les interactions de pilote requises peuvent sérialiser le processeur et le GPU, et les opérations impliquées sont lourdes, car elles nécessitent souvent des transitions de noyau. Répartissez la création sur plusieurs frames ou réutilisez les ressources sans les créer/les libérer. Idéalement, vous devez attendre plusieurs images avant de verrouiller ou de libérer des ressources récemment utilisées pour le rendu.
-   À la fin du cadre, veillez à dissocier tous les canaux de ressources (c’est-à-dire les sources de flux, les étapes de texture et les index actuels). Cela permet de s’assurer que les références non résolues aux ressources sont supprimées avant que Resource Manager ne conserve les ressources résidantes qui ne sont en fait plus utilisées.
-   Pour les textures, utilisez des formats compressés (par exemple, DXTn) avec MIP-Maps et envisagez d’utiliser un Atlas de textures. Ces dernières réduisent les besoins en bande passante et peuvent réduire la taille globale des ressources, ce qui les rend plus efficaces.
-   Pour Geometry, utilisez la géométrie indexée, car cela permet de compresser les ressources de mémoire tampon de vertex et le matériel vidéo moderne est fortement optimisé autour de la réutilisation des vertex. En utilisant des nuanceurs de vertex programmables, vous pouvez compresser les informations de vertex et les développer pendant le traitement du vertex. Là encore, cela permet de réduire les besoins en bande passante et rend les ressources de tampon de vertex plus efficaces.
-   Évitez l’optimisation de la gestion des ressources. Les révisions ultérieures des pilotes, du matériel et du système d’exploitation peuvent potentiellement entraîner des problèmes de compatibilité si l’application est réglée trop lourdement sur une combinaison particulière. Étant donné que la plupart des applications sont liées à l’UC, la gestion coûteuse basée sur le processeur entraîne généralement des problèmes de performances supplémentaires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des ressources](/windows/desktop/direct3d9/managing-resources)
</dt> <dt>

[Appareils perdus](/windows/desktop/direct3d9/lost-devices)
</dt> <dt>

[Optimisations des performances](/windows/desktop/direct3d9/performance-optimizations)
</dt> <dt>

[Ressources de texture compressées](/windows/desktop/direct3d9/compressed-texture-resources)
</dt> <dt>

[Requêtes](/windows/desktop/direct3d9/queries)
</dt> <dt>

[**D3DUSAGE**](/windows/desktop/direct3d9/d3dusage)
</dt> <dt>

[**D3DPOOL**](/windows/desktop/direct3d9/d3dpool)
</dt> <dt>

[D3DCREATE](/windows/desktop/direct3d9/d3dcreate)
</dt> </dl>

 

 