---
description: Ajoute un objet certificat à une collection Recipients.
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: Recipients. Add, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540384"
---
# <a name="recipientsadd-method"></a><span data-ttu-id="aed9e-103">Recipients. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="aed9e-103">Recipients.Add method</span></span>

<span data-ttu-id="aed9e-104">\[La méthode **Add** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="aed9e-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="aed9e-105">Utilisez plutôt la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="aed9e-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="aed9e-106">La méthode **Add** ajoute un objet [**certificat**](certificate.md) à une collection [**Recipients**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="aed9e-106">The **Add** method adds a [**Certificate**](certificate.md) object to a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed9e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aed9e-107">Syntax</span></span>


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="aed9e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aed9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aed9e-109">*Certificat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aed9e-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed9e-110">Expression qui correspond à l’objet de [**certificat**](certificate.md) à ajouter à la collection.</span><span class="sxs-lookup"><span data-stu-id="aed9e-110">Expression that resolves to the [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aed9e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aed9e-111">Return value</span></span>

<span data-ttu-id="aed9e-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="aed9e-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aed9e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aed9e-113">Requirements</span></span>



| <span data-ttu-id="aed9e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aed9e-114">Requirement</span></span> | <span data-ttu-id="aed9e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="aed9e-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aed9e-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="aed9e-116">Redistributable</span></span><br/> | <span data-ttu-id="aed9e-117">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="aed9e-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aed9e-118">DLL</span><span class="sxs-lookup"><span data-stu-id="aed9e-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="aed9e-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aed9e-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aed9e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aed9e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed9e-121">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="aed9e-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="aed9e-122">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="aed9e-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
