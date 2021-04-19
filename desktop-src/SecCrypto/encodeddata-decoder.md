---
description: Obtient un objet décodeur, s’il en existe un.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: EncodedData. Decoder, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531053"
---
# <a name="encodeddatadecoder-method"></a><span data-ttu-id="60f81-103">EncodedData. Decoder, méthode</span><span class="sxs-lookup"><span data-stu-id="60f81-103">EncodedData.Decoder method</span></span>

<span data-ttu-id="60f81-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="60f81-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="60f81-105">Utilisez plutôt la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="60f81-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="60f81-106">La méthode de **décodeur** obtient un objet décodeur, s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="60f81-106">The **Decoder** method obtains a decoder object, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f81-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60f81-107">Syntax</span></span>


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a><span data-ttu-id="60f81-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60f81-108">Parameters</span></span>

<span data-ttu-id="60f81-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="60f81-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="60f81-110">Notes</span><span class="sxs-lookup"><span data-stu-id="60f81-110">Remarks</span></span>

<span data-ttu-id="60f81-111">Si les données encodées n’ont pas d’objet décodeur, la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="60f81-111">If the encoded data does not have a decoder object, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f81-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60f81-112">Requirements</span></span>



| <span data-ttu-id="60f81-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60f81-113">Requirement</span></span> | <span data-ttu-id="60f81-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="60f81-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60f81-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="60f81-115">End of client support</span></span><br/> | <span data-ttu-id="60f81-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60f81-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="60f81-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="60f81-117">End of server support</span></span><br/> | <span data-ttu-id="60f81-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60f81-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="60f81-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="60f81-119">Redistributable</span></span><br/>       | <span data-ttu-id="60f81-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="60f81-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="60f81-121">DLL</span><span class="sxs-lookup"><span data-stu-id="60f81-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="60f81-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60f81-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
