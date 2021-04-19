---
description: Définit ou récupère l’objet de certificat qui représente le certificat d’un signataire des données.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Signature. Certificate, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535237"
---
# <a name="signercertificate-property"></a><span data-ttu-id="0acaf-103">Signature. Certificate, propriété</span><span class="sxs-lookup"><span data-stu-id="0acaf-103">Signer.Certificate property</span></span>

<span data-ttu-id="0acaf-104">\[La propriété **certificat** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="0acaf-104">\[The **Certificate** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0acaf-105">Utilisez plutôt la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="0acaf-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="0acaf-106">La propriété **Certificate** définit ou récupère l’objet [**certificat**](certificate.md) qui représente le certificat d’un signataire des données.</span><span class="sxs-lookup"><span data-stu-id="0acaf-106">The **Certificate** property sets or retrieves the [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span> <span data-ttu-id="0acaf-107">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="0acaf-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0acaf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0acaf-108">Syntax</span></span>


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a><span data-ttu-id="0acaf-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0acaf-109">Property value</span></span>

<span data-ttu-id="0acaf-110">Objet de [**certificat**](certificate.md) qui représente le certificat d’un signataire des données.</span><span class="sxs-lookup"><span data-stu-id="0acaf-110">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span>

## <a name="remarks"></a><span data-ttu-id="0acaf-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0acaf-111">Remarks</span></span>

<span data-ttu-id="0acaf-112">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="0acaf-112">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="0acaf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0acaf-113">Requirements</span></span>



| <span data-ttu-id="0acaf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0acaf-114">Requirement</span></span> | <span data-ttu-id="0acaf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0acaf-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0acaf-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0acaf-116">Redistributable</span></span><br/> | <span data-ttu-id="0acaf-117">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="0acaf-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0acaf-118">DLL</span><span class="sxs-lookup"><span data-stu-id="0acaf-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="0acaf-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0acaf-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0acaf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0acaf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0acaf-121">**Signataire**</span><span class="sxs-lookup"><span data-stu-id="0acaf-121">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
