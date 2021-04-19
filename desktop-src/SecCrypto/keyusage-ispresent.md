---
description: Récupère une valeur booléenne qui indique si l’extension KeyUsage est présente.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: KeyUsage. IsPresent, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537340"
---
# <a name="keyusageispresent-property"></a><span data-ttu-id="a4aff-103">KeyUsage. IsPresent, propriété</span><span class="sxs-lookup"><span data-stu-id="a4aff-103">KeyUsage.IsPresent property</span></span>

<span data-ttu-id="a4aff-104">\[La propriété **IsPresent** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a4aff-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a4aff-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a4aff-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a4aff-106">La propriété **IsPresent** récupère une valeur booléenne qui indique si l’extension [**KeyUsage**](keyusage.md) est présente.</span><span class="sxs-lookup"><span data-stu-id="a4aff-106">The **IsPresent** property retrieves a Boolean value that indicates whether the [**KeyUsage**](keyusage.md) extension is present.</span></span>

<span data-ttu-id="a4aff-107">Cette propriété est la propriété par défaut de l’objet [**KeyUsage**](keyusage.md) .</span><span class="sxs-lookup"><span data-stu-id="a4aff-107">This property is the default property of the [**KeyUsage**](keyusage.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4aff-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4aff-108">Syntax</span></span>


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a4aff-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a4aff-109">Property value</span></span>

<span data-ttu-id="a4aff-110">Si la **valeur est true**, l’extension KeyUsage est présente.</span><span class="sxs-lookup"><span data-stu-id="a4aff-110">If **true**, the KeyUsage extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4aff-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4aff-111">Requirements</span></span>



| <span data-ttu-id="a4aff-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4aff-112">Requirement</span></span> | <span data-ttu-id="a4aff-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4aff-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4aff-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a4aff-114">Redistributable</span></span><br/> | <span data-ttu-id="a4aff-115">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4aff-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a4aff-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a4aff-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="a4aff-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4aff-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4aff-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4aff-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4aff-119">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="a4aff-119">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
