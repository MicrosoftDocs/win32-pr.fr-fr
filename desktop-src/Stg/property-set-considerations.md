---
title: Considérations relatives aux jeux de propriétés
description: Il est fortement recommandé que les jeux de propriétés soient réduits, car le flux de jeu de propriétés est lu en mémoire avant qu’une seule propriété puisse être lue ou écrite.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Considérations relatives aux jeux de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675906"
---
# <a name="property-set-considerations"></a><span data-ttu-id="5eb9d-104">Considérations relatives aux jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="5eb9d-104">Property Set Considerations</span></span>

<span data-ttu-id="5eb9d-105">Il est fortement recommandé que les jeux de propriétés soient réduits, car le flux de jeu de propriétés est lu en mémoire avant qu’une seule propriété puisse être lue ou écrite.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-105">It is strongly recommended that property sets be kept small because the property set stream is read into memory before a single property can be read or written.</span></span> <span data-ttu-id="5eb9d-106">« Small » signifie moins de 32 kilo-octets de données.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-106">"small" means less than 32 kilobytes of data.</span></span> <span data-ttu-id="5eb9d-107">Cela présente rarement un problème, car en général, les propriétés « en ligne » sont des éléments de petite taille, tels que des chaînes descriptives, des mots clés, des horodatages, des nombres, des noms d’auteur, des identificateurs globaux uniques (GUID), des identificateurs de classe (CLSID), etc.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-107">This rarely presents a problem because typically, "in-line" properties will be small items such as descriptive strings, keywords, time stamps, counts, author names, globally unique identifiers (GUIDs), class identifiers (CLSIDs), and so forth.</span></span>

<span data-ttu-id="5eb9d-108">Pour stocker des segments de données plus volumineux, ou dans les cas où la taille totale d’un ensemble de propriétés associées dépasse bien la quantité recommandée, l’utilisation de types non simples, tels que **VT \_ Stream** et **VT \_ Storage** , est fortement recommandée.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-108">To store larger chunks of data, or in cases where the total size of a set of related properties far exceeds the recommended amount, the use of nonsimple types such as **VT\_STREAM** and **VT\_STORAGE** are strongly recommended.</span></span> <span data-ttu-id="5eb9d-109">Celles-ci ne sont pas stockées dans le flux de jeu de propriétés, de sorte qu’elles n’affectent pas de manière significative la surcharge initiale de la première opération d’accès et d’écriture d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-109">These are not stored within the property set stream, so they do not significantly affect the initial overhead of the first accessing and writing of a property.</span></span> <span data-ttu-id="5eb9d-110">Il y a une surcharge minimale, car le flux de jeu de propriétés contient le nom de la propriété de flux ou de valeur de stockage frères, ce qui réduit le temps de traitement.</span><span class="sxs-lookup"><span data-stu-id="5eb9d-110">There is a minimal overhead as the property set stream contains the name of the sibling stream- or storage-valued property and this takes an additional small amount of time to process.</span></span>

<span data-ttu-id="5eb9d-111">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="5eb9d-111">For more information, see:</span></span>

-   [<span data-ttu-id="5eb9d-112">Considérations relatives à l’implémentation de IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="5eb9d-112">IPropertySetStorage Implementation Considerations</span></span>](ipropertysetstorage-implementation-considerations.md)
-   [<span data-ttu-id="5eb9d-113">Stockage des jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="5eb9d-113">Storing Property Sets</span></span>](storing-property-sets.md)
-   [<span data-ttu-id="5eb9d-114">Caractéristiques de performances</span><span class="sxs-lookup"><span data-stu-id="5eb9d-114">Performance Characteristics</span></span>](performance-characteristics.md)
-   [<span data-ttu-id="5eb9d-115">Implémentation du jeu de propriétés d’informations de résumé</span><span class="sxs-lookup"><span data-stu-id="5eb9d-115">Implementing the Summary Information Property Set</span></span>](implementing-the-summary-information-property-set.md)

 

 




