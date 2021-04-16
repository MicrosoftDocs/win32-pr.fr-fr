---
title: TF_InvalidAssemblyListCacheIfExist fonction)
description: La \_ fonction TF InvalidAssemblyListCacheIfExist invalide le cache de description du processeur d’entrée de texte.
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- Infrastructure des services de texte de fonction TF_InvalidAssemblyListCacheIfExist
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dd28ab2247fae28af1c5f322832aebe071fab4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508437"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a><span data-ttu-id="36bce-104">TF \_ InvalidAssemblyListCacheIfExist fonction)</span><span class="sxs-lookup"><span data-stu-id="36bce-104">TF\_InvalidAssemblyListCacheIfExist function</span></span>

<span data-ttu-id="36bce-105">La fonction **tf \_ InvalidAssemblyListCacheIfExist** invalide le cache de description du processeur d’entrée de texte.</span><span class="sxs-lookup"><span data-stu-id="36bce-105">The **TF\_InvalidAssemblyListCacheIfExist** function invalidates the text input processor's description cache.</span></span> <span data-ttu-id="36bce-106">Il n’est pas nécessaire d’appeler cette fonction si le programme d’installation du processeur d’entrée requiert un redémarrage ou une ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="36bce-106">It is not necessary to call this function if the input processor setup program requires you to restart or log on.</span></span> <span data-ttu-id="36bce-107">Le cache est valide jusqu’à ce que l’utilisateur se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="36bce-107">The cache is valid until the user logs off.</span></span>

## <a name="syntax"></a><span data-ttu-id="36bce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36bce-108">Syntax</span></span>


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a><span data-ttu-id="36bce-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36bce-109">Parameters</span></span>

<span data-ttu-id="36bce-110">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="36bce-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36bce-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36bce-111">Return value</span></span>

<span data-ttu-id="36bce-112">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="36bce-112">This function can return one of these values.</span></span>



| <span data-ttu-id="36bce-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="36bce-113">Return code</span></span>                                                                            | <span data-ttu-id="36bce-114">Description</span><span class="sxs-lookup"><span data-stu-id="36bce-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="36bce-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="36bce-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="36bce-116">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="36bce-116">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="36bce-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="36bce-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="36bce-118">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="36bce-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="36bce-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="36bce-119">Examples</span></span>

<span data-ttu-id="36bce-120">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="36bce-120">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="36bce-121">L’exemple suivant montre comment obtenir un pointeur vers cette fonction.</span><span class="sxs-lookup"><span data-stu-id="36bce-121">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="36bce-122">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="36bce-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="36bce-123">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="36bce-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a><span data-ttu-id="36bce-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36bce-124">Requirements</span></span>



| <span data-ttu-id="36bce-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36bce-125">Requirement</span></span> | <span data-ttu-id="36bce-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="36bce-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="36bce-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36bce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="36bce-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36bce-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="36bce-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36bce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="36bce-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36bce-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="36bce-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="36bce-131">Redistributable</span></span><br/>          | <span data-ttu-id="36bce-132">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="36bce-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="36bce-133">DLL</span><span class="sxs-lookup"><span data-stu-id="36bce-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36bce-134"><dt>Msctf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36bce-134"><dt>Msctf.dll</dt></span></span> </dl> |



 

