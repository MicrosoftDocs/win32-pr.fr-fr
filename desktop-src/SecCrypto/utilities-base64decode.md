---
description: Décode une chaîne de base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Méthode Utilities. Base64Decode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542578"
---
# <a name="utilitiesbase64decode-method"></a><span data-ttu-id="71966-103">Méthode Utilities. Base64Decode</span><span class="sxs-lookup"><span data-stu-id="71966-103">Utilities.Base64Decode method</span></span>

<span data-ttu-id="71966-104">\[La méthode **Base64Decode** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.\]</span><span class="sxs-lookup"><span data-stu-id="71966-104">\[The **Base64Decode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="71966-105">La méthode **Base64Decode** décode une chaîne de base64.</span><span class="sxs-lookup"><span data-stu-id="71966-105">The **Base64Decode** method decodes a string from base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="71966-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71966-106">Syntax</span></span>


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a><span data-ttu-id="71966-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71966-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71966-108">*EncodedString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71966-108">*EncodedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71966-109">Chaîne encodée en base64 à décoder.</span><span class="sxs-lookup"><span data-stu-id="71966-109">The base64-encoded string to decode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71966-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71966-110">Return value</span></span>

<span data-ttu-id="71966-111">Chaîne décodée.</span><span class="sxs-lookup"><span data-stu-id="71966-111">The decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="71966-112">Notes</span><span class="sxs-lookup"><span data-stu-id="71966-112">Remarks</span></span>

<span data-ttu-id="71966-113">L’encodage Base64 est le schéma utilisé pour transmettre des données binaires.</span><span class="sxs-lookup"><span data-stu-id="71966-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="71966-114">Base64 traite les données en tant que groupes 24 bits, en mappant ces données à quatre caractères encodés.</span><span class="sxs-lookup"><span data-stu-id="71966-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="71966-115">L’encodage Base64 est parfois appelé encodage 3 à 4.</span><span class="sxs-lookup"><span data-stu-id="71966-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="71966-116">Chaque 6 bits du groupe 24 bits est utilisé comme index dans une table de mappage (l’alphabet base64) pour obtenir un caractère pour les données encodées.</span><span class="sxs-lookup"><span data-stu-id="71966-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="71966-117">Les données encodées ont des longueurs de ligne limitées à 76 caractères.</span><span class="sxs-lookup"><span data-stu-id="71966-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="71966-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71966-118">Requirements</span></span>



| <span data-ttu-id="71966-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71966-119">Requirement</span></span> | <span data-ttu-id="71966-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="71966-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71966-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="71966-121">Redistributable</span></span><br/> | <span data-ttu-id="71966-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="71966-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="71966-123">DLL</span><span class="sxs-lookup"><span data-stu-id="71966-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="71966-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71966-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71966-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71966-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71966-126">**Services**</span><span class="sxs-lookup"><span data-stu-id="71966-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




