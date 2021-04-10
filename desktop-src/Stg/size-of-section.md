---
title: Taille de la section
description: Le type de données de la taille de la section indique la taille, en octets, de la section.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197343"
---
# <a name="size-of-section"></a><span data-ttu-id="1a7fa-103">Taille de la section</span><span class="sxs-lookup"><span data-stu-id="1a7fa-103">Size of Section</span></span>

<span data-ttu-id="1a7fa-104">Le type de données de la taille de la section indique la taille, en octets, de la section.</span><span class="sxs-lookup"><span data-stu-id="1a7fa-104">The section size data type indicates the size, in bytes, of the section.</span></span> <span data-ttu-id="1a7fa-105">Étant donné que la taille de la section est les 4 premiers octets, les sections peuvent être copiées sous la forme d’un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="1a7fa-105">Because the section size is the first 4 bytes, sections can be copied as an array of bytes.</span></span> <span data-ttu-id="1a7fa-106">La taille de la section doit toujours être un multiple de quatre.</span><span class="sxs-lookup"><span data-stu-id="1a7fa-106">The section size should always be a multiple of four.</span></span>

<span data-ttu-id="1a7fa-107">Par exemple, une section vide, autrement dit, l’une avec les propriétés zéro, aurait un nombre d’octets de huit (le nombre d’octets **DWORD** et le nombre de propriétés **DWORD** ).</span><span class="sxs-lookup"><span data-stu-id="1a7fa-107">For example, an empty section, that is, one with zero properties in it, would have a byte count of eight (the **DWORD** byte count and the **DWORD** count of properties).</span></span> <span data-ttu-id="1a7fa-108">La section elle-même contient les 8 octets suivants : **08 00 00 00 00 00 00 00**.</span><span class="sxs-lookup"><span data-stu-id="1a7fa-108">The section itself would contain the 8 bytes: **08 00 00 00 00 00 00 00**.</span></span>

 

 




