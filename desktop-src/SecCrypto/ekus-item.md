---
description: Récupère l’objet EKU qui représente la propriété utilisation améliorée de la clé (EKU) indexée.
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: 'IEKUs :: Item, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e3eaf8d0b303207aae3ef78cc82771e1436b1027
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526803"
---
# <a name="iekusitem-property"></a><span data-ttu-id="1f3ef-103">IEKUs :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="1f3ef-103">IEKUs::Item property</span></span>

<span data-ttu-id="1f3ef-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1f3ef-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1f3ef-105">Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1f3ef-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1f3ef-106">La propriété **Item** récupère l’objet [**EKU**](eku.md) qui représente la propriété utilisation améliorée de la clé (EKU) indexée.</span><span class="sxs-lookup"><span data-stu-id="1f3ef-106">The **Item** property retrieves the [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

<span data-ttu-id="1f3ef-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1f3ef-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f3ef-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f3ef-108">Syntax</span></span>


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="1f3ef-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1f3ef-109">Property value</span></span>

<span data-ttu-id="1f3ef-110">Objet [**EKU**](eku.md) qui représente la propriété utilisation améliorée de la clé (EKU) indexée.</span><span class="sxs-lookup"><span data-stu-id="1f3ef-110">An [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f3ef-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f3ef-111">Requirements</span></span>



| <span data-ttu-id="1f3ef-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f3ef-112">Requirement</span></span> | <span data-ttu-id="1f3ef-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f3ef-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3ef-114">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1f3ef-114">End of client support</span></span><br/> | <span data-ttu-id="1f3ef-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f3ef-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1f3ef-116">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1f3ef-116">End of server support</span></span><br/> | <span data-ttu-id="1f3ef-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f3ef-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1f3ef-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1f3ef-118">Redistributable</span></span><br/>       | <span data-ttu-id="1f3ef-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="1f3ef-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1f3ef-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1f3ef-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1f3ef-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f3ef-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f3ef-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f3ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f3ef-123">**Utilisations améliorées de la clé**</span><span class="sxs-lookup"><span data-stu-id="1f3ef-123">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
