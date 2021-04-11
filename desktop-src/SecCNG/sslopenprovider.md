---
description: Ouvre un handle vers le fournisseur de protocole SSL (SSL (Secure Sockets Layer) Protocol) spécifié.
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: SslOpenProvider, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201355"
---
# <a name="sslopenprovider-function"></a><span data-ttu-id="06281-103">SslOpenProvider fonction)</span><span class="sxs-lookup"><span data-stu-id="06281-103">SslOpenProvider function</span></span>

<span data-ttu-id="06281-104">La fonction **SslOpenProvider** ouvre un handle pour le fournisseur de protocole SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ) spécifié.</span><span class="sxs-lookup"><span data-stu-id="06281-104">The **SslOpenProvider** function opens a handle to the specified [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="06281-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06281-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="06281-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06281-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06281-107">*phSslProvider* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="06281-107">*phSslProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06281-108">Adresse d’un **handle NCRYPT \_ Prov \_** dans lequel écrire le descripteur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="06281-108">The address of an **NCRYPT\_PROV\_HANDLE** in which to write the provider handle.</span></span>

<span data-ttu-id="06281-109">Lorsque vous avez fini d’utiliser le descripteur, vous devez le libérer en appelant la fonction [**SslFreeObject**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="06281-109">When you have finished using the handle, you should free it by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="06281-110">*pszProviderName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06281-110">*pszProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06281-111">Pointeur vers une chaîne Unicode qui contient le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="06281-111">A pointer to a Unicode string that contains the provider name.</span></span> <span data-ttu-id="06281-112">Si la valeur de ce paramètre est **null**, un descripteur **du \_ \_ fournisseur MS Schannel** est retourné.</span><span class="sxs-lookup"><span data-stu-id="06281-112">If the value of this parameter is **NULL**, a handle to the **MS\_SCHANNEL\_PROVIDER** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="06281-113">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06281-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06281-114">Ce paramètre est réservé à une utilisation ultérieure et doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="06281-114">This parameter is reserved for future use, and it must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06281-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06281-115">Return value</span></span>

<span data-ttu-id="06281-116">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="06281-116">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="06281-117">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="06281-117">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="06281-118">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="06281-118">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="06281-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="06281-119">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="06281-120">Description</span><span class="sxs-lookup"><span data-stu-id="06281-120">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06281-121"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="06281-121"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="06281-122">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="06281-122">One of the provided handles is not valid.</span></span><br/>                      |
| <dl> <span data-ttu-id="06281-123"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="06281-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="06281-124">Le paramètre *phSslProvider* ou *PpProviderList* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="06281-124">The *phSslProvider* or *ppProviderList* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="06281-125"><dt>**État \_ AUCUNE \_ mémoire**</dt> <dt>0xC0000017L</dt></span><span class="sxs-lookup"><span data-stu-id="06281-125"><dt>**STATUS\_NO\_MEMORY**</dt> <dt>0xC0000017L</dt></span></span> </dl>      | <span data-ttu-id="06281-126">La mémoire disponible est insuffisante pour allouer les tampons nécessaires.</span><span class="sxs-lookup"><span data-stu-id="06281-126">Not enough memory is available to allocate necessary buffers.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="06281-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06281-127">Requirements</span></span>



| <span data-ttu-id="06281-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06281-128">Requirement</span></span> | <span data-ttu-id="06281-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="06281-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06281-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06281-130">Minimum supported client</span></span><br/> | <span data-ttu-id="06281-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06281-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06281-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06281-132">Minimum supported server</span></span><br/> | <span data-ttu-id="06281-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06281-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="06281-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="06281-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="06281-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="06281-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="06281-136">DLL</span><span class="sxs-lookup"><span data-stu-id="06281-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06281-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06281-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

