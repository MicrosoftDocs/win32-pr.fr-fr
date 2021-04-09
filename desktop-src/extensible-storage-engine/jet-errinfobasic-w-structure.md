---
description: 'En savoir plus sur : structure JET_ERRINFOBASIC_W'
title: Structure JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103954030"
---
# <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="44474-103">Structure JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="44474-103">JET_ERRINFOBASIC_W Structure</span></span>


<span data-ttu-id="44474-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="44474-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="44474-105">Structure JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="44474-105">JET_ERRINFOBASIC_W Structure</span></span>

<span data-ttu-id="44474-106">La structure **JET_ERRINFOBASIC_W** définit les données retournées à partir de la méthode [JetGetErrorInfo ()](./jetgeterrorinfow-function.md) lorsque la JET_ErrorInfoSpecificErr InfoLevel est passée.</span><span class="sxs-lookup"><span data-stu-id="44474-106">The **JET_ERRINFOBASIC_W** structure defines the data that is returned from the [JetGetErrorInfo()](./jetgeterrorinfow-function.md) method when the JET_ErrorInfoSpecificErr InfoLevel is passed in.</span></span>

<span data-ttu-id="44474-107">Remarque : cette documentation est basée sur une version préliminaire du moteur de stockage extensible.</span><span class="sxs-lookup"><span data-stu-id="44474-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="44474-108">Ces informations sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="44474-108">This information is subject to change.</span></span>

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a><span data-ttu-id="44474-109">Membres</span><span class="sxs-lookup"><span data-stu-id="44474-109">Members</span></span>

<span data-ttu-id="44474-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="44474-110">**cbStruct**</span></span>

<span data-ttu-id="44474-111">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="44474-111">The size of the structure, in bytes.</span></span> <span data-ttu-id="44474-112">Elle doit être définie sur sizeof (JET_ERRINFOBASIC).</span><span class="sxs-lookup"><span data-stu-id="44474-112">It must be set to sizeof( JET_ERRINFOBASIC ).</span></span>

<span data-ttu-id="44474-113">**errValue**</span><span class="sxs-lookup"><span data-stu-id="44474-113">**errValue**</span></span>

<span data-ttu-id="44474-114">Valeur d’erreur qui a été évaluée, comme passé pour l’argument *pvResult* à [JetGetErrorInfo ()](./jetgeterrorinfow-function.md).</span><span class="sxs-lookup"><span data-stu-id="44474-114">The error value that was evaluated, as passed in for the *pvResult* argument to [JetGetErrorInfo()](./jetgeterrorinfow-function.md).</span></span>

<span data-ttu-id="44474-115">**errcatMostSpecific**</span><span class="sxs-lookup"><span data-stu-id="44474-115">**errcatMostSpecific**</span></span>

<span data-ttu-id="44474-116">La constante [JET_ERRCAT](./jet-errcat.md) de niveau le plus bas qui est associée à l’erreur ; autrement dit, la catégorie de niveau feuille dans la hiérarchie de catégories documentée dans [JET_ERRCAT](./jet-errcat.md).</span><span class="sxs-lookup"><span data-stu-id="44474-116">The lowest-level [JET_ERRCAT](./jet-errcat.md) constant that is associated with the error; that is, the leaf-level category in the category hierarchy documented in [JET_ERRCAT](./jet-errcat.md).</span></span>

<span data-ttu-id="44474-117">**rgCategoricalHierarchy \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="44474-117">**rgCategoricalHierarchy\[8\]**</span></span>

<span data-ttu-id="44474-118">La hiérarchie des catégories d’erreur associée à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="44474-118">The hierarchy of error categories that is associated with the error.</span></span> <span data-ttu-id="44474-119">La position 0 est le niveau le plus élevé dans la hiérarchie de [JET_ERRCAT](./jet-errcat.md), et le reste sont des sous-catégories jusqu’à ce que la catégorie la plus spécifique soit définie, après quoi toutes les catégories sont JET_errcatUnknownes.</span><span class="sxs-lookup"><span data-stu-id="44474-119">Position 0 is the highest level in the hierarchy of [JET_ERRCAT](./jet-errcat.md), and the rest are subcategories until the most specific category is set, after which all categories are JET_errcatUnknown.</span></span>

<span data-ttu-id="44474-120">**lSourceLine**</span><span class="sxs-lookup"><span data-stu-id="44474-120">**lSourceLine**</span></span>

<span data-ttu-id="44474-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="44474-121">Reserved.</span></span>

<span data-ttu-id="44474-122">**rgszSourceFile \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="44474-122">**rgszSourceFile\[64\]**</span></span>

<span data-ttu-id="44474-123">Réservé.</span><span class="sxs-lookup"><span data-stu-id="44474-123">Reserved.</span></span>

### <a name="requirements"></a><span data-ttu-id="44474-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44474-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44474-125"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="44474-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="44474-126">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="44474-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44474-127"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="44474-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="44474-128">Nécessite Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="44474-128">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44474-129"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="44474-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="44474-130">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="44474-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
