---
description: Vérifie la signature d’un fichier signé et obtient la valeur de hachage et l’identificateur d’algorithme pour le fichier.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: WTHelperGetFileHash fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952111"
---
# <a name="wthelpergetfilehash-function"></a><span data-ttu-id="e10dd-103">WTHelperGetFileHash fonction)</span><span class="sxs-lookup"><span data-stu-id="e10dd-103">WTHelperGetFileHash function</span></span>

<span data-ttu-id="e10dd-104">\[La fonction **WTHelperGetFileHash** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e10dd-104">\[The **WTHelperGetFileHash** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e10dd-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="e10dd-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="e10dd-106">La fonction **WTHelperGetFileHash** vérifie la signature d’un fichier signé et obtient la valeur de hachage et l’identificateur d’algorithme pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="e10dd-106">The **WTHelperGetFileHash** function verifies the signature of a signed file and obtains the hash value and algorithm identifier for the file.</span></span>

> [!Note]  
> <span data-ttu-id="e10dd-107">Cette fonction n’est pas déclarée dans un fichier d’en-tête publié.</span><span class="sxs-lookup"><span data-stu-id="e10dd-107">This function is not declared in a published header file.</span></span> <span data-ttu-id="e10dd-108">Pour utiliser cette fonction, déclarez-la dans le format exact indiqué.</span><span class="sxs-lookup"><span data-stu-id="e10dd-108">To use this function, declare it in the exact format shown.</span></span> <span data-ttu-id="e10dd-109">Cette fonction n’a pas non plus de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="e10dd-109">This function also has no associated import library.</span></span> <span data-ttu-id="e10dd-110">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Wintrust.dll.</span><span class="sxs-lookup"><span data-stu-id="e10dd-110">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e10dd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e10dd-111">Syntax</span></span>


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a><span data-ttu-id="e10dd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e10dd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10dd-113">*pwszFilename* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e10dd-113">*pwszFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10dd-114">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le chemin d’accès et le nom de fichier du fichier pour lequel obtenir le hachage.</span><span class="sxs-lookup"><span data-stu-id="e10dd-114">A pointer to a null-terminated Unicode string that contains the path and file name of the file to get the hash for.</span></span>

</dd> <dt>

<span data-ttu-id="e10dd-115">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e10dd-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10dd-116">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e10dd-116">This parameter is not used and should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e10dd-117">*pvReserved* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e10dd-117">*pvReserved* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e10dd-118">Ce paramètre n’est pas utilisé et doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e10dd-118">This parameter is not used and should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e10dd-119">*pbFileHash* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e10dd-119">*pbFileHash* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e10dd-120">Pointeur vers une mémoire tampon destinée à recevoir la valeur de hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="e10dd-120">A pointer to a buffer to receive the hash value for the file.</span></span> <span data-ttu-id="e10dd-121">Le paramètre *pcbFileHash* contient la taille de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e10dd-121">The *pcbFileHash* parameter contains the size of this buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e10dd-122">*pcbFileHash* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e10dd-122">*pcbFileHash* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e10dd-123">Pointeur vers une variable **DWORD** qui, en entrée, contient la taille, en octets, de la mémoire tampon *pbFileHash* et, à la sortie, reçoit la taille, en octets, de la valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="e10dd-123">A pointer to a **DWORD** variable that, on input, contains the size, in bytes, of the *pbFileHash* buffer and, on output, receives the size, in bytes, of the hash value.</span></span>

<span data-ttu-id="e10dd-124">Pour obtenir la taille requise de la valeur de hachage, transmettez la valeur **null** pour le paramètre *pbFileHash* .</span><span class="sxs-lookup"><span data-stu-id="e10dd-124">To obtain the required size of the hash value, pass **NULL** for the *pbFileHash* parameter.</span></span> <span data-ttu-id="e10dd-125">Cette fonction place la taille requise, en octets, de la valeur de hachage à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="e10dd-125">This function will place the required size, in bytes, of the hash value in this location.</span></span>

<span data-ttu-id="e10dd-126">Si le paramètre *pbFileHash* n’est pas **null** et que la taille n’est pas assez grande pour recevoir la valeur de hachage, cette fonction placera la taille requise, en octets, à cet emplacement et retournera l' **erreur plus de \_ \_ données**.</span><span class="sxs-lookup"><span data-stu-id="e10dd-126">If the *pbFileHash* parameter is not **NULL**, and the size is not large enough to receive the hash value, this function will place the required size, in bytes, in this location and return **ERROR\_MORE\_DATA**.</span></span>

</dd> <dt>

<span data-ttu-id="e10dd-127">*pHashAlgid* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e10dd-127">*pHashAlgid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e10dd-128">Pointeur vers une variable [**d' \_ ID ALG**](alg-id.md) pour recevoir l’identificateur de l’algorithme utilisé pour créer la valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="e10dd-128">A pointer to an [**ALG\_ID**](alg-id.md) variable to receive the identifier of the algorithm used to create the hash value.</span></span> <span data-ttu-id="e10dd-129">Ce paramètre peut avoir la **valeur null** si cette information n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e10dd-129">This parameter can be **NULL** if this information is not needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10dd-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e10dd-130">Return value</span></span>

<span data-ttu-id="e10dd-131">Retourne un code d’État qui indique la réussite ou l’échec de la fonction.</span><span class="sxs-lookup"><span data-stu-id="e10dd-131">Returns a status code that indicates the success or failure of the function.</span></span>

<span data-ttu-id="e10dd-132">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="e10dd-132">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="e10dd-133">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e10dd-133">Return code</span></span>                                                                                               | <span data-ttu-id="e10dd-134">Description</span><span class="sxs-lookup"><span data-stu-id="e10dd-134">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e10dd-135"><dt>**ERREUR de \_ réussite**</dt></span><span class="sxs-lookup"><span data-stu-id="e10dd-135"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>             | <span data-ttu-id="e10dd-136">Le fichier est signé et la signature a été vérifiée.</span><span class="sxs-lookup"><span data-stu-id="e10dd-136">The file is signed, and the signature was verified.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="e10dd-137"><dt>**ERREUR \_ plus de \_ données**</dt></span><span class="sxs-lookup"><span data-stu-id="e10dd-137"><dt>**ERROR\_MORE\_DATA**</dt></span></span> </dl>          | <span data-ttu-id="e10dd-138">Le paramètre *pbFileHash* n’est pas **null**, et la taille spécifiée par le paramètre *pcbFileHash* n’est pas assez grande pour recevoir le hachage.</span><span class="sxs-lookup"><span data-stu-id="e10dd-138">The *pbFileHash* parameter is not **NULL**, and the size specified by the *pcbFileHash* parameter is not large enough to receive the hash.</span></span><br/> |
| <dl> <span data-ttu-id="e10dd-139"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e10dd-139"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="e10dd-140">Un échec d’allocation de mémoire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="e10dd-140">A memory allocation failure occurred.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="e10dd-141"><dt>**CONFIANCE \_ E \_ condensé incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e10dd-141"><dt>**TRUST\_E\_BAD\_DIGEST**</dt></span></span> </dl>      | <span data-ttu-id="e10dd-142">La signature du fichier n’a pas été vérifiée.</span><span class="sxs-lookup"><span data-stu-id="e10dd-142">The signature of the file was not verified.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="e10dd-143"><dt>**APPROUVER \_ E \_ NoSignature**</dt></span><span class="sxs-lookup"><span data-stu-id="e10dd-143"><dt>**TRUST\_E\_NOSIGNATURE**</dt></span></span> </dl>      | <span data-ttu-id="e10dd-144">Le fichier n’a pas été signé ou a une signature qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e10dd-144">The file was not signed or had a signature that is not valid.</span></span><br/>                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="e10dd-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e10dd-145">Requirements</span></span>



| <span data-ttu-id="e10dd-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e10dd-146">Requirement</span></span> | <span data-ttu-id="e10dd-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="e10dd-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e10dd-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e10dd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e10dd-149">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e10dd-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e10dd-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e10dd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e10dd-151">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e10dd-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e10dd-152">DLL</span><span class="sxs-lookup"><span data-stu-id="e10dd-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e10dd-153"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e10dd-153"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
