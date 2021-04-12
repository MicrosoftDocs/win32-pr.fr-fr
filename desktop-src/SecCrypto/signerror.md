---
description: Appelle la fonction GetLastError et convertit le code de retour en HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: SignError fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7a405bef4666721e485e8b5ad6905209b2244bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034045"
---
# <a name="signerror-function"></a><span data-ttu-id="74269-103">SignError fonction)</span><span class="sxs-lookup"><span data-stu-id="74269-103">SignError function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74269-104">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="74269-104">This API is deprecated.</span></span> <span data-ttu-id="74269-105">Microsoft peut supprimer cette API dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74269-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="74269-106">La fonction **SignError** appelle la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) et convertit le code de retour en **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="74269-106">The **SignError** function calls the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function and converts the return code to an **HRESULT**.</span></span>

> [!Note]  
> <span data-ttu-id="74269-107">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="74269-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="74269-108">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="74269-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="74269-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74269-109">Syntax</span></span>


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a><span data-ttu-id="74269-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74269-110">Parameters</span></span>

<span data-ttu-id="74269-111">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="74269-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74269-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74269-112">Return value</span></span>

<span data-ttu-id="74269-113">Si la méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="74269-113">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="74269-114">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="74269-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="74269-115">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="74269-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74269-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74269-116">Requirements</span></span>



| <span data-ttu-id="74269-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74269-117">Requirement</span></span> | <span data-ttu-id="74269-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="74269-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74269-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74269-119">Minimum supported client</span></span><br/> | <span data-ttu-id="74269-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74269-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="74269-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74269-121">Minimum supported server</span></span><br/> | <span data-ttu-id="74269-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74269-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74269-123">DLL</span><span class="sxs-lookup"><span data-stu-id="74269-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74269-124"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74269-124"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
