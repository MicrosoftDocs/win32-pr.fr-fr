---
description: Enregistre une clé privée et la clé publique correspondante dans un fichier spécifié.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: PvkPrivateKeySave fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523315"
---
# <a name="pvkprivatekeysave-function"></a><span data-ttu-id="fa8da-103">PvkPrivateKeySave fonction)</span><span class="sxs-lookup"><span data-stu-id="fa8da-103">PvkPrivateKeySave function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa8da-104">Cette API est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fa8da-104">This API is deprecated.</span></span> <span data-ttu-id="fa8da-105">Microsoft peut supprimer cette API dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fa8da-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="fa8da-106">La fonction **PvkPrivateKeySave** enregistre une [*clé privée*](../secgloss/p-gly.md) et la [*clé publique*](../secgloss/p-gly.md) correspondante dans un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="fa8da-106">The **PvkPrivateKeySave** function saves a [*private key*](../secgloss/p-gly.md) and its corresponding [*public key*](../secgloss/p-gly.md) to a specified file.</span></span>

> [!Note]  
> <span data-ttu-id="fa8da-107">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="fa8da-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="fa8da-108">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="fa8da-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fa8da-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa8da-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fa8da-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa8da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa8da-111">*hCryptProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8da-111">*hCryptProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8da-112">Handle d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="fa8da-112">A handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="fa8da-113">*hFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8da-113">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8da-114">Handle vers un fichier créé avec l’autorisation de lecture/écriture initiale et l’autorisation en lecture seule ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fa8da-114">A handle to a file created with initial read/write permission and subsequent read-only permission.</span></span>

</dd> <dt>

<span data-ttu-id="fa8da-115">*dwKeySpec* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8da-115">*dwKeySpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8da-116">Entier long pour le type de clé.</span><span class="sxs-lookup"><span data-stu-id="fa8da-116">A long integer for the type of key.</span></span> <span data-ttu-id="fa8da-117">Les valeurs possibles sont notamment **at \_ KeyExchange** ou **at \_ signature**.</span><span class="sxs-lookup"><span data-stu-id="fa8da-117">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa8da-118">*hwndOwner* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8da-118">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8da-119">Si un mot de passe est requis pour chiffrer la clé privée, ce paramètre est un handle vers le parent de la boîte de dialogue ; dans le cas contraire, la **valeur est null**.</span><span class="sxs-lookup"><span data-stu-id="fa8da-119">If a password is required to encrypt the private key, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fa8da-120">*pwszKeyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8da-120">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8da-121">Pointeur vers une chaîne se terminant par un caractère null pour le nom de la clé à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="fa8da-121">A pointer to a null-terminated string for the name of the key to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="fa8da-122">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8da-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8da-123">Valeur **DWORD** qui spécifie des options supplémentaires pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="fa8da-123">A **DWORD** value that specifies additional options for the function.</span></span> <span data-ttu-id="fa8da-124">Pour plus d’informations, consultez le paramètre *dwFlags* dans [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="fa8da-124">For more information, see the *dwFlags* parameter in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa8da-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa8da-125">Return value</span></span>

<span data-ttu-id="fa8da-126">En cas de réussite, cette fonction retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="fa8da-126">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="fa8da-127">La fonction **PvkPrivateKeySave** retourne la **valeur false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="fa8da-127">The **PvkPrivateKeySave** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa8da-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa8da-128">Requirements</span></span>



| <span data-ttu-id="fa8da-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa8da-129">Requirement</span></span> | <span data-ttu-id="fa8da-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa8da-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8da-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa8da-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fa8da-132">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa8da-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fa8da-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa8da-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fa8da-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa8da-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa8da-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fa8da-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa8da-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa8da-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
