---
description: Définit ou récupère les données à signer. Il s’agit de la propriété par défaut.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: SignedData. Content, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540063"
---
# <a name="signeddatacontent-property"></a><span data-ttu-id="a32eb-104">SignedData. Content, propriété</span><span class="sxs-lookup"><span data-stu-id="a32eb-104">SignedData.Content property</span></span>

<span data-ttu-id="a32eb-105">\[La propriété **contenu** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a32eb-105">\[The **Content** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a32eb-106">Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="a32eb-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a32eb-107">La propriété de **contenu** définit ou récupère les données à signer.</span><span class="sxs-lookup"><span data-stu-id="a32eb-107">The **Content** property sets or retrieves the data to be signed.</span></span> <span data-ttu-id="a32eb-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="a32eb-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a32eb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a32eb-109">Syntax</span></span>


```VB
SignedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="a32eb-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a32eb-110">Property value</span></span>

<span data-ttu-id="a32eb-111">Données à signer.</span><span class="sxs-lookup"><span data-stu-id="a32eb-111">The data to be signed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a32eb-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a32eb-112">Remarks</span></span>

<span data-ttu-id="a32eb-113">Cette propriété doit être initialisée avant l’appel de la méthode [**Sign**](signeddata-sign.md) .</span><span class="sxs-lookup"><span data-stu-id="a32eb-113">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span> <span data-ttu-id="a32eb-114">Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée, et toute signature associée à l’objet avant la modification de la propriété est perdue.</span><span class="sxs-lookup"><span data-stu-id="a32eb-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32eb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a32eb-115">Requirements</span></span>



| <span data-ttu-id="a32eb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a32eb-116">Requirement</span></span> | <span data-ttu-id="a32eb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a32eb-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a32eb-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a32eb-118">Redistributable</span></span><br/> | <span data-ttu-id="a32eb-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a32eb-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a32eb-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a32eb-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="a32eb-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a32eb-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a32eb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a32eb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a32eb-123">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="a32eb-123">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
