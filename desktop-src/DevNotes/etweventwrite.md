---
description: 'En savoir plus sur : fonction EtwEventWrite'
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033732"
---
# <a name="etweventwrite-function"></a><span data-ttu-id="30758-103">EtwEventWrite fonction)</span><span class="sxs-lookup"><span data-stu-id="30758-103">EtwEventWrite function</span></span>

<span data-ttu-id="30758-104">[La fonction EtwEventWrite et les structures qu’elle retourne sont internes au système d’exploitation et sujettes à changement d’une version de Windows à une autre.]</span><span class="sxs-lookup"><span data-stu-id="30758-104">[The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="30758-105">Écrit un événement de base dans une session.</span><span class="sxs-lookup"><span data-stu-id="30758-105">Writes a basic event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="30758-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30758-106">Syntax</span></span>

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="30758-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30758-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30758-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="30758-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="30758-109">RegHandle pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="30758-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="30758-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="30758-110">*EventDescriptor*</span></span>
</dt> <dd>

<span data-ttu-id="30758-111">Descripteur d’événement de l’événement à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="30758-111">Event descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="30758-112">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="30758-112">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="30758-113">Nombre d’éléments de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="30758-113">Number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="30758-114">*UserData*</span><span class="sxs-lookup"><span data-stu-id="30758-114">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="30758-115">Pointeur vers un tableau d’éléments de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="30758-115">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30758-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30758-116">Return value</span></span>

<span data-ttu-id="30758-117">Code d’erreur Win32.</span><span class="sxs-lookup"><span data-stu-id="30758-117">A Win32 error code.</span></span>


## <a name="remarks"></a><span data-ttu-id="30758-118">Notes</span><span class="sxs-lookup"><span data-stu-id="30758-118">Remarks</span></span>

<span data-ttu-id="30758-119">La fonction EtwEventWrite et les structures qu’elle retourne sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à une autre.</span><span class="sxs-lookup"><span data-stu-id="30758-119">The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="30758-120">Pour maintenir la compatibilité de votre application, il est préférable d’utiliser à la place des fonctions publiques.</span><span class="sxs-lookup"><span data-stu-id="30758-120">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="30758-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30758-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="30758-122">**Plateforme cible**</span><span class="sxs-lookup"><span data-stu-id="30758-122">**Target Platform**</span></span> | <span data-ttu-id="30758-123">Windows</span><span class="sxs-lookup"><span data-stu-id="30758-123">Windows</span></span> |
| <span data-ttu-id="30758-124">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="30758-124">**Header**</span></span> | <span data-ttu-id="30758-125">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="30758-125">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="30758-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30758-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30758-127">EventWrite</span><span class="sxs-lookup"><span data-stu-id="30758-127">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="30758-128">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="30758-128">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
