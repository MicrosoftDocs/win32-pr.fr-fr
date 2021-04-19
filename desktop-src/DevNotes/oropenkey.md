---
description: Ouvre la clé de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: OROpenKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521684"
---
# <a name="oropenkey-function"></a><span data-ttu-id="9e801-103">OROpenKey fonction)</span><span class="sxs-lookup"><span data-stu-id="9e801-103">OROpenKey function</span></span>

<span data-ttu-id="9e801-104">Ouvre la clé de Registre spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9e801-104">Opens the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e801-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e801-105">Syntax</span></span>


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="9e801-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e801-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e801-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e801-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e801-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9e801-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="9e801-109">*lpSubKeyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9e801-109">*lpSubKeyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e801-110">Pointeur vers une chaîne UNICODE qui contient le nom de la clé de Registre à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="9e801-110">A pointer to a UNICODE string that contains the name of the registry key to be opened.</span></span> <span data-ttu-id="9e801-111">Cette clé doit être une sous-clé de la clé identifiée par le paramètre *handle* .</span><span class="sxs-lookup"><span data-stu-id="9e801-111">This key must be a subkey of the key identified by the *Handle* parameter.</span></span>

<span data-ttu-id="9e801-112">Les noms de clés ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="9e801-112">Key names are not case sensitive.</span></span>

<span data-ttu-id="9e801-113">Si ce paramètre est **null** ou un pointeur vers une chaîne vide, la fonction retourne le même handle que celui qui a été passé.</span><span class="sxs-lookup"><span data-stu-id="9e801-113">If this parameter is **NULL** or a pointer to an empty string, the function returns the same handle that was passed in.</span></span> <span data-ttu-id="9e801-114">Si la clé spécifiée par le paramètre *descripteur* est la clé racine de la ruche, la fonction retourne un \_ paramètre non valide de l’erreur \_ .</span><span class="sxs-lookup"><span data-stu-id="9e801-114">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="9e801-115">Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="9e801-115">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e801-116">*phkResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9e801-116">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e801-117">Pointeur vers une variable qui reçoit un handle vers la clé ouverte.</span><span class="sxs-lookup"><span data-stu-id="9e801-117">A pointer to a variable that receives a handle to the opened key.</span></span> <span data-ttu-id="9e801-118">Utilisez la fonction [**ORCloseKey**](orclosekey.md) pour fermer la clé une fois que vous avez fini d’utiliser le handle.</span><span class="sxs-lookup"><span data-stu-id="9e801-118">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e801-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e801-119">Return value</span></span>

<span data-ttu-id="9e801-120">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="9e801-120">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9e801-121">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9e801-121">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="9e801-122">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="9e801-122">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="9e801-123">Si le handle à retourner est un descripteur de la clé racine de la ruche, la fonction retourne un \_ paramètre d’erreur non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="9e801-123">If the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="9e801-124">Si la clé spécifiée a été marquée comme supprimée, cette fonction retourne la clé d’erreur \_ \_ supprimée.</span><span class="sxs-lookup"><span data-stu-id="9e801-124">If the specified key has been marked as deleted, this function returns ERROR\_KEY\_DELETED.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e801-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9e801-125">Remarks</span></span>

<span data-ttu-id="9e801-126">Impossible d’utiliser la fonction **OROpenKey** pour ouvrir la clé racine dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9e801-126">The **OROpenKey** function cannot be used to open the root key in an offline registry hive.</span></span> <span data-ttu-id="9e801-127">Pour obtenir un descripteur de la clé racine d’une ruche, utilisez la fonction [**OROpenHive**](oropenhive.md) pour charger la ruche en mémoire.</span><span class="sxs-lookup"><span data-stu-id="9e801-127">To obtain a handle to the root key of a hive, use the [**OROpenHive**](oropenhive.md) function to load the hive into memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e801-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e801-128">Requirements</span></span>



| <span data-ttu-id="9e801-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e801-129">Requirement</span></span> | <span data-ttu-id="9e801-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e801-130">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e801-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9e801-131">Redistributable</span></span><br/> | <span data-ttu-id="9e801-132">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="9e801-132">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="9e801-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e801-133">Header</span></span><br/>          | <dl> <span data-ttu-id="9e801-134"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e801-134"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e801-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9e801-135">DLL</span></span><br/>             | <dl> <span data-ttu-id="9e801-136"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e801-136"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e801-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e801-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e801-138">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="9e801-138">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="9e801-139">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="9e801-139">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="9e801-140">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="9e801-140">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="9e801-141">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="9e801-141">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
