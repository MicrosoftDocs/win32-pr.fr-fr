---
description: Récupère une valeur booléenne qui indique si le bit bit keyCertSign est défini.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: KeyUsage. IsKeyCertSignEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d475565896910f76211e3843526e9a889586efa0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525320"
---
# <a name="keyusageiskeycertsignenabled-property"></a><span data-ttu-id="6fdc2-103">KeyUsage. IsKeyCertSignEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="6fdc2-103">KeyUsage.IsKeyCertSignEnabled property</span></span>

<span data-ttu-id="6fdc2-104">\[La propriété **IsKeyCertSignEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6fdc2-104">\[The **IsKeyCertSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6fdc2-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6fdc2-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6fdc2-106">La propriété **IsKeyCertSignEnabled** récupère une valeur booléenne qui indique si le bit bit keyCertSign est défini.</span><span class="sxs-lookup"><span data-stu-id="6fdc2-106">The **IsKeyCertSignEnabled** property retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdc2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fdc2-107">Syntax</span></span>


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6fdc2-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6fdc2-108">Property value</span></span>

<span data-ttu-id="6fdc2-109">Si la **valeur est true**, le bit bit keyCertSign est défini.</span><span class="sxs-lookup"><span data-stu-id="6fdc2-109">If **true**, the keyCertSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fdc2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fdc2-110">Requirements</span></span>



| <span data-ttu-id="6fdc2-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fdc2-111">Requirement</span></span> | <span data-ttu-id="6fdc2-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fdc2-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdc2-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6fdc2-113">Redistributable</span></span><br/> | <span data-ttu-id="6fdc2-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6fdc2-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6fdc2-115">DLL</span><span class="sxs-lookup"><span data-stu-id="6fdc2-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="6fdc2-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fdc2-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fdc2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fdc2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fdc2-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="6fdc2-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
