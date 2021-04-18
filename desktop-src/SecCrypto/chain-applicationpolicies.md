---
description: Retourne une collection d’OID qui représente les OID de stratégie d’application valides pour la chaîne.
ms.assetid: 4e4a7dce-5004-4b80-b132-3cdc0c048cde
title: 'IChain2 :: ApplicationPolicies, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ApplicationPolicies
- IChain2.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a90eb7a493bfe81f5c4a38f773b0307380002b6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526464"
---
# <a name="ichain2applicationpolicies-method"></a><span data-ttu-id="06c88-103">IChain2 :: ApplicationPolicies, méthode</span><span class="sxs-lookup"><span data-stu-id="06c88-103">IChain2::ApplicationPolicies method</span></span>

<span data-ttu-id="06c88-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="06c88-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="06c88-105">Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="06c88-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="06c88-106">La méthode **ApplicationPolicies** retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie d’application valides pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="06c88-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span>

<span data-ttu-id="06c88-107">Cette méthode est introduite dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="06c88-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c88-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06c88-108">Syntax</span></span>


```VB
Chain.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="06c88-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06c88-109">Parameters</span></span>

<span data-ttu-id="06c88-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="06c88-110">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c88-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06c88-111">Requirements</span></span>



| <span data-ttu-id="06c88-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06c88-112">Requirement</span></span> | <span data-ttu-id="06c88-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="06c88-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06c88-114">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="06c88-114">End of client support</span></span><br/> | <span data-ttu-id="06c88-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06c88-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="06c88-116">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="06c88-116">End of server support</span></span><br/> | <span data-ttu-id="06c88-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06c88-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="06c88-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="06c88-118">Redistributable</span></span><br/>       | <span data-ttu-id="06c88-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="06c88-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="06c88-120">DLL</span><span class="sxs-lookup"><span data-stu-id="06c88-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="06c88-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06c88-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
