---
description: Définit ou récupère l’option de certificat du signataire.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Signer. options, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529912"
---
# <a name="signeroptions-property"></a><span data-ttu-id="305ff-103">Signer. options, propriété</span><span class="sxs-lookup"><span data-stu-id="305ff-103">Signer.Options property</span></span>

<span data-ttu-id="305ff-104">\[La propriété **options** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="305ff-104">\[The **Options** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="305ff-105">Utilisez plutôt la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="305ff-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="305ff-106">La propriété **options** définit ou récupère l’option de certificat du signataire.</span><span class="sxs-lookup"><span data-stu-id="305ff-106">The **Options** property sets or retrieves the signer's certificate option.</span></span>

<span data-ttu-id="305ff-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="305ff-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="305ff-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="305ff-108">Syntax</span></span>


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a><span data-ttu-id="305ff-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="305ff-109">Property value</span></span>

<span data-ttu-id="305ff-110">La valeur du [**\_ certificat CAPICOM \_ inclut \_**](capicom-certificate-include-option.md) l’énumération d’option qui spécifie l’option de certificat du signataire.</span><span class="sxs-lookup"><span data-stu-id="305ff-110">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies the signer's certificate option.</span></span> <span data-ttu-id="305ff-111">La valeur par défaut est le \_ certificat CAPICOM \_ \_ chaîne \_ , à l’exception de la \_ racine.</span><span class="sxs-lookup"><span data-stu-id="305ff-111">The default value is CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT.</span></span> <span data-ttu-id="305ff-112">Le tableau suivant répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="305ff-112">The following table shows the possible values.</span></span>



| <span data-ttu-id="305ff-113">Value</span><span class="sxs-lookup"><span data-stu-id="305ff-113">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="305ff-114">Signification</span><span class="sxs-lookup"><span data-stu-id="305ff-114">Meaning</span></span>                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="305ff-115"><dt>**le certificat CAPICOM \_ \_ inclut une \_ chaîne \_ à l’exception \_ de la racine**</dt></span><span class="sxs-lookup"><span data-stu-id="305ff-115"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="305ff-116">Enregistre tous les certificats de la chaîne à l’exception de l’entité racine.</span><span class="sxs-lookup"><span data-stu-id="305ff-116">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="305ff-117"><dt>**le certificat CAPICOM \_ \_ inclut une \_ \_ chaîne entière**</dt></span><span class="sxs-lookup"><span data-stu-id="305ff-117"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="305ff-118">Enregistre la totalité de la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="305ff-118">Saves the complete certificate chain.</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="305ff-119"><dt>**le certificat CAPICOM \_ \_ inclut \_ uniquement l' \_ entité \_ end**</dt></span><span class="sxs-lookup"><span data-stu-id="305ff-119"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="305ff-120">Enregistre uniquement le certificat d’entité finale.</span><span class="sxs-lookup"><span data-stu-id="305ff-120">Saves only the end entity certificate.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="305ff-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="305ff-121">Requirements</span></span>



| <span data-ttu-id="305ff-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="305ff-122">Requirement</span></span> | <span data-ttu-id="305ff-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="305ff-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="305ff-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="305ff-124">Redistributable</span></span><br/> | <span data-ttu-id="305ff-125">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="305ff-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="305ff-126">DLL</span><span class="sxs-lookup"><span data-stu-id="305ff-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="305ff-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="305ff-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="305ff-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="305ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="305ff-129">**Signataire**</span><span class="sxs-lookup"><span data-stu-id="305ff-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
