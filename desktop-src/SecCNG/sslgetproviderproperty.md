---
description: Récupère la valeur d’une propriété de fournisseur spécifiée.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: SslGetProviderProperty, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867666"
---
# <a name="sslgetproviderproperty-function"></a><span data-ttu-id="083a6-103">SslGetProviderProperty fonction)</span><span class="sxs-lookup"><span data-stu-id="083a6-103">SslGetProviderProperty function</span></span>

<span data-ttu-id="083a6-104">La fonction **SslGetProviderProperty** récupère la valeur d’une propriété de fournisseur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="083a6-104">The **SslGetProviderProperty** function retrieves the value of a specified provider property.</span></span>

## <a name="syntax"></a><span data-ttu-id="083a6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="083a6-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="083a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="083a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="083a6-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="083a6-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083a6-108">Handle du fournisseur SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ) pour lequel la propriété doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="083a6-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider for which to retrieve the property.</span></span>

</dd> <dt>

<span data-ttu-id="083a6-109">*pszProperty* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="083a6-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083a6-110">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom de la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="083a6-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="083a6-111">*ppbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="083a6-111">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="083a6-112">Adresse d’une mémoire tampon qui reçoit la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="083a6-112">The address of a buffer that receives the property value.</span></span>

<span data-ttu-id="083a6-113">L’appelant de la fonction doit libérer cette mémoire tampon en appelant la fonction [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="083a6-113">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="083a6-114">*pcbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="083a6-114">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="083a6-115">Taille, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="083a6-115">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="083a6-116">*ppEnumState* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="083a6-116">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="083a6-117">Adresse d’un pointeur **void** qui reçoit les informations d’état d’énumération utilisées dans les appels ultérieurs à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="083a6-117">The address of a **VOID** pointer that receives enumeration state information that is used in subsequent calls to this function.</span></span> <span data-ttu-id="083a6-118">Ces informations n’ont qu’une signification pour le fournisseur SSL et sont opaques pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="083a6-118">This information only has meaning to the SSL provider and is opaque to the caller.</span></span> <span data-ttu-id="083a6-119">Le fournisseur SSL utilise ces informations pour déterminer l’élément qui est ensuite dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="083a6-119">The SSL provider uses this information to determine which item is next in the enumeration.</span></span> <span data-ttu-id="083a6-120">Si la variable vers laquelle pointe ce paramètre contient la **valeur null**, l’énumération est démarrée à partir du début.</span><span class="sxs-lookup"><span data-stu-id="083a6-120">If the variable pointed to by this parameter contains **NULL**, the enumeration is started from the beginning.</span></span>

<span data-ttu-id="083a6-121">L’appelant de la fonction doit libérer cette mémoire en appelant la fonction [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="083a6-121">The caller of the function must free this memory by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="083a6-122">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="083a6-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083a6-123">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="083a6-123">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="083a6-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="083a6-124">Return value</span></span>

<span data-ttu-id="083a6-125">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="083a6-125">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="083a6-126">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="083a6-126">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="083a6-127">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="083a6-127">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="083a6-128">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="083a6-128">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="083a6-129">Description</span><span class="sxs-lookup"><span data-stu-id="083a6-129">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="083a6-130"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="083a6-130"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="083a6-131">La mémoire disponible est insuffisante pour allouer les tampons nécessaires.</span><span class="sxs-lookup"><span data-stu-id="083a6-131">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="083a6-132"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="083a6-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="083a6-133">Le descripteur *hSslProvider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="083a6-133">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="083a6-134"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="083a6-134"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="083a6-135">L’un des paramètres fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="083a6-135">One of the supplied parameters is not valid.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="083a6-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="083a6-136">Requirements</span></span>



| <span data-ttu-id="083a6-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="083a6-137">Requirement</span></span> | <span data-ttu-id="083a6-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="083a6-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="083a6-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="083a6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="083a6-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="083a6-140">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="083a6-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="083a6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="083a6-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="083a6-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="083a6-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="083a6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="083a6-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="083a6-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="083a6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="083a6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="083a6-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="083a6-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

