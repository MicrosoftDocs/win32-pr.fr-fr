---
description: Récupère une chaîne qui contient le numéro de série du certificat.
ms.assetid: d08be744-4ae8-49f9-8b00-48e76c296f2b
title: Propriété Certificate. SerialNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SerialNumber
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6dbd9485891cc89e686cef118e12dd43ec400f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542320"
---
# <a name="certificateserialnumber-property"></a><span data-ttu-id="32102-103">Propriété Certificate. SerialNumber</span><span class="sxs-lookup"><span data-stu-id="32102-103">Certificate.SerialNumber property</span></span>

<span data-ttu-id="32102-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="32102-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="32102-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="32102-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="32102-106">La propriété **SerialNumber** récupère une chaîne qui contient le numéro de série du certificat.</span><span class="sxs-lookup"><span data-stu-id="32102-106">The **SerialNumber** property retrieves a string that contains the certificate serial number.</span></span>

<span data-ttu-id="32102-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="32102-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="32102-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32102-108">Syntax</span></span>


```VB
Certificate.SerialNumber As String
```



## <a name="property-value"></a><span data-ttu-id="32102-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="32102-109">Property value</span></span>

<span data-ttu-id="32102-110">Chaîne qui contient le numéro de série du certificat.</span><span class="sxs-lookup"><span data-stu-id="32102-110">A string that contains the certificate serial number.</span></span>

## <a name="requirements"></a><span data-ttu-id="32102-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32102-111">Requirements</span></span>



| <span data-ttu-id="32102-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32102-112">Requirement</span></span> | <span data-ttu-id="32102-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="32102-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32102-114">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="32102-114">End of client support</span></span><br/> | <span data-ttu-id="32102-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32102-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="32102-116">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="32102-116">End of server support</span></span><br/> | <span data-ttu-id="32102-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32102-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="32102-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="32102-118">Redistributable</span></span><br/>       | <span data-ttu-id="32102-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="32102-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="32102-120">DLL</span><span class="sxs-lookup"><span data-stu-id="32102-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="32102-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32102-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
