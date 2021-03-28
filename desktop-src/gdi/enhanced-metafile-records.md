---
description: Un métafichier amélioré est un tableau d’enregistrements.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Enregistrements de métafichiers améliorés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972682"
---
# <a name="enhanced-metafile-records"></a><span data-ttu-id="34564-103">Enregistrements de métafichiers améliorés</span><span class="sxs-lookup"><span data-stu-id="34564-103">Enhanced Metafile Records</span></span>

<span data-ttu-id="34564-104">Un métafichier amélioré est un tableau d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="34564-104">An enhanced metafile is an array of records.</span></span> <span data-ttu-id="34564-105">Un enregistrement de métafichier est une structure [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="34564-105">A metafile record is a variable-length [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) structure.</span></span> <span data-ttu-id="34564-106">Au début de chaque enregistrement de métafichier amélioré se trouve une structure [**le**](/windows/win32/api/wingdi/ns-wingdi-emr) , qui contient deux membres.</span><span class="sxs-lookup"><span data-stu-id="34564-106">At the beginning of every enhanced metafile record is an [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) structure, which contains two members.</span></span> <span data-ttu-id="34564-107">Le premier membre, iType, identifie le type d’enregistrement qui est, la fonction GDI dont les paramètres sont contenus dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="34564-107">The first member, iType, identifies the record type that is, the GDI function whose parameters are contained in the record.</span></span> <span data-ttu-id="34564-108">Étant donné que les structures sont de longueur variable, l’autre membre, nSize, contient la taille de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="34564-108">Because the structures are variable in length, the other member, nSize, contains the size of the record.</span></span> <span data-ttu-id="34564-109">Immédiatement après le membre nSize, les paramètres restants, le cas échéant, de la fonction GDI.</span><span class="sxs-lookup"><span data-stu-id="34564-109">Immediately following the nSize member are the remaining parameters, if any, of the GDI function.</span></span> <span data-ttu-id="34564-110">Le reste de la structure contient des données supplémentaires qui dépendent du type d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="34564-110">The remainder of the structure contains additional data that is dependent on the record type.</span></span>

<span data-ttu-id="34564-111">Le premier enregistrement dans un métafichier amélioré est toujours la structure [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) , qui est l’en-tête de métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="34564-111">The first record in an enhanced metafile is always the [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) structure, which is the enhanced-metafile header.</span></span> <span data-ttu-id="34564-112">L’en-tête spécifie les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="34564-112">The header specifies the following information:</span></span>

-   <span data-ttu-id="34564-113">Taille du métafichier, en octets</span><span class="sxs-lookup"><span data-stu-id="34564-113">Size of the metafile, in bytes</span></span>
-   <span data-ttu-id="34564-114">Dimensions du cadre d’image, en unités de périphérique</span><span class="sxs-lookup"><span data-stu-id="34564-114">Dimensions of the picture frame, in device units</span></span>
-   <span data-ttu-id="34564-115">Dimensions du cadre d’image, en unités de 01 à millimètres</span><span class="sxs-lookup"><span data-stu-id="34564-115">Dimensions of the picture frame, in .01-millimeter units</span></span>
-   <span data-ttu-id="34564-116">Nombre d’enregistrements dans le métafichier</span><span class="sxs-lookup"><span data-stu-id="34564-116">Number of records in the metafile</span></span>
-   <span data-ttu-id="34564-117">Décalage d’une description de texte facultative</span><span class="sxs-lookup"><span data-stu-id="34564-117">Offset to an optional text description</span></span>
-   <span data-ttu-id="34564-118">Taille de la palette facultative</span><span class="sxs-lookup"><span data-stu-id="34564-118">Size of the optional palette</span></span>
-   <span data-ttu-id="34564-119">Résolution de l’appareil d’origine, en pixels</span><span class="sxs-lookup"><span data-stu-id="34564-119">Resolution of the original device, in pixels</span></span>
-   <span data-ttu-id="34564-120">Résolution de l’appareil d’origine, en millimètres</span><span class="sxs-lookup"><span data-stu-id="34564-120">Resolution of the original device, in millimeters</span></span>

<span data-ttu-id="34564-121">Une description de texte facultative peut suivre l’enregistrement d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="34564-121">An optional text description can follow the header record.</span></span> <span data-ttu-id="34564-122">La description textuelle décrit l’image et le nom de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="34564-122">The text description describes the picture and the author's name.</span></span> <span data-ttu-id="34564-123">La palette facultative spécifie les couleurs utilisées pour créer le métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="34564-123">The optional palette specifies the colors used to create the enhanced metafile.</span></span> <span data-ttu-id="34564-124">Les enregistrements restants identifient les fonctions GDI utilisées pour créer l’image.</span><span class="sxs-lookup"><span data-stu-id="34564-124">The remaining records identify the GDI functions used to create the picture.</span></span> <span data-ttu-id="34564-125">La sortie hexadécimale suivante correspond à un enregistrement généré pour un appel à la fonction [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) .</span><span class="sxs-lookup"><span data-stu-id="34564-125">The following hexadecimal output corresponds to a record generated for a call to the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function.</span></span>


```C++
00000011 0000000C 00000004 
```



<span data-ttu-id="34564-126">La valeur 0x00000011 spécifie le type d’enregistrement (correspond à la \_ constante le SETMAPMODE définie dans le fichier WinGDI. h).</span><span class="sxs-lookup"><span data-stu-id="34564-126">The value 0x00000011 specifies the record type (corresponds to the EMR\_SETMAPMODE constant defined in the file Wingdi.h).</span></span> <span data-ttu-id="34564-127">La valeur 0x0000000C spécifie la longueur de l’enregistrement, en octets.</span><span class="sxs-lookup"><span data-stu-id="34564-127">The value 0x0000000C specifies the length of the record, in bytes.</span></span> <span data-ttu-id="34564-128">La valeur 0x00000004 identifie le mode de mappage (correspond à la \_ constante mm LOENGLISH définie dans la fonction [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) ).</span><span class="sxs-lookup"><span data-stu-id="34564-128">The value 0x00000004 identifies the mapping mode (corresponds to the MM\_LOENGLISH constant defined in the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function).</span></span>

<span data-ttu-id="34564-129">Pour obtenir la liste des types d’enregistrements supplémentaires, consultez [structures de métafichier](metafile-structures.md).</span><span class="sxs-lookup"><span data-stu-id="34564-129">For a list of additional record types, see [Metafile Structures](metafile-structures.md).</span></span>

 

 



