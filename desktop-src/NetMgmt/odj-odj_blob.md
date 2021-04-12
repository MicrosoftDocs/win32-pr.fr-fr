---
title: ODJ_BLOB
description: Définition du ODJ_BLOB IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104463890"
---
# <a name="odj_blob-structure"></a><span data-ttu-id="21e5a-103">Structure ODJ_BLOB</span><span class="sxs-lookup"><span data-stu-id="21e5a-103">ODJ_BLOB structure</span></span>

<span data-ttu-id="21e5a-104">Spécifie une structure contenant soit une structure de ODJ_WIN7BLOB sérialisée, soit une structure de OP_PACKAGE sérialisée.</span><span class="sxs-lookup"><span data-stu-id="21e5a-104">Specifies a structure containing either a serialized ODJ_WIN7BLOB structure or a serialized OP_PACKAGE structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e5a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21e5a-105">Syntax</span></span>

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a><span data-ttu-id="21e5a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="21e5a-106">Members</span></span>

### <a name="ulodjformat"></a><span data-ttu-id="21e5a-107">ulODJFormat</span><span class="sxs-lookup"><span data-stu-id="21e5a-107">ulODJFormat</span></span>

<span data-ttu-id="21e5a-108">Spécifie la version logique de la structure et doit être défini sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="21e5a-108">Specifies the logical version of the structure and must be set to one of the following values:</span></span>

|<span data-ttu-id="21e5a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="21e5a-109">Value</span></span>|<span data-ttu-id="21e5a-110">Signification</span><span class="sxs-lookup"><span data-stu-id="21e5a-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="21e5a-111">ODJ_WIN7_FORMAT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="21e5a-111">ODJ_WIN7_FORMAT (0x00000001)</span></span>|<span data-ttu-id="21e5a-112">Les octets contenus dans pBlob doivent contenir une structure ODJ_WIN7_BLOB sérialisée.</span><span class="sxs-lookup"><span data-stu-id="21e5a-112">The bytes contained in pBlob must contain a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="21e5a-113">ODJ_WIN8_FORMAT (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="21e5a-113">ODJ_WIN8_FORMAT (0x00000002)</span></span>|<span data-ttu-id="21e5a-114">Les octets contenus dans pBlob doivent contenir une structure OP_PACKAGE sérialisée.</span><span class="sxs-lookup"><span data-stu-id="21e5a-114">The bytes contained in pBlob must contain a serialized OP_PACKAGE structure.</span></span>|

### <a name="cbblob"></a><span data-ttu-id="21e5a-115">cbBlob</span><span class="sxs-lookup"><span data-stu-id="21e5a-115">cbBlob</span></span>

<span data-ttu-id="21e5a-116">Doit être défini sur le nombre d’octets dans le tableau pBlob.</span><span class="sxs-lookup"><span data-stu-id="21e5a-116">This must be set to the number of bytes in the pBlob array.</span></span>

### <a name="pblob"></a><span data-ttu-id="21e5a-117">pBlob</span><span class="sxs-lookup"><span data-stu-id="21e5a-117">pBlob</span></span>

<span data-ttu-id="21e5a-118">Pointe vers une mémoire tampon d’octets qui contient une structure sérialisée telle que spécifiée par ulODJFormat ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="21e5a-118">Points to a byte buffer containing a serialized structure as specified by ulODJFormat above.</span></span>

## <a name="see-also"></a><span data-ttu-id="21e5a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21e5a-119">See also</span></span>

[<span data-ttu-id="21e5a-120">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="21e5a-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

