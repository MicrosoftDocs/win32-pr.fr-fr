---
description: Retourne une valeur booléenne qui indique si l’extension d’utilisation améliorée de la clé est marquée comme critique.
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: ExtendedKeyUsage. IsCritical, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5331922567af3b9a34517ab5059fa03ad9904270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528701"
---
# <a name="extendedkeyusageiscritical-property"></a><span data-ttu-id="ca55a-103">ExtendedKeyUsage. IsCritical, propriété</span><span class="sxs-lookup"><span data-stu-id="ca55a-103">ExtendedKeyUsage.IsCritical property</span></span>

<span data-ttu-id="ca55a-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ca55a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ca55a-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ca55a-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ca55a-106">La propriété **IsCritical** retourne une valeur booléenne qui indique si l’extension d’utilisation améliorée de la clé est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="ca55a-106">The **IsCritical** property returns a Boolean value that indicates whether the EKU extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca55a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca55a-107">Syntax</span></span>


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ca55a-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ca55a-108">Property value</span></span>

<span data-ttu-id="ca55a-109">Si la **valeur est true**, l’extension d’utilisation améliorée de la clé est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="ca55a-109">If **true**, the EKU extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca55a-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca55a-110">Requirements</span></span>



| <span data-ttu-id="ca55a-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca55a-111">Requirement</span></span> | <span data-ttu-id="ca55a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca55a-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca55a-113">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ca55a-113">End of client support</span></span><br/> | <span data-ttu-id="ca55a-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca55a-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ca55a-115">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ca55a-115">End of server support</span></span><br/> | <span data-ttu-id="ca55a-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca55a-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ca55a-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ca55a-117">Redistributable</span></span><br/>       | <span data-ttu-id="ca55a-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca55a-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ca55a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ca55a-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ca55a-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca55a-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca55a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca55a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca55a-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="ca55a-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
