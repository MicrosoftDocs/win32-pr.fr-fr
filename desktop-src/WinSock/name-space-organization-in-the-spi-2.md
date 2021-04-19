---
description: Organisation de l’espace de noms dans le SPI Windows Sockets (Winsock).
ms.assetid: c369a476-23e4-48a1-912b-2d876deb0b88
title: Organisation de l’espace de noms dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a572ad86299f0bf5ba3e7f95662e1616da520608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515022"
---
# <a name="namespace-organization-in-the-spi"></a><span data-ttu-id="778bd-103">Organisation de l’espace de noms dans le SPI</span><span class="sxs-lookup"><span data-stu-id="778bd-103">Namespace Organization in the SPI</span></span>

<span data-ttu-id="778bd-104">De nombreux espaces de noms sont organisés hiérarchiquement.</span><span class="sxs-lookup"><span data-stu-id="778bd-104">Many namespaces are arranged hierarchically.</span></span> <span data-ttu-id="778bd-105">Certains, tels que X. 500 et NDS, permettent une imbrication illimitée.</span><span class="sxs-lookup"><span data-stu-id="778bd-105">Some, such as X.500 and NDS, allow unlimited nesting.</span></span> <span data-ttu-id="778bd-106">D’autres autorisent la combinaison de services dans un seul niveau de hiérarchie ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="778bd-106">Others allow services to be combined into a single level of hierarchy or group.</span></span> <span data-ttu-id="778bd-107">Il s’agit généralement d’un groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="778bd-107">This is typically referred to as a workgroup.</span></span> <span data-ttu-id="778bd-108">Lors de la construction d’une requête, il est souvent nécessaire d’établir un point de contexte dans une hiérarchie d’espaces de noms à partir de laquelle la recherche commence.</span><span class="sxs-lookup"><span data-stu-id="778bd-108">When constructing a query, it is often necessary to establish a context point within a namespace hierarchy from which the search will begin.</span></span>

 

 



