---
description: Supprime un objet de certificat d’une collection de destinataires.
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: Recipients. Remove, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06d276e2d8e75e8822cee3503a7e8342a94a6b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539603"
---
# <a name="recipientsremove-method"></a><span data-ttu-id="783f0-103">Recipients. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="783f0-103">Recipients.Remove method</span></span>

<span data-ttu-id="783f0-104">\[La méthode **Remove** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="783f0-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="783f0-105">Utilisez plutôt la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="783f0-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="783f0-106">La méthode **Remove** supprime un objet [**certificat**](certificate.md) d’une collection [**Recipients**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="783f0-106">The **Remove** method removes a [**Certificate**](certificate.md) object from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="783f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="783f0-107">Syntax</span></span>


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="783f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="783f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="783f0-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="783f0-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783f0-110">Index de l’objet de [**certificat**](certificate.md) à supprimer de la collection.</span><span class="sxs-lookup"><span data-stu-id="783f0-110">Index of the [**Certificate**](certificate.md) object to be removed from the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="783f0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="783f0-111">Return value</span></span>

<span data-ttu-id="783f0-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="783f0-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="783f0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="783f0-113">Requirements</span></span>



| <span data-ttu-id="783f0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="783f0-114">Requirement</span></span> | <span data-ttu-id="783f0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="783f0-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="783f0-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="783f0-116">Redistributable</span></span><br/> | <span data-ttu-id="783f0-117">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="783f0-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="783f0-118">DLL</span><span class="sxs-lookup"><span data-stu-id="783f0-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="783f0-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="783f0-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="783f0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="783f0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783f0-121">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="783f0-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="783f0-122">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="783f0-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
