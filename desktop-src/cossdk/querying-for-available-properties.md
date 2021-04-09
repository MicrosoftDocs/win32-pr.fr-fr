---
description: Interrogation des propriétés disponibles
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Interrogation des propriétés disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111286"
---
# <a name="querying-for-available-properties"></a><span data-ttu-id="a6216-103">Interrogation des propriétés disponibles</span><span class="sxs-lookup"><span data-stu-id="a6216-103">Querying for Available Properties</span></span>

<span data-ttu-id="a6216-104">Si vous écrivez un outil d’administration à usage général, vous devrez probablement écrire des routines pour définir des propriétés en général.</span><span class="sxs-lookup"><span data-stu-id="a6216-104">If you are writing a general-purpose administration tool, you most likely will need to write routines for setting properties in full generality.</span></span> <span data-ttu-id="a6216-105">Pour prendre cela en charge, il existe une fonctionnalité qui vous permet de Rechercher dynamiquement les propriétés disponibles pour les éléments d’une collection donnée.</span><span class="sxs-lookup"><span data-stu-id="a6216-105">To support this, there is a facility that enables you to dynamically query for the properties that are available for the items in any given collection.</span></span>

<span data-ttu-id="a6216-106">La collection [**PropertyInfo**](propertyinfo.md) est disponible à partir de n’importe quel regroupement que vous êtes susceptible de contenir.</span><span class="sxs-lookup"><span data-stu-id="a6216-106">The [**PropertyInfo**](propertyinfo.md) collection is available from any collection that you might be holding.</span></span> <span data-ttu-id="a6216-107">La collection **PropertyInfo** contient un élément pour chaque propriété disponible.</span><span class="sxs-lookup"><span data-stu-id="a6216-107">The **PropertyInfo** collection contains an item for each available property.</span></span> <span data-ttu-id="a6216-108">Vous pouvez énumérer ces éléments pour déterminer si une propriété donnée est disponible.</span><span class="sxs-lookup"><span data-stu-id="a6216-108">You can enumerate through these items to determine whether a given property is available.</span></span>

<span data-ttu-id="a6216-109">Vous pouvez obtenir la collection [**PropertyInfo**](propertyinfo.md) à partir de n’importe quelle collection que vous conservez à l’aide de la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , en laissant le deuxième paramètre vide à l’emplacement où vous spécifiez normalement la propriété de clé d’un élément parent.</span><span class="sxs-lookup"><span data-stu-id="a6216-109">You can get the [**PropertyInfo**](propertyinfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6216-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6216-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6216-111">Obtention et définition des propriétés</span><span class="sxs-lookup"><span data-stu-id="a6216-111">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="a6216-112">Interdépendances entre les propriétés</span><span class="sxs-lookup"><span data-stu-id="a6216-112">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="a6216-113">Enregistrement ou rejet des modifications</span><span class="sxs-lookup"><span data-stu-id="a6216-113">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



