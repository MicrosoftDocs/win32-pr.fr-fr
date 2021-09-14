---
title: Glossaire Direct3D 12
description: Ces termes sont distincts de Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293582"
---
# <a name="direct3d-12-glossary"></a>Glossaire Direct3D 12

Ces termes sont distincts de Direct3D 12.

<dl> <dt>

<span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**liant**
</dt> <dd>

Processus d’attachement de la mémoire au pipeline Graphics. La liaison de ressources, par exemple, implique la liaison d’une ressource, telle qu’une texture au pipeline, pour une utilisation lors du rendu d’un objet.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**mémoire tampon**
</dt> <dd>

Type de ressource D3D synonyme d’une allocation de mémoire contiguë.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**lots**
</dt> <dd>

Mémoire tampon de commande que l’unité de traitement graphique (GPU) peut exécuter uniquement directement par le biais d’une *liste de commandes directe*. Un bundle hérite de tous les États GPU (à l’exception de l' *objet d’état de pipeline* actuellement défini et de la topologie primitive).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**allocateur de commande**
</dt> <dd>

Allocations de mémoire sous-jacentes dans lesquelles sont stockées les commandes GPU. L’objet d’allocation de commande s’applique à la fois à des *listes de commandes directes* et à des *offres groupées*.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**Liste des commandes**
</dt> <dd>

Une liste de commandes correspond à un ensemble de commandes que le GPU exécute. Celles-ci incluent des commandes telles que la définition d’État, de dessin, d’effacement et de copie. L’interface de la liste de commandes D3D12 est très différente de l’interface de la liste de commandes D3D11. L’interface de la liste de commandes D3D12 contient des API similaires aux API de rendu de contexte de périphérique D3D11.

Une liste de commandes D3D12 ne mappe pas les ressources et ne les annule pas, ne modifie pas les mappages de vignettes, ne redimensionne pas les pools de mosaïques, ne récupère pas les données de requête et n’envoie jamais des commandes au GPU en vue de leur exécution.

Contrairement aux contextes différés de D3D11, les listes de commandes D3D12 prennent uniquement en charge deux niveaux d’indirection. Une *liste de commandes directe* correspond à une mémoire tampon de commande que le GPU peut exécuter. Une *offre groupée* ne peut être exécutée que directement via une liste de commandes directe.

Une liste de commandes directe n’hérite d’aucun État GPU. Un bundle hérite de tous les États GPU (à l’exception de l’objet d’état de pipeline actuellement défini et de la topologie primitive).

La mémoire pour une liste de commandes est définie par l' *allocateur de commande*. L’objectif des listes de commandes est qu’elles peuvent être envoyées à un GPU sous la forme d’une demande de rendu unique.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**file d’attente de commandes**
</dt> <dd>

Une file d’attente de *commandes répertorie* les exécutions successives du GPU. Les applications doivent envoyer explicitement des *listes de commandes* à une file d’attente de commandes pour exécution. En général, il existe trois files d’attente de commandes : les graphiques 3D, Compute et Copy, qui correspondent au pipeline graphique 3D, au moteur de calcul et à un ou plusieurs moteurs de copie sur le GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**pixellisation conservatrice**
</dt> <dd>

La pixellisation conservatrice est un mode de fonctionnement pour l’étape de rastérisation du pipeline graphique Direct3D. Il désactive la pixellisation standard basée sur les échantillons et pixellise à la place un pixel qui est couvert par n’importe quelle quantité par une primitive. Une distinction importante est que, alors que toute couverture produit un pixel pixellisé, cette couverture ne peut pas être caractérisée par le matériel. par conséquent, la couverture apparaît toujours en binaire dans un nuanceur de pixels : entièrement couvertes ou non couvertes. Il est laissé au code du nuanceur de pixels pour déterminer de façon analytique la couverture réelle.

La pixellisation conservatrice peut être utile avec des problèmes tels que la détection des collisions et des collisions, compartimentage et l’élimination des occlusions, où la couleur d’un pixel est plus certaine et les cas limites peuvent être éliminés. Consultez [pixellisation conservatrice](conservative-rasterization.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Vue de la mémoire tampon constante (CBV)**
</dt> <dd>

Les mémoires tampons constantes contiennent des données constantes de nuanceur, telles qu’une vue caméra, des matrices de projection et des matrices universelles. Une « vue de mémoire tampon constante » est la vue spécifique au format de la mémoire tampon telle qu’elle est affichée par le pipeline Graphics.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**tas par défaut**
</dt> <dd>

Segment de mémoire en mode utilisateur qui se concentre sur la prise en charge des types de ressources GPU persistants, y compris les ressources écrites par GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**Description**
</dt> <dd>

Les descripteurs sont l’unité principale de liaison pour une seule ressource dans D3D12. Un descripteur est un bloc de données relativement petit, qui décrit entièrement un objet au GPU, dans un format spécifique au GPU. Il existe de nombreux types différents de descripteurs : les vues des ressources de nuanceur (SRVs), les vues d’accès non ordonnées (UAVs), les vues de mémoire tampon constante (CBVs) et les échantillonneurs sont quelques exemples.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**tas du descripteur**
</dt> <dd>

Un tas de descripteur est une collection d’allocations contiguës de descripteurs, une allocation pour chaque descripteur. Le point principal d’un tas de descripteur doit englober l’essentiel de l’allocation de mémoire nécessaire pour stocker les spécifications de descripteur des types d’objets que les nuanceurs référencent dans le cadre d’une fenêtre de rendu aussi grande que possible (idéalement une image entière de rendu ou plus).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tableau du descripteur**
</dt> <dd>

Une table de descripteur est logiquement un tableau de descripteurs. Chaque table de descripteur stocke des descripteurs d’un ou plusieurs types, notamment SRVs, UAVe, CBVs et échantillonneurs. Une table de descripteurs n’est pas une allocation de mémoire, il s’agit simplement d’un décalage et d’une longueur dans un tas de descripteur.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**liste de commandes directe**
</dt> <dd>

Mémoire tampon de commande que le GPU peut exécuter. Une liste de commandes directe n’hérite d’aucun État GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**peindre**
</dt> <dd>

Mécanisme de synchronisation du GPU et de l’UC. Le GPU et le processeur peuvent être demandés à attendre une clôture, en attendant que l’autre processeur rattrape son retard. Consultez [synchronisation multimoteur](./user-mode-heap-synchronization.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**risque, suivi des risques**
</dt> <dd>

Un risque se produit lorsqu’une ressource a été utilisée à un usage unique et que l’application a l’intention de la réutiliser à d’autres fins. Pour réutiliser la ressource, les caches intermédiaires doivent être vidés ou invalidés, les exigences de compression doivent être cohérentes avec la deuxième utilisation, et la ressource doit être dans l’État requis pour éviter de lire la ressource une fois qu’elle a été écrite et invalidée dans le but prévu.

Le processus de gestion des ressources et d’évitement de ces problèmes de synchronisation est appelé suivi des risques. S’il n’y a aucun suivi de risque par le pilote, l’application est responsable de cette tâche. Dans la plupart des versions antérieures de DirectX, le suivi des dangers était géré par le pilote. Pour améliorer les performances, les méthodes sans suivi des risques sont disponibles dans DirectX 12.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**HLSL (High-Level Shader Language)**
</dt> <dd>

Un langage informatique, similaire mais distinct de nombreuses façons à partir de C, utilisé pour écrire le code du nuanceur. Les nuanceurs vertex, pixel, Geometry, Compute, Domain et coque sont tous écrits en HLSL. Un compilateur convertit la source HLSL en un format binaire que le GPU doit consommer.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multimoteur**
</dt> <dd>

Les différentes instances et types de moteurs dans une seule unité GPU. Les types de moteurs sont les suivants : Graphics, Compute et Copy.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**
</dt> <dd>

Une configuration matérielle où il existe plusieurs cartes graphiques. Les adaptateurs distincts sont parfois appelés des nœuds. Avoir plusieurs GPU peut faire en sorte que la tâche de les synchroniser avec l’UC, et l’autre, est considérablement plus complexe qu’avec une seule GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Objet d’État du pipeline (PSO)**
</dt> <dd>

Partie significative de l’état du GPU. Cet État comprend tous les nuanceurs actuellement définis et certains objets d’état de fonction fixe. La seule façon de modifier les États contenus dans l’objet de pipeline est de modifier l’objet de pipeline actuellement lié.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**prédication**
</dt> <dd>

Un prédicat est une fonctionnalité qui permet au GPU plutôt qu’au processeur de déterminer de ne pas dessiner, copier ou distribuer un objet. Par exemple, si un cadre englobant d’un objet est entièrement bloqués par un autre objet ou si la perspective a réduit l’objet à une valeur inférieure à la taille d’un pixel, il est possible qu’il n’y ait aucun point de tentative de dessin de l’objet masqué. Consultez [predicate](predication.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Vue de l’ordre du rastériseur (ROV)**
</dt> <dd>

Les pipelines graphiques standard peuvent avoir des difficultés à converser correctement ensemble plusieurs textures qui contiennent de la transparence. Les objets tels que les clôtures de câble, les fumées, les incendies, les végétations et les verres de couleur utilisent la transparence pour atteindre l’effet souhaité. Des problèmes surviennent lorsque plusieurs textures contenant de la transparence sont alignées les unes avec les autres (fumée devant une clôture devant une couche de verre contenant de la végétation, par exemple). Les vues triées du rastériseur (ROVs) permettent aux algorithmes de transparence des commandes (OIT) sous-jacents d’utiliser les fonctionnalités du matériel pour tenter de résoudre correctement l’ordre de transparence. La transparence est gérée par le nuanceur de pixels.

Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons de vue d’accès non triée (UAV) avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de pipeline graphique pour UAVs.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**tas readback**
</dt> <dd>

Segment de mémoire en mode utilisateur qui se concentre sur le transfert de données du GPU vers le processeur.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**ressource**
</dt> <dd>

Entité qui fournit des données au pipeline et définit ce qui est rendu au cours de votre scène. Les ressources peuvent être chargées à partir de votre support de jeu ou créées dynamiquement au moment de l’exécution. En règle générale, les ressources incluent des données de texture, des données de vertex et des données de nuanceur. La plupart des applications Direct3D créent et détruisent largement les ressources tout au long de leur durée de vie.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barrière des ressources**
</dt> <dd>

Une barrière de ressources informe le pilote que la synchronisation de plusieurs accès à une ressource unique peut être nécessaire, par exemple, la lecture et l’écriture dans la même texture.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**liaison de ressource**
</dt> <dd>

La liaison de ressources est le processus qui consiste à lier des ressources (textures, mémoires tampons de vertex, tampons d’index, etc.) au pipeline Graphics, ce qui permet aux nuanceurs du pipeline de traiter la ressource correcte.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**tas de ressources**
</dt> <dd>

Les tas de ressources sont un terme générique pour les segments de mémoire tampon qui sont mis de côté pour contenir des ressources lors de leur transfert vers et depuis le GPU. un transfert vers le gpu requiert un segment de mémoire Télécharger, du gpu au processeur requiert un segment de mémoire Readback, et un segment de mémoire persistant pour le gpu à gérer sur plusieurs frames de rendu est appelé un tas par défaut.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**signature racine**
</dt> <dd>

Les signatures racines définissent toutes les ressources qui doivent être liées aux pipelines graphiques, ou de calcul. Une signature racine est configurée par les listes de commandes App et Links aux ressources dont les nuanceurs ont besoin en général, il existe un graphique et une signature racine de calcul par application.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**échantillonneur**
</dt> <dd>

Un échantillonneur est du code qui lit à partir d’une texture.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Affichage des ressources du nuanceur (SRV)**
</dt> <dd>

Moyen spécifique au format d’examiner les données dans une ressource de nuanceur, telle qu’une texture.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**tas statique**
</dt> <dd>

Segment de mémoire en mode utilisateur qui se concentre sur plusieurs ressources de lecture seule GPU qui sont généralement utilisées en même temps et qui ne sont pas souvent modifiées.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**chaîne de permutation**
</dt> <dd>

Les chaînes d’échange contrôlent la rotation de la mémoire tampon d’arrière-plan, formant ainsi la base de l’animation graphique. Les chaînes d’échange sont gérées par l’API Set de bas niveau DXGI (consultez [vue d’ensemble d’dxgi](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**
</dt> <dd>

Technique de recherche de données multidimensionnelles en mémoire, de sorte que les données de la dimensionnalité proche ont tendance à avoir des adresses à proximité. En particulier, toutes les données d’une ligne ne se trouvent pas à l’emplacement contigu avant les données de la ligne suivante. Une « Swizzle paramétrable » décrit une méthode standardisée pour décrire des modèles de Swizzle.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**motif**
</dt> <dd>

Type de ressource D3D à plusieurs dimensions et dont la disposition mémoire est optimisée pour l’accès multidimensionnel à partir du GPU. Les textures contiennent souvent l’image brute requise pour le rendu sur une surface, avant l’éclairage et la fusion, mais peut contenir d’autres formes de données telles que des dégradés de couleur et des couleurs de référence. Direct3D 12 prend en charge une, deux et trois textures unidimensionnelles.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**disposé**
</dt> <dd>

Page de la mémoire vidéo, similaire à une page UC/système de mémoire. La notation de vignette permet de distinguer le sous-système de mémoire virtuelle du GPU du sous-système de mémoire virtuelle de l’UC. Les GPU offrent des fonctionnalités de mémoire virtuelle similaires à celles de la mémoire virtuelle du système. Certains GPU ont des fonctionnalités de mémoire virtuelle partagées, qui permettent le partage de certaines pages du sous-système de mémoire virtuelle avec l’UC et le GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**ressources en mosaïque**
</dt> <dd>

Les ressources en mosaïque sont nécessaires, si bien que la mémoire GPU est gaspillée, le stockage des régions de surfaces que l’application connaît n’est pas accessible et le matériel peut comprendre comment filtrer les vignettes adjacentes. Les ressources en mosaïque sont des ressources logiques volumineuses, mais elles nécessitent de petites quantités de mémoire physique.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Vue d’accès non triée (UAV)**
</dt> <dd>

Une vue d’accès non ordonnée dans une ressource (qui comprend des mémoires tampons, des textures et des tableaux de textures sans échantillonnage multiple) autorise un accès en lecture/écriture non ordonné de manière temporelle à partir de plusieurs threads. Cela signifie que ce type de ressource peut être lu/écrit simultanément par plusieurs threads sans générer de conflits de mémoire.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**charger le tas**
</dt> <dd>

Segment de mémoire en mode utilisateur qui se concentre sur le transfert de données du processeur vers le GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**segment de mémoire en mode utilisateur**
</dt> <dd>

Collection d’allocations de mémoire volumineuses et contiguës qui sont recyclées sans conscience du composant de noyau : les méthodes d’allocation et de destruction n’appellent pas les méthodes d’allocation et de destruction du noyau dans un état stable. les tas Télécharger, Readback et Default sont des variantes de tas en mode utilisateur.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**ressources en mosaïque de volume**
</dt> <dd>

[Ressources en mosaïque](/windows)en trois dimensions.

</dd> </dl>

 

 