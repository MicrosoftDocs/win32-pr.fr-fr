---
description: Énumère les membres de fichier individuels dans la section CatalogFiles d’un fichier de définition de catalogue (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: CryptCATCDFEnumMembersByCDFTagEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525732"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a><span data-ttu-id="1c13a-103">CryptCATCDFEnumMembersByCDFTagEx fonction)</span><span class="sxs-lookup"><span data-stu-id="1c13a-103">CryptCATCDFEnumMembersByCDFTagEx function</span></span>

<span data-ttu-id="1c13a-104">\[La fonction **CryptCATCDFEnumMembersByCDFTagEx** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1c13a-104">\[The **CryptCATCDFEnumMembersByCDFTagEx** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1c13a-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="1c13a-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="1c13a-106">La fonction **CryptCATCDFEnumMembersByCDFTagEx** énumère les membres de fichier individuels dans la section **CatalogFiles** d’un fichier de définition de catalogue (CDF).</span><span class="sxs-lookup"><span data-stu-id="1c13a-106">The **CryptCATCDFEnumMembersByCDFTagEx** function enumerates the individual file members in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="1c13a-107">**CryptCATCDFEnumMembersByCDFTagEx** est appelé par [MakeCat](makecat.md).</span><span class="sxs-lookup"><span data-stu-id="1c13a-107">**CryptCATCDFEnumMembersByCDFTagEx** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="1c13a-108">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="1c13a-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="1c13a-109">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="1c13a-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1c13a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c13a-110">Syntax</span></span>


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="1c13a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c13a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c13a-112">*pCDF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c13a-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c13a-113">Pointeur vers une structure [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="1c13a-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c13a-114">*pwszPrevCDFTag* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1c13a-114">*pwszPrevCDFTag* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c13a-115">Pointeur vers une chaîne terminée par le caractère **null** qui identifie le membre du fichier catalogue.</span><span class="sxs-lookup"><span data-stu-id="1c13a-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="1c13a-116">*pfnParseError* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c13a-116">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c13a-117">Pointeur vers une fonction définie par l’utilisateur pour gérer les erreurs d’analyse de fichier.</span><span class="sxs-lookup"><span data-stu-id="1c13a-117">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> <dt>

<span data-ttu-id="1c13a-118">*ppMember* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c13a-118">*ppMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c13a-119">Pointeur vers une structure [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) qui contient les informations relatives au membre de fichier.</span><span class="sxs-lookup"><span data-stu-id="1c13a-119">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the file member information.</span></span>

</dd> <dt>

<span data-ttu-id="1c13a-120">*fContinueOnError* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c13a-120">*fContinueOnError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c13a-121">Valeur qui spécifie s’il faut conserver en mémoire une référence au dernier membre énuméré.</span><span class="sxs-lookup"><span data-stu-id="1c13a-121">A value that specifies whether to keep in memory a reference to the last enumerated member.</span></span>

</dd> <dt>

<span data-ttu-id="1c13a-122">*pvReserved* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c13a-122">*pvReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c13a-123">Ce paramètre est réservé. ne l’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="1c13a-123">This parameter is reserved; do not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c13a-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c13a-124">Return value</span></span>

<span data-ttu-id="1c13a-125">En cas de réussite, cette fonction retourne un pointeur vers une chaîne se terminant par un caractère **null** qui identifie un membre de fichier dans la section **CATALOGFILES** d’un CDF.</span><span class="sxs-lookup"><span data-stu-id="1c13a-125">Upon success, this function returns a pointer to a **null**-terminated string that identifies a file member in the **CatalogFiles** section of a CDF.</span></span> <span data-ttu-id="1c13a-126">La fonction **CryptCATCDFEnumMembersByCDFTagEx** retourne un pointeur **null** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="1c13a-126">The **CryptCATCDFEnumMembersByCDFTagEx** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c13a-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1c13a-127">Remarks</span></span>

<span data-ttu-id="1c13a-128">En général, vous appelez cette fonction dans une boucle pour énumérer tous les membres du fichier catalogue dans un CDF.</span><span class="sxs-lookup"><span data-stu-id="1c13a-128">You typically call this function in a loop to enumerate all of the catalog file members in a CDF.</span></span> <span data-ttu-id="1c13a-129">Avant d’entrer dans la boucle, affectez à *pwszPrevCDFTag* la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1c13a-129">Before entering the loop, set *pwszPrevCDFTag* to **NULL**.</span></span> <span data-ttu-id="1c13a-130">La fonction retourne un pointeur vers le premier membre.</span><span class="sxs-lookup"><span data-stu-id="1c13a-130">The function returns a pointer to the first member.</span></span> <span data-ttu-id="1c13a-131">Affectez à *pwszPrevCDFTag* la valeur de retour de la fonction pour les itérations suivantes de la boucle.</span><span class="sxs-lookup"><span data-stu-id="1c13a-131">Set *pwszPrevCDFTag* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="1c13a-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="1c13a-132">Examples</span></span>

<span data-ttu-id="1c13a-133">L’exemple suivant illustre la séquence correcte des assignations pour le paramètre *pwszPrevCDFTag* ( `pwszMemberTag` ).</span><span class="sxs-lookup"><span data-stu-id="1c13a-133">The following example shows the correct sequence of assignments for the *pwszPrevCDFTag* parameter (`pwszMemberTag`).</span></span>


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="1c13a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c13a-134">Requirements</span></span>



| <span data-ttu-id="1c13a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c13a-135">Requirement</span></span> | <span data-ttu-id="1c13a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c13a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c13a-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c13a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1c13a-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c13a-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1c13a-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c13a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1c13a-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c13a-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c13a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1c13a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c13a-142"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c13a-142"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c13a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c13a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c13a-144">MakeCat</span><span class="sxs-lookup"><span data-stu-id="1c13a-144">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="1c13a-145">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="1c13a-145">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="1c13a-146">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="1c13a-146">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="1c13a-147">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="1c13a-147">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="1c13a-148">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="1c13a-148">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
