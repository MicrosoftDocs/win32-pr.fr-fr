---
description: Récupère la valeur de la clé publique.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: Propriété PublicKey. EncodedKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de2c7b2bfbbdaf28345ae29e260bfd30c5754ffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545656"
---
# <a name="publickeyencodedkey-property"></a><span data-ttu-id="3043b-103">Propriété PublicKey. EncodedKey</span><span class="sxs-lookup"><span data-stu-id="3043b-103">PublicKey.EncodedKey property</span></span>

<span data-ttu-id="3043b-104">\[La propriété **EncodedKey** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="3043b-104">\[The **EncodedKey** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3043b-105">Utilisez plutôt la [**propriété X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3043b-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3043b-106">La propriété **EncodedKey** récupère la valeur de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="3043b-106">The **EncodedKey** property retrieves the value of the public key.</span></span>

## <a name="syntax"></a><span data-ttu-id="3043b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3043b-107">Syntax</span></span>


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="3043b-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3043b-108">Property value</span></span>

<span data-ttu-id="3043b-109">Objet [**EncodedData**](encodeddata.md) qui fournit l’accès à la valeur de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="3043b-109">An [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="3043b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3043b-110">Requirements</span></span>



| <span data-ttu-id="3043b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3043b-111">Requirement</span></span> | <span data-ttu-id="3043b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="3043b-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3043b-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3043b-113">Redistributable</span></span><br/> | <span data-ttu-id="3043b-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="3043b-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3043b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="3043b-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="3043b-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3043b-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3043b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3043b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3043b-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="3043b-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
