---
description: Récupère une valeur booléenne qui indique si le bit keyAgreement est défini.
ms.assetid: 3dd1f6c7-893d-453e-92dc-ffeffd879519
title: KeyUsage. IsKeyAgreementEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyAgreementEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 74369996d9e525746e315d1dd2934ef854ffd110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525918"
---
# <a name="keyusageiskeyagreementenabled-property"></a><span data-ttu-id="eb1fa-103">KeyUsage. IsKeyAgreementEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="eb1fa-103">KeyUsage.IsKeyAgreementEnabled property</span></span>

<span data-ttu-id="eb1fa-104">\[La propriété **IsKeyAgreementEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-104">\[The **IsKeyAgreementEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eb1fa-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="eb1fa-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="eb1fa-106">La propriété **IsKeyAgreementEnabled** récupère une valeur booléenne qui indique si le bit keyAgreement est défini.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-106">The **IsKeyAgreementEnabled** property retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1fa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb1fa-107">Syntax</span></span>


```VB
KeyUsage.IsKeyAgreementEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="eb1fa-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="eb1fa-108">Property value</span></span>

<span data-ttu-id="eb1fa-109">Si la **valeur est true**, le bit keyAgreement est défini.</span><span class="sxs-lookup"><span data-stu-id="eb1fa-109">If **true**, the keyAgreement bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb1fa-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb1fa-110">Requirements</span></span>



| <span data-ttu-id="eb1fa-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb1fa-111">Requirement</span></span> | <span data-ttu-id="eb1fa-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb1fa-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1fa-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="eb1fa-113">Redistributable</span></span><br/> | <span data-ttu-id="eb1fa-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="eb1fa-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="eb1fa-115">DLL</span><span class="sxs-lookup"><span data-stu-id="eb1fa-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="eb1fa-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb1fa-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb1fa-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb1fa-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb1fa-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="eb1fa-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
