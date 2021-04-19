---
description: Retourne la collection de EKU pour le certificat.
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: ExtendedKeyUsage. EKU, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 24bcf7b4332e75afad0e21415a7dfe8eb690c32b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540974"
---
# <a name="extendedkeyusageekus-property"></a><span data-ttu-id="22279-103">ExtendedKeyUsage. EKU, propriété</span><span class="sxs-lookup"><span data-stu-id="22279-103">ExtendedKeyUsage.EKUs property</span></span>

<span data-ttu-id="22279-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="22279-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="22279-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="22279-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="22279-106">La propriété **EKU** renvoie la collection de [**EKU**](ekus.md) pour le certificat.</span><span class="sxs-lookup"><span data-stu-id="22279-106">The **EKUs** property returns the [**EKUs**](ekus.md) collection for the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="22279-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22279-107">Syntax</span></span>


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a><span data-ttu-id="22279-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="22279-108">Property value</span></span>

<span data-ttu-id="22279-109">Collection [**de EKU qui**](ekus.md) contient les objets [**EKU**](eku.md) pour le certificat.</span><span class="sxs-lookup"><span data-stu-id="22279-109">The [**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="22279-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22279-110">Requirements</span></span>



| <span data-ttu-id="22279-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22279-111">Requirement</span></span> | <span data-ttu-id="22279-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="22279-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22279-113">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="22279-113">End of client support</span></span><br/> | <span data-ttu-id="22279-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22279-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="22279-115">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="22279-115">End of server support</span></span><br/> | <span data-ttu-id="22279-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22279-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="22279-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="22279-117">Redistributable</span></span><br/>       | <span data-ttu-id="22279-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="22279-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="22279-119">DLL</span><span class="sxs-lookup"><span data-stu-id="22279-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="22279-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22279-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22279-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22279-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22279-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="22279-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
