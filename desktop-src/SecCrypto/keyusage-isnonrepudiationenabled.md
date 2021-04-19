---
description: Récupère une valeur booléenne qui indique si le bit nonRepudiationEnabled est défini.
ms.assetid: d9bcf0fc-8b2d-408c-b587-71903ef5f5f6
title: KeyUsage. IsNonRepudiationEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsNonRepudiationEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 30e0a532cd39f2150591a3eb74ed9bbba83a7080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535221"
---
# <a name="keyusageisnonrepudiationenabled-property"></a><span data-ttu-id="f9eb3-103">KeyUsage. IsNonRepudiationEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="f9eb3-103">KeyUsage.IsNonRepudiationEnabled property</span></span>

<span data-ttu-id="f9eb3-104">\[La propriété **IsNonRepudiationEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f9eb3-104">\[The **IsNonRepudiationEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f9eb3-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f9eb3-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f9eb3-106">La propriété **IsNonRepudiationEnabled** récupère une valeur booléenne qui indique si le bit nonRepudiationEnabled est défini.</span><span class="sxs-lookup"><span data-stu-id="f9eb3-106">The **IsNonRepudiationEnabled** property retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9eb3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9eb3-107">Syntax</span></span>


```VB
KeyUsage.IsNonRepudiationEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f9eb3-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f9eb3-108">Property value</span></span>

<span data-ttu-id="f9eb3-109">Si la **valeur est true**, le bit nonRepudiationEnabled est défini.</span><span class="sxs-lookup"><span data-stu-id="f9eb3-109">If **true**, the nonRepudiationEnabled bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9eb3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9eb3-110">Requirements</span></span>



| <span data-ttu-id="f9eb3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9eb3-111">Requirement</span></span> | <span data-ttu-id="f9eb3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9eb3-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9eb3-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f9eb3-113">Redistributable</span></span><br/> | <span data-ttu-id="f9eb3-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="f9eb3-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f9eb3-115">DLL</span><span class="sxs-lookup"><span data-stu-id="f9eb3-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="f9eb3-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9eb3-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9eb3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9eb3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9eb3-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="f9eb3-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
