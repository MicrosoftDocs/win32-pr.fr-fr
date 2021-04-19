---
title: Section
description: La section est la troisième partie du flux de jeu de propriétés et contient les valeurs de jeu de propriétés réelles.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f51891d14a9690e295379b7bcf619fe0fbe19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509193"
---
# <a name="section"></a><span data-ttu-id="747d3-103">Section</span><span class="sxs-lookup"><span data-stu-id="747d3-103">Section</span></span>

<span data-ttu-id="747d3-104">La section est la troisième partie du flux de jeu de propriétés et contient les valeurs de jeu de propriétés réelles.</span><span class="sxs-lookup"><span data-stu-id="747d3-104">The section is the third part of the property set stream and contains the actual property set values.</span></span>

<span data-ttu-id="747d3-105">Une section contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="747d3-105">A section contains:</span></span>

-   <span data-ttu-id="747d3-106">Nombre d’octets pour la section qui est incluse dans le nombre d’octets lui-même.</span><span class="sxs-lookup"><span data-stu-id="747d3-106">Byte count for the section which is inclusive of the byte count itself.</span></span>
-   <span data-ttu-id="747d3-107">Tableau de paires ID/ID de propriété 32 bits.</span><span class="sxs-lookup"><span data-stu-id="747d3-107">Array of 32-bit Property ID/Offset pairs.</span></span>
-   <span data-ttu-id="747d3-108">Tableau d’indicateurs de type de propriété/paires de valeurs.</span><span class="sxs-lookup"><span data-stu-id="747d3-108">Array of property Type Indicators/Value pairs.</span></span>

<span data-ttu-id="747d3-109">Les décalages représentent la distance entre le début de la section et le début de la paire propriété (type, valeur).</span><span class="sxs-lookup"><span data-stu-id="747d3-109">Offsets are the distance from the start of the section to the start of the property (type, value) pair.</span></span> <span data-ttu-id="747d3-110">Cela permet de copier une section en tant que tableau d’octets sans traduction de la structure interne.</span><span class="sxs-lookup"><span data-stu-id="747d3-110">This allows a section to be copied as an array of bytes without any translation of internal structure.</span></span>

<span data-ttu-id="747d3-111">Les Pseudo-structures suivantes illustrent le format d’une section.</span><span class="sxs-lookup"><span data-stu-id="747d3-111">The following pseudo-structures illustrate the format of a section.</span></span>

``` syntax
typedef struct tagPROPERTYSECTIONHEADER 
{ 
    DWORD  cbSection ;    // Size of Section 
    DWORD  cProperties ;  // Count of Properties in section 
} PROPERTYSECTIONHEADER; 
 
typedef struct tagPROPERTYIDOFFSET 
{ 
    DWORD  propid;    // Name of property 
    DWORD  dwOffset;  // Offset from start of section to property 
} PROPERTYIDOFFSET; 
 
typedef struct tagSERIALIZEDPROPERTYVALUE 
{ 
    DWORD  dwType;    // Property Type 
    BYTE   rgb[];     // Property Value 
} SERIALIZEDPROPERTYVALUE ;
```

 

 




