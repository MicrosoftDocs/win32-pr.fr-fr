---
description: Récupère la date de fin de validité du certificat.
ms.assetid: 25e76b25-9a18-439c-acb8-e0af97b6fcd5
title: Propriété Certificate. ValidToDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidToDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08f6c0748c38ec31085c937eda37a413a3644f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532864"
---
# <a name="certificatevalidtodate-property"></a><span data-ttu-id="e8684-103">Propriété Certificate. ValidToDate</span><span class="sxs-lookup"><span data-stu-id="e8684-103">Certificate.ValidToDate property</span></span>

<span data-ttu-id="e8684-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e8684-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e8684-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e8684-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e8684-106">La propriété **ValidToDate** récupère la date de fin de validité du certificat.</span><span class="sxs-lookup"><span data-stu-id="e8684-106">The **ValidToDate** property retrieves the ending date for the validity of the certificate.</span></span>

<span data-ttu-id="e8684-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e8684-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8684-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8684-108">Syntax</span></span>


```VB
Certificate.ValidToDate As Date
```



## <a name="property-value"></a><span data-ttu-id="e8684-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e8684-109">Property value</span></span>

<span data-ttu-id="e8684-110">Date qui indique la date de fin de validité du certificat.</span><span class="sxs-lookup"><span data-stu-id="e8684-110">A date that indicates the ending date for the validity of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8684-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8684-111">Requirements</span></span>



| <span data-ttu-id="e8684-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8684-112">Requirement</span></span> | <span data-ttu-id="e8684-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8684-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8684-114">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e8684-114">End of client support</span></span><br/> | <span data-ttu-id="e8684-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8684-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e8684-116">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e8684-116">End of server support</span></span><br/> | <span data-ttu-id="e8684-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8684-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e8684-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e8684-118">Redistributable</span></span><br/>       | <span data-ttu-id="e8684-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8684-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e8684-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e8684-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e8684-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8684-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8684-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8684-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8684-123">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="e8684-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
