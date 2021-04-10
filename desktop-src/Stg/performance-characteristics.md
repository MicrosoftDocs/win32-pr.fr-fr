---
title: Caractéristiques de performances
description: Un appel à l’implémentation de fichier composé COM de l’interface IPropertySetStorage pour créer un jeu de propriétés entraîne la création d’un flux ou d’un stockage via un appel à IStorage CreateStream, ou IStorage CreateStorage.
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8597862602a367ed93a3d6e5e0bcac76035c337a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941141"
---
# <a name="performance-characteristics"></a>Caractéristiques de performances

Un appel à l’implémentation de fichier composé COM de l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) pour créer un jeu de propriétés entraîne la création d’un flux ou d’un stockage via un appel à [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) ou [**IStorage :: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage). Un jeu de propriétés par défaut est créé en mémoire, mais il n’est pas vidé sur le disque. Lorsqu’il y a un appel à [**IPropertyStorage :: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple), il s’exécute dans la mémoire tampon.

Quand un jeu de propriétés est ouvert, [IStorage :: OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ou [IStorage :: OpenStorage](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) est utilisé. L’ensemble du flux de propriétés est lu dans la mémoire contiguë. Les opérations [**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) fonctionnent alors en lisant la mémoire tampon. Par conséquent, le premier accès est coûteux en termes de temps (en raison des lectures sur le disque), mais les accès ultérieurs sont très efficaces. Les écritures peuvent être légèrement plus coûteuses, car les opérations de configuration sur le flux sous-jacent peuvent être nécessaires pour garantir que l’espace disque est disponible si des données sont ajoutées.

Aucune garantie n’est faite pour si [**IPropertyStorage :: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) vide les mises à jour. En général, le client doit supposer que **IPropertyStorage :: WriteMultiple** met à jour uniquement le en mémoire tampon. Pour vider des données, [**IPropertyStorage :: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) ou [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (dernière version) doit être appelé.

Cette conception signifie que [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) peut aboutir, mais que les données ne sont pas réellement écrites de façon permanente.

> [!Note]  
> Cette taille du flux de jeu de propriétés ne peut pas dépasser 256 Ko.

 

 

 