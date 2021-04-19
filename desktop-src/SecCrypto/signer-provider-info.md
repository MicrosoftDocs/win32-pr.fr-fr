---
description: Spécifie les informations du fournisseur de services de chiffrement (CSP) et de la clé privée utilisées pour créer une signature numérique.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: Structure SIGNER_PROVIDER_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521109"
---
# <a name="signer_provider_info-structure"></a><span data-ttu-id="931a8-103">Structure d' \_ informations du fournisseur de signataires \_</span><span class="sxs-lookup"><span data-stu-id="931a8-103">SIGNER\_PROVIDER\_INFO structure</span></span>

<span data-ttu-id="931a8-104">La structure d' **\_ \_ informations du fournisseur de signataires** spécifie le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et les informations de clé privée utilisés pour créer une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="931a8-104">The **SIGNER\_PROVIDER\_INFO** structure specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="931a8-105">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="931a8-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="931a8-106">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="931a8-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="931a8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="931a8-107">Syntax</span></span>


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a><span data-ttu-id="931a8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="931a8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="931a8-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="931a8-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="931a8-110">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="931a8-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="931a8-111">**pwszProviderName**</span><span class="sxs-lookup"><span data-stu-id="931a8-111">**pwszProviderName**</span></span>
</dt> <dd>

<span data-ttu-id="931a8-112">Nom du fournisseur de services de chiffrement utilisé pour créer la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="931a8-112">The name of the CSP used to create the digital signature.</span></span> <span data-ttu-id="931a8-113">Si la valeur de ce membre est **null**, le fournisseur par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="931a8-113">If the value of this member is **NULL**, the default provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="931a8-114">**dwProviderType**</span><span class="sxs-lookup"><span data-stu-id="931a8-114">**dwProviderType**</span></span>
</dt> <dd>

<span data-ttu-id="931a8-115">Type du fournisseur de services de chiffrement spécifié par le membre **pwszProviderName** .</span><span class="sxs-lookup"><span data-stu-id="931a8-115">The type of the CSP specified by the **pwszProviderName** member.</span></span>

</dd> <dt>

<span data-ttu-id="931a8-116">**dwKeySpec**</span><span class="sxs-lookup"><span data-stu-id="931a8-116">**dwKeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="931a8-117">Spécification de la clé.</span><span class="sxs-lookup"><span data-stu-id="931a8-117">The key specification.</span></span> <span data-ttu-id="931a8-118">Si ce membre a la valeur zéro, la spécification de clé dans le membre **pwszPvkFileName** ou **pwszKeyContainer** est utilisée.</span><span class="sxs-lookup"><span data-stu-id="931a8-118">If this member is set to zero, the key specification in the **pwszPvkFileName** or **pwszKeyContainer** member is used.</span></span> <span data-ttu-id="931a8-119">S’il existe plus d’une spécification de clé dans le membre **pwszKeyContainer** , **at \_ signature** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="931a8-119">If there is more than one key specification in the **pwszKeyContainer** member, **AT\_SIGNATURE** is used.</span></span> <span data-ttu-id="931a8-120">En cas d’échec, à l’utilisation **de \_ KeyExchange** .</span><span class="sxs-lookup"><span data-stu-id="931a8-120">If it fails, **AT\_KEYEXCHANGE** is used.</span></span>

</dd> <dt>

<span data-ttu-id="931a8-121">**dwPvkChoice**</span><span class="sxs-lookup"><span data-stu-id="931a8-121">**dwPvkChoice**</span></span>
</dt> <dd>

<span data-ttu-id="931a8-122">Spécifie le type d’informations de clé privée.</span><span class="sxs-lookup"><span data-stu-id="931a8-122">Specifies the type of private key information.</span></span> <span data-ttu-id="931a8-123">Ce membre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="931a8-123">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="931a8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="931a8-124">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="931a8-125">Signification</span><span class="sxs-lookup"><span data-stu-id="931a8-125">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <span data-ttu-id="931a8-126"><dt>**Pvk \_ TAPEZ \_ le \_ nom de fichier**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="931a8-126"><dt>**PVK\_TYPE\_FILE\_NAME**</dt> <dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="931a8-127">Les informations de la clé privée sont un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="931a8-127">The private key information is a file name.</span></span><br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <span data-ttu-id="931a8-128"><dt>**Pvk \_ TAPEZ \_ keycontainer**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="931a8-128"><dt>**PVK\_TYPE\_KEYCONTAINER**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="931a8-129">Les informations de la clé privée sont un conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="931a8-129">The private key information is a key container.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="931a8-130">**pwszPvkFileName**</span><span class="sxs-lookup"><span data-stu-id="931a8-130">**pwszPvkFileName**</span></span>
</dt> <dd>

<span data-ttu-id="931a8-131">Nom du fichier qui contient les informations sur la clé privée.</span><span class="sxs-lookup"><span data-stu-id="931a8-131">The name of the file that contains the private key information.</span></span>

</dd> <dt>

<span data-ttu-id="931a8-132">**pwszKeyContainer**</span><span class="sxs-lookup"><span data-stu-id="931a8-132">**pwszKeyContainer**</span></span>
</dt> <dd>

<span data-ttu-id="931a8-133">Nom du conteneur de clé qui contient les informations sur la clé privée.</span><span class="sxs-lookup"><span data-stu-id="931a8-133">The name of the key container that contains the private key information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="931a8-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="931a8-134">Requirements</span></span>



| <span data-ttu-id="931a8-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="931a8-135">Requirement</span></span> | <span data-ttu-id="931a8-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="931a8-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="931a8-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="931a8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="931a8-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="931a8-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="931a8-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="931a8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="931a8-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="931a8-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="931a8-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="931a8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="931a8-142">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="931a8-142">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="931a8-143">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="931a8-143">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
