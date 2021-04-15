---
description: Recherche de partitions pendant l’activation
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Recherche de partitions pendant l’activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104562136"
---
# <a name="locating-partitions-during-activation"></a>Recherche de partitions pendant l’activation

La localisation de la partition correcte dans laquelle activer un composant dépend des éléments suivants :

-   L’appel de fonction et les paramètres utilisés dans le programme appelant pour activer le composant
-   Indique si le composant en cours d’activation est local ou distant
-   Utilisation interne du cache de partition

## <a name="the-calling-program"></a>Programme appelant

COM+ sélectionne la partition pour l’activation des composants en fonction de la façon dont le programme appelant active le composant.

COM+ peut effectuer trois actions différentes lors de la sélection d’une partition pour l’activation d’un composant. L’action entreprise dépend de la manière dont le programme appelant instancie l’objet qui est, que l’appel de fonction inclue un moniker de partition, qui se compose d’un ID de partition et d’un CLSID, ou qui inclut un CLSID uniquement.

Le tableau suivant répertorie les différentes actions que COM+ peut effectuer, par ordre de priorité, pour localiser une partition.



| Appel de fonction                                                  | Paramètre                                                      | Action COM+                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) ou **GetObject**<br/> | Moniker de partition (comprend l’ID de partition et le CLSID)<br/> | Utilise l’ID de partition spécifié dans le moniker de la partition.<br/>                                                                                                                           |
| [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | CLSID<br/>                                               | Utilise l’ID de partition de la partition par défaut de l’identité de l’utilisateur ou l’ID de partition qui a été ajouté au contexte au cours d’une activation de composant précédente dans le même processus.<br/> |



 

Les actions COM+ répertoriées dans le tableau précédent sont expliquées dans les sections suivantes.

## <a name="use-of-partition-monikers"></a>Utilisation des monikers de partition

Une partition peut être sélectionnée explicitement dans un appel de fonction à l’aide d’un *moniker de partition*. Un moniker de partition est utilisé dans le code pour spécifier explicitement la partition du composant activé. Si un moniker de partition est utilisé pour localiser la partition, l’activation se produit à partir de cette partition. Autrement dit, l’ID de partition inclus dans le moniker est prioritaire sur la partition par défaut de l’utilisateur ou sur un ID de partition qui existe dans le contexte de l’appelant.

Dans le code C++, la syntaxe d’utilisation d’un moniker de partition est la suivante :


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



L’exemple suivant montre un extrait de code C++, dans lequel un moniker de partition est utilisé en tant qu’argument de la fonction [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) :


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



Dans Visual Basic Code, la syntaxe d’un moniker de partition est la suivante :


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



L’exemple suivant montre un extrait de code Visual Basic, dans lequel un moniker de partition est utilisé en tant qu’argument de la fonction **GetObject** :


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a>Utilisation du mappage par défaut

Lorsque la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) est utilisée pour activer un composant à l’aide du CLSID du composant, com+ utilise le mappage d’identité d’utilisateur par défaut, c’est-à-dire le jeu de partitions auquel l’utilisateur est mappé dans Active Directory. Toutefois, si l’utilisateur n’est pas mappé à un ensemble de partitions dans Active Directory, la partition globale est sélectionnée.

## <a name="use-of-partition-ids-and-object-context"></a>Utilisation des ID de partition et du contexte de l’objet

L’une des cinq propriétés assignées à une nouvelle partition est l’ID de partition. Lorsque le programme client appelle la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour instancier un objet, l’ID de partition est ajouté au contexte. L’utilisation de l’ID de partition du contexte pour localiser la partition est importante, car elle garantit qu’une fois qu’une chaîne d’activations a commencé, l’ID de partition reste le même, sauf si elle est modifiée explicitement via un moniker de partition.

Pour plus d’informations sur la localisation des partitions lors de l’activation, consultez [composants et partitions en file d’attente com+](com--queued-components-and-partitions.md).

## <a name="local-and-remote-activation"></a>Activation locale et à distance

-   Si le composant appelé existe sur un autre ordinateur, les propriétés de partition (y compris l’ID de partition) sont marshalées vers l’autre ordinateur et le composant est activé à partir de la partition marshalée. Si aucun ID de partition n’a été marshalé, COM+ utilise l’ensemble de partitions par défaut mappé à l’identité de l’utilisateur dans Active Directory.

## <a name="the-partition-cache"></a>Cache de partition

Dans un environnement de domaine, COM+ utilise les mappages dans Active Directory pour localiser la partition correcte pour l’activation des composants. Toutefois, les recherches fréquentes dans Active Directory peuvent entraîner un trafic réseau excessif. Pour réduire le trafic réseau résultant des recherches fréquentes de mappages d’utilisateur à partition dans Active Directory, COM+ utilise un *cache de partition*.

Le cache de partition contient les mappages effectués dans Active Directory entre les identités des utilisateurs ou les unités d’organisation et leurs jeux de partitions. Ce cache de partition se trouve sur le serveur d’applications sur lequel résident les applications COM+.

Lorsque COM+ doit déterminer la partition par défaut d’un utilisateur ou valider les droits d’accès d’un utilisateur à une partition, il vérifie localement le cache de partition pour rechercher le mappage de l’utilisateur, au lieu de vérifier Active Directory à distance.

Si la recherche dans le cache de partition échoue, COM+ vérifie Active Directory. Si la recherche est réussie dans Active Directory, COM+ stocke ce mappage dans le cache de partition. La prochaine fois qu’une recherche est effectuée pour ce mappage d’utilisateur à partition, COM+ la trouvera dans le cache de partition.

L’illustration suivante montre le processus utilisé par COM+ pour localiser une partition pour l’activation d’un composant.

![Diagramme illustrant une arborescence de résolution des problèmes pour le processus utilisé par COM+ pour localiser une partition pour l’activation des composants.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

La taille du cache et l’heure d’expiration des entrées du cache sont définies via des clés de registre. Pour plus d’informations sur la configuration de ces clés de Registre, consultez [création et configuration de partitions com+](creating-and-configuring-com--partitions.md).

> [!Note]  
> Si un ordinateur serveur est déconnecté du réseau et que le mappage utilisateur à partition est modifié alors que le serveur est déconnecté, le cache de partition peut contenir un mappage utilisateur à partition obsolète. Cela peut entraîner une erreur d’activation si le mappage utilisateur-partition est le mécanisme utilisé pour activer un composant.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche d’un composant pour l’activation](locating-a-component-for-activation.md)
</dt> </dl>

 

