---
description: Le flux d’informations de synthèse contient des informations sur le package qui peuvent être consultées via l’Explorateur Microsoft Windows.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: À propos du flux d’informations de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115394"
---
# <a name="about-the-summary-information-stream"></a><span data-ttu-id="207c3-103">À propos du flux d’informations de synthèse</span><span class="sxs-lookup"><span data-stu-id="207c3-103">About the Summary Information Stream</span></span>

<span data-ttu-id="207c3-104">Le flux d’informations de synthèse contient des informations sur le package qui peuvent être consultées via l’Explorateur Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="207c3-104">The summary information stream contains information about the package that can be viewed through Microsoft Windows Explorer.</span></span> <span data-ttu-id="207c3-105">Ces informations sont accessibles via l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="207c3-105">This information is accessible through the **IStream** interface.</span></span> <span data-ttu-id="207c3-106">Il revient à l’auteur de fournir les valeurs de chacune de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="207c3-106">It is up to the author to provide the values for each of these properties.</span></span>

<span data-ttu-id="207c3-107">Le flux d’informations de synthèse utilise COM pour fournir un stockage structuré des bases de données.</span><span class="sxs-lookup"><span data-stu-id="207c3-107">The summary information stream uses COM to provide structured storage of databases.</span></span> <span data-ttu-id="207c3-108">COM prend en charge le concept de stockage structuré accessible via l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="207c3-108">COM supports the concept of structured storage accessible through the **IStream** interface.</span></span> <span data-ttu-id="207c3-109">Le stockage structuré, à son tour, prend en charge le concept de jeux de propriétés comme méthode flexible pour sérialiser pratiquement toutes les informations.</span><span class="sxs-lookup"><span data-stu-id="207c3-109">Structured storage, in turn, supports the concept of property sets as a flexible method for serializing almost any information.</span></span> <span data-ttu-id="207c3-110">La spécification COM définit un jeu de propriétés standard unique, des informations de synthèse, qui est utilisé pour remplir les feuilles de propriétés visibles à partir de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="207c3-110">The COM specification defines a single standard property set, summary information, which is used to populate property sheets viewable from Windows Explorer.</span></span> <span data-ttu-id="207c3-111">Par conséquent, les utilisateurs peuvent afficher les informations stockées dans le flux d’informations de résumé lorsqu’ils cliquent avec le bouton droit sur une base de données du programme d’installation ou qu’ils sélectionnent [Propriétés](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="207c3-111">So, information stored in the summary information stream can be viewed by users when they right-click an installer database or transform and select [Properties](about-properties.md).</span></span>

<span data-ttu-id="207c3-112">Pour obtenir la liste des propriétés de résumé, consultez [jeu de propriétés de flux d’informations résumées](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="207c3-112">For a list of the summary property set see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="207c3-113">Pour obtenir une brève description des propriétés des informations de résumé utilisées avec les bases de données, les transformations et les correctifs, consultez [descriptions des propriétés récapitulatives](summary-property-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="207c3-113">For brief descriptions of the Summary Information properties used with databases, transforms, and patches, see [Summary Property Descriptions](summary-property-descriptions.md).</span></span>

 

 



