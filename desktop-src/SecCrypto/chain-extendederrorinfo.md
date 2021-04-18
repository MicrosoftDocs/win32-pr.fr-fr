---
description: Retourne une chaîne qui contient des informations d’erreur supplémentaires sur l’entrée indexée.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'IChain2 :: ExtendedErrorInfo, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522810"
---
# <a name="ichain2extendederrorinfo-method"></a><span data-ttu-id="1d5a0-103">IChain2 :: ExtendedErrorInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="1d5a0-103">IChain2::ExtendedErrorInfo method</span></span>

<span data-ttu-id="1d5a0-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1d5a0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1d5a0-105">Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1d5a0-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1d5a0-106">La méthode **ExtendedErrorInfo** retourne une chaîne qui contient des informations d’erreur supplémentaires sur l’entrée indexée.</span><span class="sxs-lookup"><span data-stu-id="1d5a0-106">The **ExtendedErrorInfo** method returns a string that contains additional error information about the indexed entry.</span></span>

<span data-ttu-id="1d5a0-107">Cette méthode est introduite dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1d5a0-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5a0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d5a0-108">Syntax</span></span>


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1d5a0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d5a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d5a0-110">*Index* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1d5a0-110">*Index* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1d5a0-111">**Valeur de type long** représentant l’index de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="1d5a0-111">A **Long** representing the index of the entry.</span></span> <span data-ttu-id="1d5a0-112">La valeur par défaut est 1, qui retourne des informations d’erreur pour le certificat de fin dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1d5a0-112">The default value is 1, which returns error information for the end certificate in the chain.</span></span> <span data-ttu-id="1d5a0-113">Certificates **. Count** retourne des informations sur le certificat racine de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1d5a0-113">**Certificates.Count** returns information about the root certificate of the chain.</span></span> <span data-ttu-id="1d5a0-114">0 retourne des informations d’erreur étendues pour la chaîne entière.</span><span class="sxs-lookup"><span data-stu-id="1d5a0-114">0 returns extended error information for the entire chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d5a0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d5a0-115">Return value</span></span>

<span data-ttu-id="1d5a0-116">Chaîne qui contient les informations d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="1d5a0-116">A string that contains the extended error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d5a0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d5a0-117">Requirements</span></span>



| <span data-ttu-id="1d5a0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d5a0-118">Requirement</span></span> | <span data-ttu-id="1d5a0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d5a0-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5a0-120">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1d5a0-120">End of client support</span></span><br/> | <span data-ttu-id="1d5a0-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d5a0-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1d5a0-122">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1d5a0-122">End of server support</span></span><br/> | <span data-ttu-id="1d5a0-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d5a0-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1d5a0-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1d5a0-124">Redistributable</span></span><br/>       | <span data-ttu-id="1d5a0-125">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d5a0-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1d5a0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1d5a0-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1d5a0-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d5a0-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d5a0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d5a0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5a0-129">**Mutation**</span><span class="sxs-lookup"><span data-stu-id="1d5a0-129">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
