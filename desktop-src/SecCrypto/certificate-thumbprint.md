---
description: Récupère une chaîne hexadécimale qui contient le hachage SHA-1 du certificat.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Propriété Certificate. empreinte
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c576c46ecf669d215c5bd20a80a0e5a65e3d4706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530393"
---
# <a name="certificatethumbprint-property"></a><span data-ttu-id="637c1-103">Propriété Certificate. empreinte</span><span class="sxs-lookup"><span data-stu-id="637c1-103">Certificate.Thumbprint property</span></span>

<span data-ttu-id="637c1-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="637c1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="637c1-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="637c1-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="637c1-106">La propriété d' **empreinte numérique** récupère une chaîne hexadécimale qui contient le hachage [*SHA-1*](../secgloss/s-gly.md) du certificat.</span><span class="sxs-lookup"><span data-stu-id="637c1-106">The **Thumbprint** property retrieves a hexadecimal string that contains the [*SHA-1*](../secgloss/s-gly.md) hash of the certificate.</span></span>

<span data-ttu-id="637c1-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="637c1-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="637c1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="637c1-108">Syntax</span></span>


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a><span data-ttu-id="637c1-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="637c1-109">Property value</span></span>

<span data-ttu-id="637c1-110">Chaîne hexadécimale qui contient le hachage SHA-1 du certificat.</span><span class="sxs-lookup"><span data-stu-id="637c1-110">A hexadecimal string that contains the SHA-1 hash of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="637c1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="637c1-111">Requirements</span></span>



| <span data-ttu-id="637c1-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="637c1-112">Requirement</span></span> | <span data-ttu-id="637c1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="637c1-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="637c1-114">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="637c1-114">End of client support</span></span><br/> | <span data-ttu-id="637c1-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="637c1-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="637c1-116">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="637c1-116">End of server support</span></span><br/> | <span data-ttu-id="637c1-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="637c1-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="637c1-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="637c1-118">Redistributable</span></span><br/>       | <span data-ttu-id="637c1-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="637c1-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="637c1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="637c1-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="637c1-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="637c1-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="637c1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="637c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="637c1-123">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="637c1-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
