---
description: La propriété Certificates récupère une collection de certificats qui représente les certificats dans la chaîne. Il s’agit de la propriété par défaut.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'IChain2 :: Certificates, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528085"
---
# <a name="ichain2certificates-property"></a><span data-ttu-id="aaad9-104">IChain2 :: Certificates, propriété</span><span class="sxs-lookup"><span data-stu-id="aaad9-104">IChain2::Certificates property</span></span>

<span data-ttu-id="aaad9-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aaad9-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="aaad9-106">Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="aaad9-106">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="aaad9-107">La propriété **Certificates** récupère une collection de [**certificats**](certificates.md) qui représente les certificats dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="aaad9-107">The **Certificates** property retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="aaad9-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="aaad9-108">This is the default property.</span></span>

<span data-ttu-id="aaad9-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aaad9-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaad9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaad9-110">Syntax</span></span>


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="aaad9-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="aaad9-111">Property value</span></span>

<span data-ttu-id="aaad9-112">Collection de [**certificats**](certificates.md) utilisée pour récupérer des informations sur chaque certificat dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="aaad9-112">A [**Certificates**](certificates.md) collection that is used to retrieve information about each certificate in the chain.</span></span> <span data-ttu-id="aaad9-113">Le premier certificat de la collection retournée, Certificates **. Item**(1), est le certificat de fin de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="aaad9-113">The first certificate in the returned collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="aaad9-114">Le dernier certificat de la collection, Certificates **. Item**(**Certificates. Count**), est le [*certificat racine*](../secgloss/r-gly.md) de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="aaad9-114">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaad9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaad9-115">Requirements</span></span>



| <span data-ttu-id="aaad9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaad9-116">Requirement</span></span> | <span data-ttu-id="aaad9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaad9-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaad9-118">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="aaad9-118">End of client support</span></span><br/> | <span data-ttu-id="aaad9-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aaad9-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aaad9-120">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="aaad9-120">End of server support</span></span><br/> | <span data-ttu-id="aaad9-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aaad9-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aaad9-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="aaad9-122">Redistributable</span></span><br/>       | <span data-ttu-id="aaad9-123">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="aaad9-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aaad9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="aaad9-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="aaad9-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaad9-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
