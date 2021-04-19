---
description: Retourne une valeur booléenne qui indique si l’extension EKU est présente. Il s’agit de la propriété par défaut.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: ExtendedKeyUsage. IsPresent, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 785fa3c973e7f90eeab20bd76826b9e5bf612891
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535293"
---
# <a name="extendedkeyusageispresent-property"></a><span data-ttu-id="935d0-104">ExtendedKeyUsage. IsPresent, propriété</span><span class="sxs-lookup"><span data-stu-id="935d0-104">ExtendedKeyUsage.IsPresent property</span></span>

<span data-ttu-id="935d0-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="935d0-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="935d0-106">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="935d0-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="935d0-107">La propriété **IsPresent** retourne une valeur booléenne qui indique si l’extension EKU est présente.</span><span class="sxs-lookup"><span data-stu-id="935d0-107">The **IsPresent** property returns a Boolean value that indicates whether the EKU extension is present.</span></span> <span data-ttu-id="935d0-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="935d0-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="935d0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="935d0-109">Syntax</span></span>


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="935d0-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="935d0-110">Property value</span></span>

<span data-ttu-id="935d0-111">Si la **valeur est true**, l’extension EKU est présente.</span><span class="sxs-lookup"><span data-stu-id="935d0-111">If **true**, the EKU extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="935d0-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="935d0-112">Requirements</span></span>



| <span data-ttu-id="935d0-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="935d0-113">Requirement</span></span> | <span data-ttu-id="935d0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="935d0-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="935d0-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="935d0-115">End of client support</span></span><br/> | <span data-ttu-id="935d0-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="935d0-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="935d0-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="935d0-117">End of server support</span></span><br/> | <span data-ttu-id="935d0-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="935d0-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="935d0-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="935d0-119">Redistributable</span></span><br/>       | <span data-ttu-id="935d0-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="935d0-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="935d0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="935d0-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="935d0-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="935d0-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="935d0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="935d0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935d0-124">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="935d0-124">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
