---
description: Récupère la collection de certificats associée à l’objet SignedData. Une fois récupérés, les objets de certificat individuels de la collection peuvent être énumérés.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: SignedData. Certificates, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542356"
---
# <a name="signeddatacertificates-property"></a><span data-ttu-id="12b7a-104">SignedData. Certificates, propriété</span><span class="sxs-lookup"><span data-stu-id="12b7a-104">SignedData.Certificates property</span></span>

<span data-ttu-id="12b7a-105">\[La propriété **certificats** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="12b7a-105">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="12b7a-106">Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="12b7a-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="12b7a-107">La propriété **certificats** récupère la collection de [**certificats**](certificates.md) associée à l’objet [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="12b7a-107">The **Certificates** property retrieves the [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span> <span data-ttu-id="12b7a-108">Une fois récupérés, les objets de [**certificat**](certificate.md) individuels de la collection peuvent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="12b7a-108">After being retrieved, the individual [**Certificate**](certificate.md) objects in the collection can be enumerated.</span></span>

## <a name="syntax"></a><span data-ttu-id="12b7a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12b7a-109">Syntax</span></span>


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="12b7a-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="12b7a-110">Property value</span></span>

<span data-ttu-id="12b7a-111">Collection de [**certificats**](certificates.md) associée à l’objet [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="12b7a-111">The [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="12b7a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12b7a-112">Requirements</span></span>



| <span data-ttu-id="12b7a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12b7a-113">Requirement</span></span> | <span data-ttu-id="12b7a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="12b7a-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12b7a-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="12b7a-115">Redistributable</span></span><br/> | <span data-ttu-id="12b7a-116">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="12b7a-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="12b7a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="12b7a-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="12b7a-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12b7a-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12b7a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12b7a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12b7a-120">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="12b7a-120">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
