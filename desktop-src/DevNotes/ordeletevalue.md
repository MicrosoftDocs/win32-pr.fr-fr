---
description: Supprime une valeur nommée de la clé de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: ORDeleteValue, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545630"
---
# <a name="ordeletevalue-function"></a><span data-ttu-id="164a5-103">ORDeleteValue fonction)</span><span class="sxs-lookup"><span data-stu-id="164a5-103">ORDeleteValue function</span></span>

<span data-ttu-id="164a5-104">Supprime une valeur nommée de la clé de Registre spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="164a5-104">Removes a named value from the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="164a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="164a5-105">Syntax</span></span>


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a><span data-ttu-id="164a5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="164a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="164a5-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="164a5-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="164a5-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="164a5-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="164a5-109">*lpValueName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="164a5-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="164a5-110">Valeur de Registre à supprimer.</span><span class="sxs-lookup"><span data-stu-id="164a5-110">The registry value to be removed.</span></span> <span data-ttu-id="164a5-111">Si ce paramètre a la valeur **null** ou est une chaîne vide, la valeur par défaut sans nom définie par la fonction [**ORSetValue**](orsetvalue.md) est supprimée.</span><span class="sxs-lookup"><span data-stu-id="164a5-111">If this parameter is **NULL** or an empty string, the default unnamed value set by the [**ORSetValue**](orsetvalue.md) function is removed.</span></span>

<span data-ttu-id="164a5-112">Les noms de valeurs ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="164a5-112">Value names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="164a5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="164a5-113">Return value</span></span>

<span data-ttu-id="164a5-114">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="164a5-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="164a5-115">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="164a5-115">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="164a5-116">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="164a5-116">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="164a5-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="164a5-117">Requirements</span></span>



| <span data-ttu-id="164a5-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="164a5-118">Requirement</span></span> | <span data-ttu-id="164a5-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="164a5-119">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="164a5-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="164a5-120">Redistributable</span></span><br/> | <span data-ttu-id="164a5-121">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="164a5-121">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="164a5-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="164a5-122">Header</span></span><br/>          | <dl> <span data-ttu-id="164a5-123"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="164a5-123"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="164a5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="164a5-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="164a5-125"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="164a5-125"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="164a5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="164a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="164a5-127">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="164a5-127">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
