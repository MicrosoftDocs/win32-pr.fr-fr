---
description: Définit les données pour la valeur d’une clé de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: ORSetValue, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533453"
---
# <a name="orsetvalue-function"></a><span data-ttu-id="eadcb-103">ORSetValue fonction)</span><span class="sxs-lookup"><span data-stu-id="eadcb-103">ORSetValue function</span></span>

<span data-ttu-id="eadcb-104">Définit les données pour la valeur d’une clé de Registre spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="eadcb-104">Sets the data for the value of a specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="eadcb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eadcb-105">Syntax</span></span>


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="eadcb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eadcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eadcb-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eadcb-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eadcb-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="eadcb-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="eadcb-109">*lpValueName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eadcb-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eadcb-110">Nom de la valeur à définir.</span><span class="sxs-lookup"><span data-stu-id="eadcb-110">The name of the value to be set.</span></span> <span data-ttu-id="eadcb-111">Si une valeur portant ce nom n’est pas déjà présente dans la clé, la fonction l’ajoute à la clé.</span><span class="sxs-lookup"><span data-stu-id="eadcb-111">If a value with this name is not already present in the key, the function adds it to the key.</span></span>

<span data-ttu-id="eadcb-112">Si *lpValueName* a la valeur **null** ou est une chaîne vide, "", la fonction définit le type et les données pour la valeur sans nom ou par défaut de la clé.</span><span class="sxs-lookup"><span data-stu-id="eadcb-112">If *lpValueName* is **NULL** or an empty string, "", the function sets the type and data for the key's unnamed or default value.</span></span>

<span data-ttu-id="eadcb-113">Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="eadcb-113">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="eadcb-114">Les clés de Registre n’ont pas de valeurs par défaut, mais elles peuvent avoir une valeur sans nom, qui peut être de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="eadcb-114">Registry keys do not have default values, but they can have one unnamed value, which can be of any type.</span></span>

</dd> <dt>

<span data-ttu-id="eadcb-115">*dwType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eadcb-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eadcb-116">Type de données vers lequel pointe le paramètre *lpData* .</span><span class="sxs-lookup"><span data-stu-id="eadcb-116">The type of data pointed to by the *lpData* parameter.</span></span> <span data-ttu-id="eadcb-117">Pour obtenir la liste des types possibles, consultez [types de valeurs de Registre](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="eadcb-117">For a list of the possible types, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="eadcb-118">*lpData* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eadcb-118">*lpData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eadcb-119">Données à stocker.</span><span class="sxs-lookup"><span data-stu-id="eadcb-119">The data to be stored.</span></span>

<span data-ttu-id="eadcb-120">Pour les types basés sur une chaîne, tels que REG \_ SZ, la chaîne doit se terminer par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="eadcb-120">For string-based types, such as REG\_SZ, the string must be null-terminated.</span></span> <span data-ttu-id="eadcb-121">Pour le \_ type de données Reg multi- \_ SZ, la chaîne doit se terminer par deux caractères null.</span><span class="sxs-lookup"><span data-stu-id="eadcb-121">For the REG\_MULTI\_SZ data type, the string must be terminated with two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="eadcb-122">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eadcb-122">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eadcb-123">Taille des informations vers lesquelles pointe le paramètre *lpData* , en octets.</span><span class="sxs-lookup"><span data-stu-id="eadcb-123">The size of the information pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="eadcb-124">Si les données sont de type REG \_ SZ, reg \_ expand \_ SZ ou reg \_ \_ multisz, *cbData* doit inclure la taille du ou des caractères null de fin.</span><span class="sxs-lookup"><span data-stu-id="eadcb-124">If the data is of type REG\_SZ, REG\_EXPAND\_SZ, or REG\_MULTI\_SZ, *cbData* must include the size of the terminating null character or characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eadcb-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eadcb-125">Return value</span></span>

<span data-ttu-id="eadcb-126">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="eadcb-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="eadcb-127">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="eadcb-127">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="eadcb-128">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="eadcb-128">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="eadcb-129">Notes</span><span class="sxs-lookup"><span data-stu-id="eadcb-129">Remarks</span></span>

<span data-ttu-id="eadcb-130">Les tailles de valeur sont limitées par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="eadcb-130">Value sizes are limited by available memory.</span></span> <span data-ttu-id="eadcb-131">Les valeurs longues (plus de 2048 octets) doivent être stockées sous forme de fichiers avec les noms de fichiers stockés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="eadcb-131">Long values (more than 2048 bytes) should be stored as files with the file names stored in the registry.</span></span> <span data-ttu-id="eadcb-132">Cela permet au registre de fonctionner efficacement.</span><span class="sxs-lookup"><span data-stu-id="eadcb-132">This helps the registry perform efficiently.</span></span> <span data-ttu-id="eadcb-133">Les éléments d’application, tels que les icônes, les bitmaps et les fichiers exécutables, doivent être stockés en tant que fichiers et ne peuvent pas être placés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="eadcb-133">Application elements such as icons, bitmaps, and executable files should be stored as files and not be placed in the registry.</span></span>

## <a name="requirements"></a><span data-ttu-id="eadcb-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eadcb-134">Requirements</span></span>



| <span data-ttu-id="eadcb-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eadcb-135">Requirement</span></span> | <span data-ttu-id="eadcb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="eadcb-136">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eadcb-137">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="eadcb-137">Redistributable</span></span><br/> | <span data-ttu-id="eadcb-138">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="eadcb-138">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="eadcb-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="eadcb-139">Header</span></span><br/>          | <dl> <span data-ttu-id="eadcb-140"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="eadcb-140"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="eadcb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="eadcb-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="eadcb-142"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eadcb-142"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eadcb-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eadcb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadcb-144">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="eadcb-144">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="eadcb-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="eadcb-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
