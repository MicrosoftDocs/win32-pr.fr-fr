---
description: Récupère une valeur booléenne qui indique si le bit keyEncipherment est défini.
ms.assetid: 2bdce181-3de7-4dc1-8059-1e1ca96c0d2d
title: KeyUsage. IsKeyEnciphermentEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db34737954b0627953758ebc1c5bf7a64b45b1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522769"
---
# <a name="keyusageiskeyenciphermentenabled-property"></a><span data-ttu-id="96408-103">KeyUsage. IsKeyEnciphermentEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="96408-103">KeyUsage.IsKeyEnciphermentEnabled property</span></span>

<span data-ttu-id="96408-104">\[La propriété **IsKeyEnciphermentEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="96408-104">\[The **IsKeyEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="96408-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="96408-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="96408-106">La propriété **IsKeyEnciphermentEnabled** récupère une valeur booléenne qui indique si le bit KeyEncipherment est défini.</span><span class="sxs-lookup"><span data-stu-id="96408-106">The **IsKeyEnciphermentEnabled** property retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="96408-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96408-107">Syntax</span></span>


```VB
KeyUsage.IsKeyEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="96408-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="96408-108">Property value</span></span>

<span data-ttu-id="96408-109">Si la **valeur est true**, le bit KeyEncipherment est défini.</span><span class="sxs-lookup"><span data-stu-id="96408-109">If **true**, the keyEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="96408-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96408-110">Requirements</span></span>



| <span data-ttu-id="96408-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96408-111">Requirement</span></span> | <span data-ttu-id="96408-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="96408-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96408-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="96408-113">Redistributable</span></span><br/> | <span data-ttu-id="96408-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="96408-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="96408-115">DLL</span><span class="sxs-lookup"><span data-stu-id="96408-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="96408-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96408-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96408-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96408-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96408-118">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="96408-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
