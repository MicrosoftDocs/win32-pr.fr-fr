---
description: Récupère un objet de certificat qui représente le certificat indexé de la collection. Il s’agit de la propriété par défaut.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Certificates. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bbafaf20f74910e8ea5eb525f48374a2807fa030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533229"
---
# <a name="certificatesitem-property"></a><span data-ttu-id="0e88d-104">Certificates. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="0e88d-104">Certificates.Item property</span></span>

<span data-ttu-id="0e88d-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0e88d-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0e88d-106">Utilisez plutôt la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0e88d-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0e88d-107">La propriété **Item** récupère un objet [**certificat**](certificate.md) qui représente le certificat indexé de la collection.</span><span class="sxs-lookup"><span data-stu-id="0e88d-107">The **Item** property retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="0e88d-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="0e88d-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e88d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e88d-109">Syntax</span></span>


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="0e88d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0e88d-110">Property value</span></span>

<span data-ttu-id="0e88d-111">Objet de [**certificat**](certificate.md) qui représente le certificat indexé.</span><span class="sxs-lookup"><span data-stu-id="0e88d-111">A [**Certificate**](certificate.md) object that represents the indexed certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e88d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e88d-112">Requirements</span></span>



| <span data-ttu-id="0e88d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e88d-113">Requirement</span></span> | <span data-ttu-id="0e88d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e88d-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e88d-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0e88d-115">End of client support</span></span><br/> | <span data-ttu-id="0e88d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e88d-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0e88d-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0e88d-117">End of server support</span></span><br/> | <span data-ttu-id="0e88d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e88d-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0e88d-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0e88d-119">Redistributable</span></span><br/>       | <span data-ttu-id="0e88d-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="0e88d-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0e88d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0e88d-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0e88d-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e88d-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e88d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e88d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e88d-124">**Certificates**</span><span class="sxs-lookup"><span data-stu-id="0e88d-124">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
