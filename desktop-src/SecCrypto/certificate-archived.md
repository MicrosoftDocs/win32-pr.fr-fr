---
description: Définit ou récupère une valeur booléenne qui indique si le certificat est archivé.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Propriété Certificate. Archived
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1d8cdea3e43bbe10ee87f8f4aa605740a15e6ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540104"
---
# <a name="certificatearchived-property"></a><span data-ttu-id="63c52-103">Propriété Certificate. Archived</span><span class="sxs-lookup"><span data-stu-id="63c52-103">Certificate.Archived property</span></span>

<span data-ttu-id="63c52-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="63c52-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="63c52-105">Utilisez plutôt la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="63c52-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="63c52-106">La propriété **archivée** définit ou récupère une valeur booléenne qui indique si le certificat est archivé.</span><span class="sxs-lookup"><span data-stu-id="63c52-106">The **Archived** property sets or retrieves a Boolean value that indicates whether the certificate is archived.</span></span>

<span data-ttu-id="63c52-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="63c52-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c52-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63c52-108">Syntax</span></span>


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a><span data-ttu-id="63c52-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="63c52-109">Property value</span></span>

<span data-ttu-id="63c52-110">Valeur booléenne qui indique si le certificat est archivé.</span><span class="sxs-lookup"><span data-stu-id="63c52-110">A Boolean value that indicates whether the certificate is archived.</span></span> <span data-ttu-id="63c52-111">Si la **valeur est true**, le certificat est archivé.</span><span class="sxs-lookup"><span data-stu-id="63c52-111">If **true**, the certificate is archived.</span></span> <span data-ttu-id="63c52-112">Notez que le fait de remplacer la valeur **false** par **true** Archive le certificat.</span><span class="sxs-lookup"><span data-stu-id="63c52-112">Note that changing the value from **false** to **true** archives the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="63c52-113">Notes</span><span class="sxs-lookup"><span data-stu-id="63c52-113">Remarks</span></span>

<span data-ttu-id="63c52-114">Cette propriété déclenche l’E CAPICOM \_ E \_ non \_ autorisée lorsque le script est basé sur une application Web.</span><span class="sxs-lookup"><span data-stu-id="63c52-114">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

> [!Note]  
> <span data-ttu-id="63c52-115">Un certificat archivé n’est pas visible dans l’interface utilisateur de gestion des certificats.</span><span class="sxs-lookup"><span data-stu-id="63c52-115">An archived certificate is not visible in the certificate management user interface.</span></span> <span data-ttu-id="63c52-116">En outre, les certificats archivés ne sont pas inclus dans la méthode [**Store. Open**](store-open.md) sauf si le \_ magasin CAPICOM \_ Open \_ include \_ est spécifié.</span><span class="sxs-lookup"><span data-stu-id="63c52-116">Also, archived certificates will not be included in the [**Store.Open**](store-open.md) method unless CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED is specified.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63c52-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63c52-117">Requirements</span></span>



| <span data-ttu-id="63c52-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63c52-118">Requirement</span></span> | <span data-ttu-id="63c52-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="63c52-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63c52-120">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="63c52-120">End of client support</span></span><br/> | <span data-ttu-id="63c52-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63c52-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="63c52-122">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="63c52-122">End of server support</span></span><br/> | <span data-ttu-id="63c52-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63c52-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="63c52-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="63c52-124">Redistributable</span></span><br/>       | <span data-ttu-id="63c52-125">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="63c52-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="63c52-126">DLL</span><span class="sxs-lookup"><span data-stu-id="63c52-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="63c52-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63c52-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
