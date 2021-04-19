---
description: Récupère la date de début de validité du certificat.
ms.assetid: d1caa7d3-ed5c-4637-bcb6-5a3fda8b978e
title: Propriété Certificate. ValidFromDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidFromDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8637114ad471b2d938a94ba2d974703bdfb1f5d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545475"
---
# <a name="certificatevalidfromdate-property"></a><span data-ttu-id="972ba-103">Propriété Certificate. ValidFromDate</span><span class="sxs-lookup"><span data-stu-id="972ba-103">Certificate.ValidFromDate property</span></span>

<span data-ttu-id="972ba-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="972ba-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="972ba-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="972ba-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="972ba-106">La propriété **ValidFromDate** récupère la date de début de validité du certificat.</span><span class="sxs-lookup"><span data-stu-id="972ba-106">The **ValidFromDate** property retrieves the beginning date for the validity of the certificate.</span></span>

<span data-ttu-id="972ba-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="972ba-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="972ba-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="972ba-108">Syntax</span></span>


```VB
Certificate.ValidFromDate As Date
```



## <a name="property-value"></a><span data-ttu-id="972ba-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="972ba-109">Property value</span></span>

<span data-ttu-id="972ba-110">Date qui indique la date de début de validité du certificat.</span><span class="sxs-lookup"><span data-stu-id="972ba-110">A date that indicates the beginning date for the validity of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="972ba-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="972ba-111">Requirements</span></span>



| <span data-ttu-id="972ba-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="972ba-112">Requirement</span></span> | <span data-ttu-id="972ba-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="972ba-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="972ba-114">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="972ba-114">End of client support</span></span><br/> | <span data-ttu-id="972ba-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="972ba-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="972ba-116">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="972ba-116">End of server support</span></span><br/> | <span data-ttu-id="972ba-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="972ba-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="972ba-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="972ba-118">Redistributable</span></span><br/>       | <span data-ttu-id="972ba-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="972ba-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="972ba-120">DLL</span><span class="sxs-lookup"><span data-stu-id="972ba-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="972ba-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="972ba-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="972ba-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="972ba-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="972ba-123">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="972ba-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
