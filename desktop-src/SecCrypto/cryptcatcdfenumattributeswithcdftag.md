---
description: Énumère les attributs des fichiers membres dans la section CatalogFiles d’un fichier de définition de catalogue (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: CryptCATCDFEnumAttributesWithCDFTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525731"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a><span data-ttu-id="33304-103">CryptCATCDFEnumAttributesWithCDFTag fonction)</span><span class="sxs-lookup"><span data-stu-id="33304-103">CryptCATCDFEnumAttributesWithCDFTag function</span></span>

<span data-ttu-id="33304-104">\[La fonction **CryptCATCDFEnumAttributesWithCDFTag** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="33304-104">\[The **CryptCATCDFEnumAttributesWithCDFTag** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="33304-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="33304-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="33304-106">La fonction **CryptCATCDFEnumAttributesWithCDFTag** énumère les attributs des fichiers membres dans la section **CatalogFiles** d’un fichier de définition de catalogue (CDF).</span><span class="sxs-lookup"><span data-stu-id="33304-106">The **CryptCATCDFEnumAttributesWithCDFTag** function enumerates the attributes of member files in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="33304-107">**CryptCATCDFEnumAttributesWithCDFTag** est appelé par [MakeCat](makecat.md).</span><span class="sxs-lookup"><span data-stu-id="33304-107">**CryptCATCDFEnumAttributesWithCDFTag** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="33304-108">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="33304-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="33304-109">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="33304-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="33304-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33304-110">Syntax</span></span>


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a><span data-ttu-id="33304-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33304-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33304-112">*pCDF* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33304-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33304-113">Pointeur vers une structure [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="33304-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="33304-114">*pwszMemberTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33304-114">*pwszMemberTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33304-115">Pointeur vers une chaîne terminée par le caractère **null** qui identifie le membre du fichier catalogue.</span><span class="sxs-lookup"><span data-stu-id="33304-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="33304-116">*pMember* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33304-116">*pMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33304-117">Pointeur vers une structure [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) qui contient les informations de membre.</span><span class="sxs-lookup"><span data-stu-id="33304-117">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the member information.</span></span>

</dd> <dt>

<span data-ttu-id="33304-118">*pPrevAttr* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33304-118">*pPrevAttr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33304-119">Pointeur vers une structure [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) pour un attribut de membre de fichier dans le CDF désigné par *pCDF*.</span><span class="sxs-lookup"><span data-stu-id="33304-119">A pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure for a file member attribute in the CDF pointed to by *pCDF*.</span></span>

</dd> <dt>

<span data-ttu-id="33304-120">*pfnParseError* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33304-120">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33304-121">Pointeur vers une fonction définie par l’utilisateur pour gérer les erreurs d’analyse de fichier.</span><span class="sxs-lookup"><span data-stu-id="33304-121">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33304-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33304-122">Return value</span></span>

<span data-ttu-id="33304-123">En cas de réussite, cette fonction retourne un pointeur vers une structure [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) .</span><span class="sxs-lookup"><span data-stu-id="33304-123">Upon success, this function returns a pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure.</span></span> <span data-ttu-id="33304-124">La fonction **CryptCATCDFEnumAttributesWithCDFTag** retourne un pointeur **null** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="33304-124">The **CryptCATCDFEnumAttributesWithCDFTag** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="33304-125">Notes</span><span class="sxs-lookup"><span data-stu-id="33304-125">Remarks</span></span>

<span data-ttu-id="33304-126">En général, vous appelez cette fonction dans une boucle pour énumérer tous les attributs de membre de fichier de catalogue dans un CDF.</span><span class="sxs-lookup"><span data-stu-id="33304-126">You typically call this function in a loop to enumerate all of the catalog file member attributes in a CDF.</span></span> <span data-ttu-id="33304-127">Avant d’entrer dans la boucle, affectez à *pPrevAttr* la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="33304-127">Before entering the loop, set *pPrevAttr* to **NULL**.</span></span> <span data-ttu-id="33304-128">La fonction retourne un pointeur vers le premier attribut.</span><span class="sxs-lookup"><span data-stu-id="33304-128">The function returns a pointer to the first attribute.</span></span> <span data-ttu-id="33304-129">Affectez à *pPrevAttr* la valeur de retour de la fonction pour les itérations suivantes de la boucle.</span><span class="sxs-lookup"><span data-stu-id="33304-129">Set *pPrevAttr* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="33304-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="33304-130">Examples</span></span>

<span data-ttu-id="33304-131">L’exemple suivant illustre la séquence correcte des assignations pour le paramètre *pPrevAttr* ( `pAttr` ).</span><span class="sxs-lookup"><span data-stu-id="33304-131">The following example shows the correct sequence of assignments for the *pPrevAttr* parameter (`pAttr`).</span></span>


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="33304-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33304-132">Requirements</span></span>



| <span data-ttu-id="33304-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33304-133">Requirement</span></span> | <span data-ttu-id="33304-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="33304-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33304-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33304-135">Minimum supported client</span></span><br/> | <span data-ttu-id="33304-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33304-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="33304-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33304-137">Minimum supported server</span></span><br/> | <span data-ttu-id="33304-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33304-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="33304-139">DLL</span><span class="sxs-lookup"><span data-stu-id="33304-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33304-140"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33304-140"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33304-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33304-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33304-142">MakeCat</span><span class="sxs-lookup"><span data-stu-id="33304-142">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="33304-143">**CRYPTCATATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="33304-143">**CRYPTCATATTRIBUTE**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[<span data-ttu-id="33304-144">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="33304-144">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="33304-145">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="33304-145">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="33304-146">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="33304-146">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="33304-147">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="33304-147">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
