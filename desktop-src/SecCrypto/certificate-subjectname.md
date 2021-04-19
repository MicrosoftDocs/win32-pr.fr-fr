---
description: Récupère une chaîne qui contient le nom de l’objet du certificat.
ms.assetid: 95dc7e8b-6670-4dfc-9fe1-d37635fb92d6
title: Propriété Certificate. SubjectName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SubjectName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b17d99ab3ab485153a0af535aa74b9a9123ddaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545359"
---
# <a name="certificatesubjectname-property"></a><span data-ttu-id="be36b-103">Propriété Certificate. SubjectName</span><span class="sxs-lookup"><span data-stu-id="be36b-103">Certificate.SubjectName property</span></span>

<span data-ttu-id="be36b-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="be36b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="be36b-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="be36b-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="be36b-106">La propriété **SubjectName** récupère une chaîne qui contient le nom de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="be36b-106">The **SubjectName** property retrieves a string that contains the name of the certificate subject.</span></span>

<span data-ttu-id="be36b-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="be36b-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="be36b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be36b-108">Syntax</span></span>


```VB
Certificate.SubjectName As String
```



## <a name="property-value"></a><span data-ttu-id="be36b-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="be36b-109">Property value</span></span>

<span data-ttu-id="be36b-110">Chaîne qui contient le nom de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="be36b-110">A string that contains the name of the certificate subject.</span></span>

## <a name="requirements"></a><span data-ttu-id="be36b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be36b-111">Requirements</span></span>



| <span data-ttu-id="be36b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be36b-112">Requirement</span></span> | <span data-ttu-id="be36b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="be36b-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be36b-114">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="be36b-114">End of client support</span></span><br/> | <span data-ttu-id="be36b-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be36b-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="be36b-116">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="be36b-116">End of server support</span></span><br/> | <span data-ttu-id="be36b-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be36b-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="be36b-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="be36b-118">Redistributable</span></span><br/>       | <span data-ttu-id="be36b-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="be36b-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="be36b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="be36b-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="be36b-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be36b-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be36b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be36b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be36b-123">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="be36b-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
