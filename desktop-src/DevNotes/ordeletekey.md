---
description: Supprime une sous-clé et ses valeurs d’une ruche de Registre hors connexion.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: ORDeleteKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521702"
---
# <a name="ordeletekey-function"></a><span data-ttu-id="3dbf9-103">ORDeleteKey fonction)</span><span class="sxs-lookup"><span data-stu-id="3dbf9-103">ORDeleteKey function</span></span>

<span data-ttu-id="3dbf9-104">Supprime une sous-clé et ses valeurs d’une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-104">Deletes a subkey and its values from an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dbf9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dbf9-105">Syntax</span></span>


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a><span data-ttu-id="3dbf9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dbf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dbf9-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3dbf9-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbf9-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-108">A handle to an open registry key in an offline registry hive.</span></span> <span data-ttu-id="3dbf9-109">Ce descripteur est retourné par la fonction [**ORCreateKey**](orcreatekey.md) ou [**OROpenKey**](oropenkey.md) .</span><span class="sxs-lookup"><span data-stu-id="3dbf9-109">This handle is returned by the [**ORCreateKey**](orcreatekey.md) or [**OROpenKey**](oropenkey.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3dbf9-110">*lpSubKey* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3dbf9-110">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbf9-111">Nom de la clé à supprimer.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-111">The name of the key to be deleted.</span></span> <span data-ttu-id="3dbf9-112">Il doit s’agir d’une sous-clé de la clé que le *handle* identifie, mais il ne peut pas avoir de sous-clés.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-112">It must be a subkey of the key that *Handle* identifies, but it cannot have subkeys.</span></span>

<span data-ttu-id="3dbf9-113">Si la sous-clé n’existe pas, la fonction retourne l’erreur \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-113">If the subkey does not exist, the function returns ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="3dbf9-114">Si ce paramètre a la **valeur null**, la fonction supprime la clé spécifiée par le paramètre *handle* .</span><span class="sxs-lookup"><span data-stu-id="3dbf9-114">If this parameter is **NULL**, the function deletes the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="3dbf9-115">Si la clé spécifiée par le paramètre *descripteur* est la clé racine de la ruche, la fonction retourne un \_ paramètre non valide de l’erreur \_ .</span><span class="sxs-lookup"><span data-stu-id="3dbf9-115">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="3dbf9-116">Les noms de clés ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-116">Key names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dbf9-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3dbf9-117">Return value</span></span>

<span data-ttu-id="3dbf9-118">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3dbf9-119">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-119">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="3dbf9-120">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="3dbf9-121">Les codes d’erreur possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3dbf9-121">Possible error codes include the following:</span></span>

-   <span data-ttu-id="3dbf9-122">Si la sous-clé spécifiée n’existe pas, la fonction retourne le fichier d’erreur \_ \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-122">If the specified subkey does not exist, the function returns ERROR\_FILE\_NOT\_FOUND.</span></span>
-   <span data-ttu-id="3dbf9-123">Si la sous-clé spécifiée est la clé racine de la ruche du Registre, la fonction retourne un paramètre d’erreur \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="3dbf9-123">If the specified subkey is the root key of the registry hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>
-   <span data-ttu-id="3dbf9-124">Si la sous-clé spécifiée a des sous-clés, la fonction retourne la clé d’erreur \_ \_ a des \_ enfants.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-124">If the specified subkey has subkeys, the function returns ERROR\_KEY\_HAS\_CHILDREN.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dbf9-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3dbf9-125">Remarks</span></span>

<span data-ttu-id="3dbf9-126">Si la clé de Registre spécifiée existe, elle est marquée comme supprimée.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-126">If the specified registry key exists, it is marked as deleted.</span></span> <span data-ttu-id="3dbf9-127">Une clé supprimée n’est pas supprimée tant que le dernier descripteur n’est pas fermé.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-127">A deleted key is not removed until the last handle to it is closed.</span></span>

<span data-ttu-id="3dbf9-128">La clé à supprimer ne doit pas avoir de sous-clés.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-128">The key to be deleted must not have subkeys.</span></span> <span data-ttu-id="3dbf9-129">Pour supprimer une clé et toutes ses sous-clés, utilisez la fonction [**OREnumKey**](orenumkey.md) pour énumérer les sous-clés et les supprimer individuellement.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-129">To delete a key and all its subkeys, use the [**OREnumKey**](orenumkey.md) function to enumerate the subkeys and delete them individually.</span></span>

<span data-ttu-id="3dbf9-130">Seule la fonction [**ORCloseKey**](orclosekey.md) peut être appelée sur une clé supprimée. toutes les autres opérations de Registre hors connexion échouent.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-130">Only the [**ORCloseKey**](orclosekey.md) function may be called on a deleted key; all other offline registry operations fail.</span></span> <span data-ttu-id="3dbf9-131">Si la clé supprimée a été créée explicitement en appelant [**ORCreateKey**](orcreatekey.md), les ressources associées à la clé sont libérées lorsque le dernier handle de la clé supprimée est fermé.</span><span class="sxs-lookup"><span data-stu-id="3dbf9-131">If the deleted key was explicitly created by calling [**ORCreateKey**](orcreatekey.md), resources associated with the key are released when the last handle to the deleted key is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dbf9-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3dbf9-132">Requirements</span></span>



| <span data-ttu-id="3dbf9-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3dbf9-133">Requirement</span></span> | <span data-ttu-id="3dbf9-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dbf9-134">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbf9-135">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3dbf9-135">Redistributable</span></span><br/> | <span data-ttu-id="3dbf9-136">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="3dbf9-136">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="3dbf9-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="3dbf9-137">Header</span></span><br/>          | <dl> <span data-ttu-id="3dbf9-138"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dbf9-138"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="3dbf9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3dbf9-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="3dbf9-140"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dbf9-140"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dbf9-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dbf9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbf9-142">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="3dbf9-142">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="3dbf9-143">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="3dbf9-143">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="3dbf9-144">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="3dbf9-144">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="3dbf9-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="3dbf9-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
