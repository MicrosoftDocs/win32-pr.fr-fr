---
description: Récupère l’objet signataire qui représente le signataire indexé.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Propriété Signers. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9b0b4179c1ea7e2ded5d945f64f03124eb864fdc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543366"
---
# <a name="signersitem-property"></a><span data-ttu-id="6e5ef-103">Propriété Signers. Item</span><span class="sxs-lookup"><span data-stu-id="6e5ef-103">Signers.Item property</span></span>

<span data-ttu-id="6e5ef-104">\[La propriété **Item** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6e5ef-105">Utilisez plutôt une collection d’objets CmsSigner.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="6e5ef-106">Pour plus d’informations, consultez la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="6e5ef-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6e5ef-107">La propriété **Item** récupère l’objet [**signataire**](signer.md) qui représente le signataire indexé.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-107">The **Item** property retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="6e5ef-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e5ef-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e5ef-109">Syntax</span></span>


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="6e5ef-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6e5ef-110">Property value</span></span>

<span data-ttu-id="6e5ef-111">Objet [**signataire**](signer.md) qui représente le signataire indexé.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-111">The [**Signer**](signer.md) object that represents the indexed signer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e5ef-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e5ef-112">Requirements</span></span>



| <span data-ttu-id="6e5ef-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e5ef-113">Requirement</span></span> | <span data-ttu-id="6e5ef-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e5ef-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5ef-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6e5ef-115">Redistributable</span></span><br/> | <span data-ttu-id="6e5ef-116">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e5ef-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6e5ef-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6e5ef-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="6e5ef-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ef-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e5ef-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e5ef-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5ef-120">**Signataires**</span><span class="sxs-lookup"><span data-stu-id="6e5ef-120">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
