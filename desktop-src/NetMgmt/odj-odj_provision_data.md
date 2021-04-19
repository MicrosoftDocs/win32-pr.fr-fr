---
title: ODJ_PROVISION_DATA
description: Définition du ODJ_PROVISION_DATA IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "106510291"
---
# <a name="odj_provision_data-structure"></a><span data-ttu-id="31cfe-103">Structure ODJ_PROVISION_DATA</span><span class="sxs-lookup"><span data-stu-id="31cfe-103">ODJ_PROVISION_DATA structure</span></span>

<span data-ttu-id="31cfe-104">Spécifie la structure de sérialisation la plus à l’extérieur utilisée par les API de jonction de domaine hors connexion.</span><span class="sxs-lookup"><span data-stu-id="31cfe-104">Specifies the outermost serialization structure used by the offline domain join apis.</span></span>

## <a name="syntax"></a><span data-ttu-id="31cfe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31cfe-105">Syntax</span></span>

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a><span data-ttu-id="31cfe-106">Membres</span><span class="sxs-lookup"><span data-stu-id="31cfe-106">Members</span></span>

### <a name="ulversion"></a><span data-ttu-id="31cfe-107">ulVersion</span><span class="sxs-lookup"><span data-stu-id="31cfe-107">ulVersion</span></span>

<span data-ttu-id="31cfe-108">La valeur doit être 1.</span><span class="sxs-lookup"><span data-stu-id="31cfe-108">This must be set to 1.</span></span>

### <a name="ulcblobs"></a><span data-ttu-id="31cfe-109">ulcBlobs</span><span class="sxs-lookup"><span data-stu-id="31cfe-109">ulcBlobs</span></span>

<span data-ttu-id="31cfe-110">Doit être défini sur le nombre d’éléments dans le tableau pBlobs.</span><span class="sxs-lookup"><span data-stu-id="31cfe-110">This must be set to the number of elements in the pBlobs array.</span></span>

### <a name="pblobs"></a><span data-ttu-id="31cfe-111">pBlobs</span><span class="sxs-lookup"><span data-stu-id="31cfe-111">pBlobs</span></span>

<span data-ttu-id="31cfe-112">Pointe vers un tableau de structures de ODJ_BLOB.</span><span class="sxs-lookup"><span data-stu-id="31cfe-112">Points to an array of ODJ_BLOB structures.</span></span>

## <a name="see-also"></a><span data-ttu-id="31cfe-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31cfe-113">See also</span></span>

[<span data-ttu-id="31cfe-114">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="31cfe-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="31cfe-115">**\_objet BLOB ODJ**</span><span class="sxs-lookup"><span data-stu-id="31cfe-115">**ODJ\_BLOB**</span></span>](odj-odj_blob.md)


