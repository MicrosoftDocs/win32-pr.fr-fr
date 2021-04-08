---
title: Points de synchronisation
description: Lorsque les jeux de propriétés sont pris en charge sur le même objet que IStorage, il est important de connaître les points de synchronisation entre le stockage de base et le stockage des propriétés.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675910"
---
# <a name="synchronization-points"></a><span data-ttu-id="5d3c9-103">Points de synchronisation</span><span class="sxs-lookup"><span data-stu-id="5d3c9-103">Synchronization Points</span></span>

<span data-ttu-id="5d3c9-104">Lorsque les jeux de propriétés sont pris en charge sur le même objet que [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), il est important de connaître les points de synchronisation entre le stockage de base et le stockage des propriétés.</span><span class="sxs-lookup"><span data-stu-id="5d3c9-104">When property sets are supported on the same object as [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), it is important to be aware of synchronization points between the base storage and the property storage.</span></span>

<span data-ttu-id="5d3c9-105">Le stockage de jeux de propriétés contient le flux de jeu de propriétés dans une mémoire tampon interne jusqu’à ce que cette mémoire tampon soit validée par le biais de la méthode [**IPropertyStorage :: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) .</span><span class="sxs-lookup"><span data-stu-id="5d3c9-105">The property set storage holds the property set stream in an internal buffer until that buffer is committed through the [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) method.</span></span> <span data-ttu-id="5d3c9-106">Cela est vrai si [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) a été ouvert en mode traité ou en mode direct.</span><span class="sxs-lookup"><span data-stu-id="5d3c9-106">This is true whether [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) was opened in transacted mode or in direct mode.</span></span>

 

 




