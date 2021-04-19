---
description: Récupère une valeur booléenne qui indique si le bit bit cRLSign est défini.
ms.assetid: 76ca86e3-55f7-4720-9fa5-d465db2a7b5a
title: KeyUsage. IsCRLSignEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCRLSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39bd8509ebc89719e5d06e5e60a300ec2cd9949a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539490"
---
# <a name="keyusageiscrlsignenabled-property"></a><span data-ttu-id="b4cf7-103">KeyUsage. IsCRLSignEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="b4cf7-103">KeyUsage.IsCRLSignEnabled property</span></span>

<span data-ttu-id="b4cf7-104">\[La propriété **IsCRLSignEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-104">\[The **IsCRLSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b4cf7-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b4cf7-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b4cf7-106">La propriété **IsCRLSignEnabled** récupère une valeur booléenne qui indique si le bit bit cRLSign est défini.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-106">The **IsCRLSignEnabled** property retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4cf7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4cf7-107">Syntax</span></span>


```VB
KeyUsage.IsCRLSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b4cf7-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b4cf7-108">Property value</span></span>

<span data-ttu-id="b4cf7-109">Si la **valeur est true**, le bit bit cRLSign est défini.</span><span class="sxs-lookup"><span data-stu-id="b4cf7-109">If **true**, the CRLSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4cf7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4cf7-110">Requirements</span></span>



| <span data-ttu-id="b4cf7-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4cf7-111">Requirement</span></span> | <span data-ttu-id="b4cf7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4cf7-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cf7-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b4cf7-113">Redistributable</span></span><br/> | <span data-ttu-id="b4cf7-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4cf7-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b4cf7-115">DLL</span><span class="sxs-lookup"><span data-stu-id="b4cf7-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="b4cf7-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4cf7-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4cf7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4cf7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4cf7-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="b4cf7-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
