---
description: Récupère une valeur booléenne qui indique si le bit decipherOnly est défini.
ms.assetid: 69d8649d-c7bc-438b-afdd-6c9d2627cd72
title: KeyUsage. IsDecipherOnlyEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDecipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5ca72348220d6943ad367e88f404e0f3163f4c42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532699"
---
# <a name="keyusageisdecipheronlyenabled-property"></a><span data-ttu-id="445c4-103">KeyUsage. IsDecipherOnlyEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="445c4-103">KeyUsage.IsDecipherOnlyEnabled property</span></span>

<span data-ttu-id="445c4-104">\[La propriété **IsDecipherOnlyEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="445c4-104">\[The **IsDecipherOnlyEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="445c4-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="445c4-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="445c4-106">La propriété **IsDecipherOnlyEnabled** récupère une valeur booléenne qui indique si le bit decipherOnly est défini.</span><span class="sxs-lookup"><span data-stu-id="445c4-106">The **IsDecipherOnlyEnabled** property retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="445c4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="445c4-107">Syntax</span></span>


```VB
KeyUsage.IsDecipherOnlyEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="445c4-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="445c4-108">Property value</span></span>

<span data-ttu-id="445c4-109">Si la **valeur est true**, le bit decipherOnly est défini.</span><span class="sxs-lookup"><span data-stu-id="445c4-109">If **true**, the decipherOnly bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="445c4-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="445c4-110">Requirements</span></span>



| <span data-ttu-id="445c4-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="445c4-111">Requirement</span></span> | <span data-ttu-id="445c4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="445c4-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="445c4-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="445c4-113">Redistributable</span></span><br/> | <span data-ttu-id="445c4-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="445c4-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="445c4-115">DLL</span><span class="sxs-lookup"><span data-stu-id="445c4-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="445c4-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="445c4-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="445c4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="445c4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445c4-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="445c4-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
