---
description: Récupère les créateurs de signature des données.
ms.assetid: 3e28f08a-c4d8-4dd7-953a-e1500eb5bee0
title: SignedData. Signers, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f4c58c2a69c483fc38412a6aa8377742d52d39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532748"
---
# <a name="signeddatasigners-property"></a><span data-ttu-id="2ed72-103">SignedData. Signers, propriété</span><span class="sxs-lookup"><span data-stu-id="2ed72-103">SignedData.Signers property</span></span>

<span data-ttu-id="2ed72-104">\[La propriété des **signataires** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="2ed72-104">\[The **Signers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2ed72-105">Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2ed72-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2ed72-106">La propriété des **signataires** récupère les créateurs de signature des données.</span><span class="sxs-lookup"><span data-stu-id="2ed72-106">The **Signers** property retrieves the signature creators of the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ed72-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ed72-107">Syntax</span></span>


```VB
SignedData.Signers As Signers
```



## <a name="property-value"></a><span data-ttu-id="2ed72-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2ed72-108">Property value</span></span>

<span data-ttu-id="2ed72-109">Collection de [**signataires**](signers.md) qui représente les créateurs de signature des données.</span><span class="sxs-lookup"><span data-stu-id="2ed72-109">The [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed72-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ed72-110">Requirements</span></span>



| <span data-ttu-id="2ed72-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ed72-111">Requirement</span></span> | <span data-ttu-id="2ed72-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ed72-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed72-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2ed72-113">Redistributable</span></span><br/> | <span data-ttu-id="2ed72-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2ed72-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2ed72-115">DLL</span><span class="sxs-lookup"><span data-stu-id="2ed72-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="2ed72-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ed72-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ed72-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ed72-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed72-118">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="2ed72-118">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
