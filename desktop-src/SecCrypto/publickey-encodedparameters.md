---
description: Récupère les paramètres de l’algorithme de clé publique.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: Propriété PublicKey. EncodedParameters
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537751"
---
# <a name="publickeyencodedparameters-property"></a><span data-ttu-id="5d629-103">Propriété PublicKey. EncodedParameters</span><span class="sxs-lookup"><span data-stu-id="5d629-103">PublicKey.EncodedParameters property</span></span>

<span data-ttu-id="5d629-104">\[La propriété **EncodedParameters** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="5d629-104">\[The **EncodedParameters** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d629-105">Utilisez plutôt la [**propriété X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="5d629-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5d629-106">La propriété **EncodedParameters** récupère les paramètres de l’algorithme de clé publique.</span><span class="sxs-lookup"><span data-stu-id="5d629-106">The **EncodedParameters** property retrieves the parameters of the public key algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d629-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d629-107">Syntax</span></span>


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="5d629-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5d629-108">Property value</span></span>

<span data-ttu-id="5d629-109">Objet [**EncodedData**](encodeddata.md) qui fournit l’accès aux paramètres de l’algorithme de clé publique.</span><span class="sxs-lookup"><span data-stu-id="5d629-109">An [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d629-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d629-110">Requirements</span></span>



| <span data-ttu-id="5d629-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d629-111">Requirement</span></span> | <span data-ttu-id="5d629-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d629-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d629-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5d629-113">Redistributable</span></span><br/> | <span data-ttu-id="5d629-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d629-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5d629-115">DLL</span><span class="sxs-lookup"><span data-stu-id="5d629-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="5d629-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d629-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d629-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d629-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d629-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="5d629-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
