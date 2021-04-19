---
description: La propriété Item récupère une extension, par index, de la collection. Il s’agit de la propriété par défaut.
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Extensions. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2cefe9ac1dd278c17161cc8e2349c051dccabff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523548"
---
# <a name="extensionsitem-property"></a><span data-ttu-id="2425d-104">Extensions. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="2425d-104">Extensions.Item property</span></span>

<span data-ttu-id="2425d-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2425d-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2425d-106">Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2425d-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2425d-107">La propriété **Item** récupère une extension, par index, de la collection.</span><span class="sxs-lookup"><span data-stu-id="2425d-107">The **Item** property retrieves an extension, by index, from the collection.</span></span> <span data-ttu-id="2425d-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="2425d-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2425d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2425d-109">Syntax</span></span>


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="2425d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2425d-110">Property value</span></span>

<span data-ttu-id="2425d-111">Objet d' [**extension**](extension.md) qui représente l’extension de certificat indexée de la collection.</span><span class="sxs-lookup"><span data-stu-id="2425d-111">An [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="2425d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2425d-112">Requirements</span></span>



| <span data-ttu-id="2425d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2425d-113">Requirement</span></span> | <span data-ttu-id="2425d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2425d-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2425d-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2425d-115">End of client support</span></span><br/> | <span data-ttu-id="2425d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2425d-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2425d-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="2425d-117">End of server support</span></span><br/> | <span data-ttu-id="2425d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2425d-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2425d-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2425d-119">Redistributable</span></span><br/>       | <span data-ttu-id="2425d-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2425d-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2425d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2425d-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2425d-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2425d-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2425d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2425d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2425d-124">**Extensions**</span><span class="sxs-lookup"><span data-stu-id="2425d-124">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
