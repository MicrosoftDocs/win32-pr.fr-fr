---
description: La propriété algorithme récupère l’objet OID qui identifie l’algorithme utilisé par la clé publique. Il s’agit de la propriété par défaut.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: PublicKey. Algorithm, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528854"
---
# <a name="publickeyalgorithm-property"></a><span data-ttu-id="b99ae-104">PublicKey. Algorithm, propriété</span><span class="sxs-lookup"><span data-stu-id="b99ae-104">PublicKey.Algorithm property</span></span>

<span data-ttu-id="b99ae-105">\[La propriété **algorithme** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="b99ae-105">\[The **Algorithm** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b99ae-106">Utilisez plutôt la [**propriété X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b99ae-106">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b99ae-107">La propriété **algorithme** récupère l’objet [**OID**](oid.md) qui identifie l’algorithme utilisé par la clé publique.</span><span class="sxs-lookup"><span data-stu-id="b99ae-107">The **Algorithm** property retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="b99ae-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="b99ae-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b99ae-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b99ae-109">Syntax</span></span>


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a><span data-ttu-id="b99ae-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b99ae-110">Property value</span></span>

<span data-ttu-id="b99ae-111">Objet [**OID**](oid.md) qui identifie l’algorithme utilisé par la clé publique.</span><span class="sxs-lookup"><span data-stu-id="b99ae-111">The [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="b99ae-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b99ae-112">Requirements</span></span>



| <span data-ttu-id="b99ae-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b99ae-113">Requirement</span></span> | <span data-ttu-id="b99ae-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b99ae-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b99ae-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b99ae-115">Redistributable</span></span><br/> | <span data-ttu-id="b99ae-116">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="b99ae-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b99ae-117">DLL</span><span class="sxs-lookup"><span data-stu-id="b99ae-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="b99ae-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b99ae-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b99ae-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b99ae-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b99ae-120">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="b99ae-120">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
