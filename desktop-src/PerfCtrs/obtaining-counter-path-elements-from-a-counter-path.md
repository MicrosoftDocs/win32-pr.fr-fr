---
description: Pour récupérer les éléments d’un chemin d’accès, appelez la fonction PdhParseCounterPath. La fonction analyse les éléments d’un chemin d’accès de compteur et les retourne dans \_ une \_ structure d’éléments de chemin d’accès de compteur PDH \_ .
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Obtention d’éléments de chemin d’accès de compteur à partir d’un chemin de compteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545817"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a><span data-ttu-id="d9d3c-104">Obtention d’éléments de chemin d’accès de compteur à partir d’un chemin de compteur</span><span class="sxs-lookup"><span data-stu-id="d9d3c-104">Obtaining Counter Path Elements from a Counter Path</span></span>

<span data-ttu-id="d9d3c-105">Pour récupérer les éléments d’un chemin d’accès, appelez la fonction [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) .</span><span class="sxs-lookup"><span data-stu-id="d9d3c-105">To retrieve the elements of a path, call the [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) function.</span></span> <span data-ttu-id="d9d3c-106">La fonction analyse les éléments d’un chemin d’accès de compteur et les retourne dans une structure [**\_ \_ d' \_ éléments de chemin d’accès de compteur PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) .</span><span class="sxs-lookup"><span data-stu-id="d9d3c-106">The function parses the elements of a counter path and returns them in a [**PDH\_COUNTER\_PATH\_ELEMENTS**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) structure.</span></span>

<span data-ttu-id="d9d3c-107">Si vous avez un nom d’instance complexe (un qui contient une instance parente et un index d’instance), vous pouvez appeler la fonction [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) pour extraire le nom de l’instance, l’index d’instance et le nom du parent.</span><span class="sxs-lookup"><span data-stu-id="d9d3c-107">If you have a complex instance name (one that contains a parent instance and instance index), you can call the [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) function to extract the instance name, instance index, and parent name.</span></span>

 

 



