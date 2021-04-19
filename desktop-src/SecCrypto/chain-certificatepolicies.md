---
description: Retourne une collection d’OID qui représente les OID de stratégie de certificat valides pour la chaîne.
ms.assetid: 18200003-f4f1-4cf3-af9a-bc223151ff68
title: 'IChain2 :: CertificatePolicies, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.CertificatePolicies
- IChain2.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e37abce9ea1aec5eb8adaf1d8eceeb3fac284fa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542214"
---
# <a name="ichain2certificatepolicies-method"></a><span data-ttu-id="e2e6b-103">IChain2 :: CertificatePolicies, méthode</span><span class="sxs-lookup"><span data-stu-id="e2e6b-103">IChain2::CertificatePolicies method</span></span>

<span data-ttu-id="e2e6b-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e2e6b-105">Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e2e6b-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e2e6b-106">La méthode **certificatePolicies** retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie de certificat valides pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e6b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2e6b-107">Syntax</span></span>


```VB
Chain.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="e2e6b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2e6b-108">Parameters</span></span>

<span data-ttu-id="e2e6b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e2e6b-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e6b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2e6b-110">Requirements</span></span>



| <span data-ttu-id="e2e6b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2e6b-111">Requirement</span></span> | <span data-ttu-id="e2e6b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2e6b-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e6b-113">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e2e6b-113">End of client support</span></span><br/> | <span data-ttu-id="e2e6b-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2e6b-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e2e6b-115">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e2e6b-115">End of server support</span></span><br/> | <span data-ttu-id="e2e6b-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2e6b-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e2e6b-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e2e6b-117">Redistributable</span></span><br/>       | <span data-ttu-id="e2e6b-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="e2e6b-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e2e6b-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e2e6b-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e2e6b-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2e6b-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
