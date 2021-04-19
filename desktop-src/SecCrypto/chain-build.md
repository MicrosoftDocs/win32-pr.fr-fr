---
description: Génère une chaîne de vérification de certificat à partir d’un certificat de fin vers le certificat racine approuvé et retourne une valeur booléenne qui indique la validité globale de la chaîne.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'IChain2 :: Build, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537341"
---
# <a name="ichain2build-method"></a><span data-ttu-id="09d7c-103">IChain2 :: Build, méthode</span><span class="sxs-lookup"><span data-stu-id="09d7c-103">IChain2::Build method</span></span>

<span data-ttu-id="09d7c-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="09d7c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="09d7c-105">Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="09d7c-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="09d7c-106">La méthode de **génération** génère une chaîne de vérification de certificat à partir d’un certificat de fin vers le [*certificat racine*](../secgloss/r-gly.md) approuvé et retourne une valeur booléenne qui indique la validité globale de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="09d7c-106">The **Build** method builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md) and returns a Boolean value that indicates the overall validity of the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d7c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09d7c-107">Syntax</span></span>


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="09d7c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09d7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d7c-109">*Certificat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09d7c-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d7c-110">Objet de [**certificat**](certificate.md) qui représente le certificat final sur lequel la chaîne de vérification doit être générée.</span><span class="sxs-lookup"><span data-stu-id="09d7c-110">A [**Certificate**](certificate.md) object that represents the end certificate upon which the verification chain is to be built.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d7c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09d7c-111">Return value</span></span>

<span data-ttu-id="09d7c-112">Valeur booléenne qui indique la validité globale de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="09d7c-112">A Boolean value that indicates the overall validity of the chain.</span></span> <span data-ttu-id="09d7c-113">La validité globale est basée sur la stratégie de vérification de validité en place.</span><span class="sxs-lookup"><span data-stu-id="09d7c-113">Overall validity is based on the validity checking policy in place.</span></span>

## <a name="remarks"></a><span data-ttu-id="09d7c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="09d7c-114">Remarks</span></span>

<span data-ttu-id="09d7c-115">La chaîne est créée à l’aide de la propriété [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) , ainsi que des stratégies d’application et de certificat spécifiées par un objet [**CertificateStatus**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="09d7c-115">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property as well as application and certificate policies specified by a [**CertificateStatus**](certificatestatus.md) object.</span></span> <span data-ttu-id="09d7c-116">La collection retournée est triée ; le premier certificat de la collection, **certificats. Item**(1), est le certificat de fin de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="09d7c-116">The returned collection is ordered; the first certificate in the collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="09d7c-117">Le dernier certificat de la collection, Certificates **. Item**(**Certificates. Count**), est le [*certificat racine*](../secgloss/r-gly.md) de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="09d7c-117">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span> <span data-ttu-id="09d7c-118">**Certificats. Item**(0) représente la chaîne entière.</span><span class="sxs-lookup"><span data-stu-id="09d7c-118">**Certificates.Item**(0) represents the entire chain.</span></span>

<span data-ttu-id="09d7c-119">Chaque fois que la méthode **chain. Build** est appelée, l' [*État*](../secgloss/s-gly.md) de l’objet [**chaîne**](chain.md) est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="09d7c-119">Each time the **Chain.Build** method is called, the [*state*](../secgloss/s-gly.md) of the [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="09d7c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09d7c-120">Requirements</span></span>



| <span data-ttu-id="09d7c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09d7c-121">Requirement</span></span> | <span data-ttu-id="09d7c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="09d7c-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09d7c-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="09d7c-123">End of client support</span></span><br/> | <span data-ttu-id="09d7c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09d7c-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="09d7c-125">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="09d7c-125">End of server support</span></span><br/> | <span data-ttu-id="09d7c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09d7c-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="09d7c-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="09d7c-127">Redistributable</span></span><br/>       | <span data-ttu-id="09d7c-128">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="09d7c-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="09d7c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="09d7c-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="09d7c-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09d7c-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d7c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09d7c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d7c-132">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="09d7c-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="09d7c-133">**Mutation**</span><span class="sxs-lookup"><span data-stu-id="09d7c-133">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
