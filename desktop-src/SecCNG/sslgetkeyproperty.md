---
description: Récupère la valeur d’une propriété nommée pour un objet clé de fournisseur SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: SslGetKeyProperty, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520114"
---
# <a name="sslgetkeyproperty-function"></a><span data-ttu-id="e5c70-103">SslGetKeyProperty fonction)</span><span class="sxs-lookup"><span data-stu-id="e5c70-103">SslGetKeyProperty function</span></span>

<span data-ttu-id="e5c70-104">La fonction **SslGetKeyProperty** récupère la valeur d’une propriété nommée pour un objet de clé de fournisseur SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="e5c70-104">The **SslGetKeyProperty** function retrieves the value of a named property for a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider key object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c70-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5c70-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e5c70-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5c70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c70-107">*HKEY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5c70-107">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c70-108">Handle du fournisseur SSL.</span><span class="sxs-lookup"><span data-stu-id="e5c70-108">The handle of the SSL provider.</span></span>

</dd> <dt>

<span data-ttu-id="e5c70-109">*pszProperty* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5c70-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c70-110">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom de la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e5c70-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span> <span data-ttu-id="e5c70-111">Il peut s’agir de l’un des [**identificateurs de propriété de stockage de clés**](key-storage-property-identifiers.md) prédéfinis ou d’un identificateur de propriété personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e5c70-111">This can be one of the predefined [**Key Storage Property Identifiers**](key-storage-property-identifiers.md) or a custom property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e5c70-112">*ppbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5c70-112">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c70-113">Pointeur vers une mémoire tampon qui reçoit la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="e5c70-113">A pointer to a buffer that receives the property value.</span></span> <span data-ttu-id="e5c70-114">L’appelant de la fonction doit libérer cette mémoire tampon en appelant la fonction [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e5c70-114">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e5c70-115">*pcbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5c70-115">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c70-116">Taille, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="e5c70-116">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e5c70-117">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5c70-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c70-118">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="e5c70-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c70-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5c70-119">Return value</span></span>

<span data-ttu-id="e5c70-120">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e5c70-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="e5c70-121">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e5c70-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="e5c70-122">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="e5c70-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="e5c70-123">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e5c70-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="e5c70-124">Description</span><span class="sxs-lookup"><span data-stu-id="e5c70-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="e5c70-125"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e5c70-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="e5c70-126">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e5c70-126">One of the provided handles is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="e5c70-127"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e5c70-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="e5c70-128">L’un des paramètres fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e5c70-128">One of the supplied parameters is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5c70-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5c70-129">Requirements</span></span>



| <span data-ttu-id="e5c70-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5c70-130">Requirement</span></span> | <span data-ttu-id="e5c70-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5c70-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c70-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5c70-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c70-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5c70-133">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e5c70-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5c70-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c70-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5c70-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e5c70-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5c70-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5c70-137"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c70-137"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="e5c70-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e5c70-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5c70-139"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5c70-139"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

