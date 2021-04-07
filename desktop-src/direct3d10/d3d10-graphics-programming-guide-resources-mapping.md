---
description: Copie et accès aux données de ressource (Direct3D 10)
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: Copie et accès aux données de ressource (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bd075585ee3123e163075a50b06b53a77a214c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748517"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>Copie et accès aux données de ressource (Direct3D 10)

Il n’est plus nécessaire de réfléchir aux ressources créées dans la mémoire vidéo ou la mémoire système. Ou si le runtime doit gérer la mémoire. Grâce à l’architecture du nouveau WDDM (Windows Display Driver Model), les applications créent désormais des ressources Direct3D 10 avec différents indicateurs d' [**utilisation**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) pour indiquer comment l’application envisage d’utiliser les données de ressource. Le nouveau modèle de pilote virtualise la mémoire utilisée par les ressources ; il devient alors le responsable du système d’exploitation/du pilote/de la mémoire de placer les ressources dans la zone de mémoire la plus performante possible en raison de l’utilisation prévue.

Le cas par défaut est que les ressources sont disponibles pour le GPU. Bien entendu, il y a des cas où les données de ressources doivent être disponibles pour le processeur. La copie de données de ressources pour que le processeur approprié puisse y accéder sans impact sur les performances nécessite une connaissance du fonctionnement des méthodes de l’API.

-   [Copie de données de ressource](#copying-and-accessing-resource-data-direct3d-10)
-   [Accès aux données de ressources](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>Copie de données de ressource

Les ressources sont créées en mémoire lorsque Direct3D exécute un appel de création. Ils peuvent être créés dans la mémoire vidéo, la mémoire système ou tout autre type de mémoire. Étant donné que le modèle de pilote WDDM virtualise cette mémoire, les applications n’ont plus besoin d’effectuer le suivi des types de ressources mémoire qui sont créés dans.

Idéalement, toutes les ressources seraient situées dans la mémoire vidéo afin que le GPU puisse y accéder immédiatement. Toutefois, il est parfois nécessaire que le processeur lise les données de ressources ou que le GPU accède aux données de ressources sur lesquelles le processeur a écrit. Direct3D 10 gère ces différents scénarios en demandant à l’application de spécifier une utilisation, puis propose plusieurs méthodes pour copier les données de ressource si nécessaire.

Selon la façon dont la ressource a été créée, il n’est pas toujours possible d’accéder directement aux données sous-jacentes. Cela peut signifier que les données de ressources doivent être copiées de la ressource source vers une autre ressource accessible par le processeur approprié. En termes de Direct3D 10, les ressources par défaut sont accessibles directement par le GPU, les ressources dynamiques et intermédiaires peuvent être directement accessibles par le processeur.

Une fois qu’une ressource a été créée, son [**utilisation**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) ne peut pas être modifiée. Au lieu de cela, copiez le contenu d’une ressource dans une autre ressource créée avec une utilisation différente. Direct3D 10 fournit cette fonctionnalité avec trois méthodes différentes. Les deux premières méthodes ( [**ID3D10Device :: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) et [**ID3D10Device :: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) sont conçues pour copier les données de ressources d’une ressource vers une autre. La troisième méthode ([**ID3D10Device :: UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) est conçue pour copier des données de la mémoire vers une ressource.

Il existe deux types de ressources principaux : mappables et non mappables. Les ressources créées avec des utilisations dynamiques ou intermédiaires sont mappées, alors que les ressources créées avec des utilisations par défaut ou immuables ne peuvent pas être mappées.

La copie de données entre des ressources non mappables est très rapide, car il s’agit du cas le plus courant et a été optimisé pour s’exécuter correctement. Étant donné que ces ressources ne sont pas directement accessibles par le processeur, elles sont optimisées afin que le GPU puisse les manipuler rapidement.

La copie de données entre des ressources mappables est plus problématique, car les performances dépendent de l’utilisation avec laquelle la ressource a été créée. Par exemple, le GPU peut lire une ressource dynamique assez rapidement, mais ne peut pas y écrire, et le GPU ne peut pas lire ou écrire directement dans les ressources intermédiaires.

Les applications qui souhaitent copier des données à partir d’une ressource avec une utilisation par défaut vers une ressource avec une utilisation intermédiaire (pour permettre au processeur de lire les données, c.-à-d. le problème de readback GPU) doivent le faire avec précaution. Pour plus d’informations sur ce dernier cas, consultez [accès aux données des ressources](#copying-and-accessing-resource-data-direct3d-10) .

## <a name="accessing-resource-data"></a>Accès aux données de ressources

L’accès à une ressource requiert le mappage de la ressource ; le mappage signifie essentiellement que l’application tente d’accorder l’accès de l’UC à la mémoire. Le processus de mappage d’une ressource afin que le processeur puisse accéder à la mémoire sous-jacente peut entraîner des goulots d’étranglement de performances et, pour cette raison, vous devez tenir compte de la façon et du moment d’exécution de cette tâche.

Les performances peuvent être interrompues si l’application tente de mapper une ressource à un moment incorrect. Si l’application tente d’accéder aux résultats d’une opération avant que cette opération ne soit terminée, un blocage de pipeline se produit.

L’exécution d’une opération de mappage à un moment incorrect peut entraîner une baisse importante des performances en forçant le GPU et le processeur à se synchroniser entre eux. Cette synchronisation aura lieu si l’application souhaite accéder à une ressource avant que le GPU n’ait fini de la copier dans une ressource que l’UC peut mapper.

L’UC ne peut lire que les ressources créées avec l' \_ indicateur intermédiaire d’utilisation de D3D10 \_ . Étant donné que les ressources créées avec cet indicateur ne peuvent pas être définies en tant que sorties du pipeline, si l’UC souhaite lire les données dans une ressource générée par le GPU, les données doivent être copiées dans une ressource créée avec l’indicateur de mise en lots. L’application peut effectuer cette opération à l’aide des méthodes [**ID3D10Device :: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) ou [**ID3D10Device :: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) pour copier le contenu d’une ressource vers une autre. L’application peut alors accéder à cette ressource en appelant la méthode Map appropriée. Lorsque l’accès à la ressource n’est plus nécessaire, l’application doit ensuite appeler la méthode unout correspondante. Par exemple, [**ID3D10Texture2D :: Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) et [**ID3D10Texture2D :: DEMAPPAGE**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap). Les différentes méthodes de mappage retournent des valeurs spécifiques en fonction des indicateurs d’entrée. Pour plus d’informations, consultez la [**section Remarques**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map) sur la carte.

> [!Note]  
> Lorsque l’application appelle la méthode Map, elle reçoit un pointeur vers les données de ressources auxquelles accéder. Le runtime garantit que le pointeur a un alignement spécifique, en fonction du [niveau](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)de la fonctionnalité. Pour [**le \_ niveau de fonctionnalité D3D \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) et supérieur, le pointeur est aligné à 16 octets. Pour le niveau de fonctionnalité inférieur à [**D3D \_ \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level), le pointeur est aligné sur 4 octets. L’alignement sur 16 octets permet à l’application d’effectuer des opérations optimisées [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))sur les données en mode natif, sans réalignement ni copie.

 

### <a name="performance-considerations"></a>Considérations relatives aux performances

Il est préférable de considérer un PC comme une machine s’exécutant comme une architecture parallèle avec deux principaux types de processeurs : un ou plusieurs PROCESSEURs et un ou plusieurs GPU. Comme pour n’importe quelle architecture parallèle, les meilleures performances sont obtenues lorsque chaque processeur est planifié avec suffisamment de tâches pour éviter qu’il ne devienne inactif et que le travail d’un processeur n’attende pas le travail d’un autre.

Le pire scénario pour le parallélisme GPU/UC est la nécessité de forcer un processeur à attendre les résultats du travail effectués par un autre. Direct3D 10 tente de supprimer ce coût en rendant les méthodes [**ID3D10Device :: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) et [**ID3D10Device :: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) asynchrones. la copie n’a pas nécessairement été exécutée au moment du retour de la méthode. L’avantage de cette méthode est que l’application ne paie pas le coût des performances de la copie des données jusqu’à ce que l’UC accède aux données, ce qui est le cas lorsque map est appelé. Si la méthode map est appelée après la copie des données, aucune perte de performances ne se produit. En revanche, si la méthode map est appelée avant que les données n’aient été copiées, un blocage de pipeline se produit.

Les appels asynchrones dans Direct3D 10 (qui constituent la grande majorité des méthodes, et en particulier les appels de rendu) sont stockés dans ce qu’on appelle une mémoire tampon de commande. Ce tampon est interne au pilote Graphics et est utilisé pour les appels par lots au matériel sous-jacent afin que le passage coûteux du mode utilisateur au mode noyau dans Microsoft Windows se produise le plus rarement possible.

La mémoire tampon de commande est vidée, provoquant ainsi un changement de mode utilisateur/noyau, dans l’une des quatre situations suivantes :

1.  [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) est appelé.
2.  [**ID3D10Device :: Flush**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush) est appelé.
3.  La mémoire tampon de commande est pleine ; sa taille est dynamique et est contrôlée par le système d’exploitation et le pilote Graphics.
4.  L’UC requiert l’accès aux résultats d’une commande en attente d’exécution dans la mémoire tampon de commande.

Parmi les quatre situations ci-dessus, le nombre quatre est le plus critique pour les performances. Si l’application émet un appel [**ID3D10Device :: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) ou [**ID3D10Device :: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) , cet appel est mis en file d’attente dans la mémoire tampon de commande. Si l’application essaie ensuite de mapper la ressource intermédiaire qui était la cible de l’appel de copie avant que le tampon de commande ait été vidé, un blocage de pipeline se produit, car non seulement l’appel de la méthode de copie doit être exécuté, mais toutes les autres commandes mises en mémoire tampon dans le tampon de commande doivent également s’exécuter. Cela entraînera la synchronisation du GPU et du processeur, car celui-ci attendra d’accéder à la ressource intermédiaire pendant que le GPU vide la mémoire tampon de commande et finalement à remplir la ressource dont le processeur a besoin. Une fois que le GPU a terminé la copie, l’UC commence à accéder à la ressource de mise en lots, mais pendant ce temps, le GPU est resté inactif.

Ce qui se passe fréquemment lors de l’exécution entraîne une dégradation importante des performances. Pour cette raison, le mappage des ressources créées avec l’utilisation par défaut doit être effectué avec précaution. L’application doit attendre suffisamment longtemps pour que le tampon de commande soit vidé et, par conséquent, toutes ces commandes finissent à s’exécuter avant de tenter de mapper la ressource intermédiaire correspondante. Quelle est la durée d’attente de l’application ? Au moins deux frames, car cela permet d’optimiser le parallélisme entre le processeur et le GPU. La façon dont le GPU fonctionne est que pendant que l’application traite le frame N en soumettant des appels au tampon de commande, le GPU est occupé à exécuter les appels à partir du frame précédent, N-1.

Par conséquent, si une application souhaite mapper une ressource qui provient de la mémoire vidéo et appelle [**ID3D10Device :: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) ou [**ID3D10Device :: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) au niveau de la trame n, cet appel commence en fait à s’exécuter au frame n + 1, lorsque l’application envoie des appels pour le frame suivant. La copie doit être terminée lorsque l’application traite le frame N + 2.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Frame</th>
<th>État GPU/UC</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>N</td>
<td><ul>
<li>Les problèmes d’UC affichent les appels pour le frame actuel.</li>
</ul></td>
</tr>
<tr class="even">
<td>N + 1</td>
<td><ul>
<li>Le GPU exécute les appels envoyés depuis l’UC pendant le frame N.</li>
<li>Les problèmes d’UC affichent les appels pour le frame actuel.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N + 2</td>
<td><ul>
<li>Le GPU a terminé l’exécution des appels envoyés depuis le processeur au cours de la trame N. les résultats sont prêts.</li>
<li>Le GPU exécute les appels envoyés depuis le processeur pendant la trame N + 1.</li>
<li>Les problèmes d’UC affichent les appels pour le frame actuel.</li>
</ul></td>
</tr>
<tr class="even">
<td>N + 3</td>
<td><ul>
<li>Le GPU a terminé l’exécution des appels envoyés depuis le processeur pendant la trame N + 1. Résultats prêts.</li>
<li>Le GPU exécute les appels envoyés depuis l’UC au cours de la trame N + 2.</li>
<li>Les problèmes d’UC affichent les appels pour le frame actuel.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N + 4</td>
<td>...</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
