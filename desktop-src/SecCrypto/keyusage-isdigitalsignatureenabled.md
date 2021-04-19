---
description: Récupère une valeur booléenne qui indique si le bit digitalSignature est défini.
ms.assetid: 561eea86-ff23-4a26-adf2-b43009566eaa
title: KeyUsage. IsDigitalSignatureEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDigitalSignatureEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b323effebe60597e1d6cf66e75d48c39fcdca4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537306"
---
# <a name="keyusageisdigitalsignatureenabled-property"></a><span data-ttu-id="58e0b-103">KeyUsage. IsDigitalSignatureEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="58e0b-103">KeyUsage.IsDigitalSignatureEnabled property</span></span>

<span data-ttu-id="58e0b-104">\[La propriété **IsDigitalSignatureEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="58e0b-104">\[The **IsDigitalSignatureEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="58e0b-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="58e0b-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="58e0b-106">La propriété **IsDigitalSignatureEnabled** récupère une valeur booléenne qui indique si le bit DigitalSignature est défini.</span><span class="sxs-lookup"><span data-stu-id="58e0b-106">The **IsDigitalSignatureEnabled** property retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e0b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58e0b-107">Syntax</span></span>


```VB
KeyUsage.IsDigitalSignatureEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="58e0b-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="58e0b-108">Property value</span></span>

<span data-ttu-id="58e0b-109">Si la **valeur est true**, le bit DigitalSignature est défini.</span><span class="sxs-lookup"><span data-stu-id="58e0b-109">If **true**, the digitalSignature bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e0b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58e0b-110">Requirements</span></span>



| <span data-ttu-id="58e0b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58e0b-111">Requirement</span></span> | <span data-ttu-id="58e0b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="58e0b-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58e0b-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="58e0b-113">Redistributable</span></span><br/> | <span data-ttu-id="58e0b-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="58e0b-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="58e0b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="58e0b-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="58e0b-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e0b-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e0b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58e0b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e0b-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="58e0b-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
