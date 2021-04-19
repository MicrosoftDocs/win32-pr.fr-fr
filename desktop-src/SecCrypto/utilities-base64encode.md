---
description: Encode une chaîne au format Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Méthode Utilities. Base64Encode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537085"
---
# <a name="utilitiesbase64encode-method"></a><span data-ttu-id="6f715-103">Méthode Utilities. Base64Encode</span><span class="sxs-lookup"><span data-stu-id="6f715-103">Utilities.Base64Encode method</span></span>

<span data-ttu-id="6f715-104">\[La méthode **Base64Encode** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.\]</span><span class="sxs-lookup"><span data-stu-id="6f715-104">\[The **Base64Encode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="6f715-105">La méthode **Base64Encode** encode une chaîne au format Base64.</span><span class="sxs-lookup"><span data-stu-id="6f715-105">The **Base64Encode** method encodes a string as base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f715-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f715-106">Syntax</span></span>


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a><span data-ttu-id="6f715-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f715-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f715-108">*SrcString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f715-108">*SrcString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f715-109">Chaîne à encoder en base64.</span><span class="sxs-lookup"><span data-stu-id="6f715-109">The string to encode as base64.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f715-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f715-110">Return value</span></span>

<span data-ttu-id="6f715-111">Chaîne encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="6f715-111">The base64-encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f715-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6f715-112">Remarks</span></span>

<span data-ttu-id="6f715-113">L’encodage Base64 est le schéma utilisé pour transmettre des données binaires.</span><span class="sxs-lookup"><span data-stu-id="6f715-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="6f715-114">Base64 traite les données en tant que groupes 24 bits, en mappant ces données à quatre caractères encodés.</span><span class="sxs-lookup"><span data-stu-id="6f715-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="6f715-115">L’encodage Base64 est parfois appelé encodage 3 à 4.</span><span class="sxs-lookup"><span data-stu-id="6f715-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="6f715-116">Chaque 6 bits du groupe 24 bits est utilisé comme index dans une table de mappage (l’alphabet base64) pour obtenir un caractère pour les données encodées.</span><span class="sxs-lookup"><span data-stu-id="6f715-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="6f715-117">Les données encodées ont des longueurs de ligne limitées à 76 caractères.</span><span class="sxs-lookup"><span data-stu-id="6f715-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f715-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f715-118">Requirements</span></span>



| <span data-ttu-id="6f715-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f715-119">Requirement</span></span> | <span data-ttu-id="6f715-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f715-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f715-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6f715-121">Redistributable</span></span><br/> | <span data-ttu-id="6f715-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f715-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6f715-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6f715-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="6f715-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f715-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f715-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f715-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f715-126">**Services**</span><span class="sxs-lookup"><span data-stu-id="6f715-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




