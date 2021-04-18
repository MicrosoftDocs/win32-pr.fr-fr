---
description: Récupère une valeur booléenne qui indique si le bit dataEncipherment est défini.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: KeyUsage. IsDataEnciphermentEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aad6cbcd21830ad127b9537749dfb1c05a4c9ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523008"
---
# <a name="keyusageisdataenciphermentenabled-property"></a><span data-ttu-id="78519-103">KeyUsage. IsDataEnciphermentEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="78519-103">KeyUsage.IsDataEnciphermentEnabled property</span></span>

<span data-ttu-id="78519-104">\[La propriété **IsDataEnciphermentEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="78519-104">\[The **IsDataEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="78519-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="78519-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="78519-106">La propriété **IsDataEnciphermentEnabled** récupère une valeur booléenne qui indique si le bit DataEncipherment est défini.</span><span class="sxs-lookup"><span data-stu-id="78519-106">The **IsDataEnciphermentEnabled** property retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="78519-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78519-107">Syntax</span></span>


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="78519-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="78519-108">Property value</span></span>

<span data-ttu-id="78519-109">Si la **valeur est true**, le bit DataEncipherment est défini.</span><span class="sxs-lookup"><span data-stu-id="78519-109">If **true**, the dataEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="78519-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78519-110">Requirements</span></span>



| <span data-ttu-id="78519-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78519-111">Requirement</span></span> | <span data-ttu-id="78519-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="78519-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78519-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="78519-113">Redistributable</span></span><br/> | <span data-ttu-id="78519-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="78519-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="78519-115">DLL</span><span class="sxs-lookup"><span data-stu-id="78519-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="78519-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78519-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78519-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78519-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78519-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="78519-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
