---
title: Monikers
description: Un moniker dans COM n’est pas seulement un moyen d’identifier un objet \ 8212 ; un moniker est également implémenté comme un objet.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126924639"
---
# <a name="monikers"></a>Monikers

Un moniker dans COM n’est pas seulement un moyen d’identifier un objet : un moniker est également implémenté comme un objet. Cet objet fournit des services qui permettent à un composant d’obtenir un pointeur vers l’objet identifié par le moniker. Ce processus est appelé *liaison*.

Les monikers sont des objets qui implémentent l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) et sont généralement implémentés dans des dll en tant qu’objets de composant. Il existe deux façons d’afficher l’utilisation des monikers : en tant que client moniker, composant qui utilise un moniker pour obtenir un pointeur vers un autre objet ; et en tant que fournisseur de monikers, un composant qui fournit des monikers identifiant ses objets aux clients monikers.

OLE utilise des monikers pour se connecter aux objets et les activer, qu’ils se trouvent sur le même ordinateur ou sur un réseau. Une utilisation très importante concerne les connexions réseau. Elles servent également à identifier, à se connecter à et à exécuter des objets de lien de document composé OLE. Dans ce cas, la source de lien joue le rôle de fournisseur de moniker et le conteneur qui contient l’objet Link agit en tant que client moniker.

Pour plus d'informations, voir les rubriques suivantes :

-   [Clients moniker](moniker-clients.md)
-   [Fournisseurs de moniker](moniker-providers.md)
-   [Implémentations du moniker OLE](ole-moniker-implementations.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[COM (Component Object Model)](the-component-object-model.md)
</dt> </dl>

 

 




