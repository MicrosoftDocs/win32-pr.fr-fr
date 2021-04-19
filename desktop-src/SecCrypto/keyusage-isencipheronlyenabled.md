---
description: Récupère une valeur booléenne qui indique si le bit encipherOnly est défini.
ms.assetid: 60d79ea4-4968-49e0-8d16-873fbcbd951c
title: KeyUsage. IsEncipherOnlyEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsEncipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8a473797f989d18e090af33f08274ecede2630b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541259"
---
# <a name="keyusageisencipheronlyenabled-property"></a><span data-ttu-id="970c2-103">KeyUsage. IsEncipherOnlyEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="970c2-103">KeyUsage.IsEncipherOnlyEnabled property</span></span>

<span data-ttu-id="970c2-104">\[La propriété **IsEncipherOnlyEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="970c2-104">\[The **IsEncipherOnlyEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="970c2-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="970c2-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="970c2-106">La propriété **IsEncipherOnlyEnabled** récupère une valeur booléenne qui indique si le bit encipherOnly est défini.</span><span class="sxs-lookup"><span data-stu-id="970c2-106">The **IsEncipherOnlyEnabled** property retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="970c2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="970c2-107">Syntax</span></span>


```VB
KeyUsage.IsEncipherOnlyEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="970c2-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="970c2-108">Property value</span></span>

<span data-ttu-id="970c2-109">Si la **valeur est true**, le bit encipherOnly est défini.</span><span class="sxs-lookup"><span data-stu-id="970c2-109">If **true**, the encipherOnly bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="970c2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="970c2-110">Requirements</span></span>



| <span data-ttu-id="970c2-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="970c2-111">Requirement</span></span> | <span data-ttu-id="970c2-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="970c2-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="970c2-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="970c2-113">Redistributable</span></span><br/> | <span data-ttu-id="970c2-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="970c2-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="970c2-115">DLL</span><span class="sxs-lookup"><span data-stu-id="970c2-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="970c2-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="970c2-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="970c2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="970c2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="970c2-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="970c2-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
