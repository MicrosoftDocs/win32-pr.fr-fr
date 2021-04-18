---
description: Récupère une valeur booléenne qui indique si l’extension KeyUsage est marquée comme critique.
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: KeyUsage. IsCritical, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b1829da9c9ddbcf5261f4cc595b72b8596193078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525919"
---
# <a name="keyusageiscritical-property"></a><span data-ttu-id="e3af6-103">KeyUsage. IsCritical, propriété</span><span class="sxs-lookup"><span data-stu-id="e3af6-103">KeyUsage.IsCritical property</span></span>

<span data-ttu-id="e3af6-104">\[La propriété **IsCritical** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e3af6-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e3af6-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e3af6-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e3af6-106">La propriété **IsCritical** récupère une valeur booléenne qui indique si l’extension KeyUsage est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="e3af6-106">The **IsCritical** property retrieves a Boolean value that indicates whether the KeyUsage extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3af6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3af6-107">Syntax</span></span>


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e3af6-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e3af6-108">Property value</span></span>

<span data-ttu-id="e3af6-109">Si la **valeur est true**, l’extension KeyUsage est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="e3af6-109">If **true**, the KeyUsage extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3af6-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3af6-110">Requirements</span></span>



| <span data-ttu-id="e3af6-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3af6-111">Requirement</span></span> | <span data-ttu-id="e3af6-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3af6-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3af6-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e3af6-113">Redistributable</span></span><br/> | <span data-ttu-id="e3af6-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="e3af6-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e3af6-115">DLL</span><span class="sxs-lookup"><span data-stu-id="e3af6-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="e3af6-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3af6-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3af6-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3af6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3af6-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="e3af6-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
