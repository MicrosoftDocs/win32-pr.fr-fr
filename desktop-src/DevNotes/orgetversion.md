---
description: Cette fonction récupère la version de la bibliothèque de Registre hors connexion.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: ORGetVersion, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541286"
---
# <a name="orgetversion-function"></a><span data-ttu-id="03942-103">ORGetVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="03942-103">ORGetVersion function</span></span>

<span data-ttu-id="03942-104">Cette fonction récupère la version de la bibliothèque de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="03942-104">This function retrieves the version of the offline registry library.</span></span>

## <a name="syntax"></a><span data-ttu-id="03942-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03942-105">Syntax</span></span>


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="03942-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03942-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03942-107">*pdwMajorVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="03942-107">*pdwMajorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03942-108">Pointeur vers une variable qui doit recevoir la version principale de la bibliothèque de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="03942-108">A pointer to a variable to receive the major version of the offline registry library.</span></span> <span data-ttu-id="03942-109">Pour la version initiale de la bibliothèque, la valeur est 1.</span><span class="sxs-lookup"><span data-stu-id="03942-109">For the initial release of the library, the value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="03942-110">*pdwMinorVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="03942-110">*pdwMinorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03942-111">Pointeur vers une variable qui doit recevoir la version mineure de la bibliothèque de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="03942-111">A pointer to a variable to receive the minor version of the offline registry library.</span></span> <span data-ttu-id="03942-112">Pour la version initiale de la bibliothèque, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="03942-112">For the initial release of the library, the value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03942-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03942-113">Return value</span></span>

<span data-ttu-id="03942-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="03942-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03942-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03942-115">Requirements</span></span>



| <span data-ttu-id="03942-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03942-116">Requirement</span></span> | <span data-ttu-id="03942-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="03942-117">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03942-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="03942-118">Redistributable</span></span><br/> | <span data-ttu-id="03942-119">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="03942-119">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="03942-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="03942-120">Header</span></span><br/>          | <dl> <span data-ttu-id="03942-121"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="03942-121"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="03942-122">DLL</span><span class="sxs-lookup"><span data-stu-id="03942-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="03942-123"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03942-123"><dt>Offreg.dll</dt></span></span> </dl> |



 

 




