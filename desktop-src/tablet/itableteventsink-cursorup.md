---
description: Se produit lorsque l’utilisateur a relâché le stylet à partir de la surface du digitaliseur de tablette.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'ITabletEventSink :: CursorUp, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210616"
---
# <a name="itableteventsinkcursorup-method"></a><span data-ttu-id="9bcc0-103">ITabletEventSink :: CursorUp, méthode</span><span class="sxs-lookup"><span data-stu-id="9bcc0-103">ITabletEventSink::CursorUp method</span></span>

<span data-ttu-id="9bcc0-104">Se produit lorsque l’utilisateur a relâché le stylet à partir de la surface du digitaliseur de tablette.</span><span class="sxs-lookup"><span data-stu-id="9bcc0-104">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bcc0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9bcc0-105">Syntax</span></span>


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="9bcc0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bcc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bcc0-107">*TCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bcc0-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bcc0-108">Identificateur de la tablette.</span><span class="sxs-lookup"><span data-stu-id="9bcc0-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="9bcc0-109">*CID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bcc0-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bcc0-110">Identificateur du stylet.</span><span class="sxs-lookup"><span data-stu-id="9bcc0-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="9bcc0-111">*nSerialNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bcc0-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bcc0-112">Numéro de série du stylet.</span><span class="sxs-lookup"><span data-stu-id="9bcc0-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="9bcc0-113">*cbPkt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bcc0-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bcc0-114">Nombre d’octets dans un paquet de données de stylet.</span><span class="sxs-lookup"><span data-stu-id="9bcc0-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="9bcc0-115">*pbPkt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bcc0-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bcc0-116">Données du stylet indiquant l’emplacement où le stylet a été levé de la tablette.</span><span class="sxs-lookup"><span data-stu-id="9bcc0-116">The stylus data indicating the location where the stylus was lifted from the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bcc0-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9bcc0-117">Return value</span></span>

<span data-ttu-id="9bcc0-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9bcc0-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9bcc0-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9bcc0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bcc0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bcc0-120">Requirements</span></span>



| <span data-ttu-id="9bcc0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bcc0-121">Requirement</span></span> | <span data-ttu-id="9bcc0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bcc0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcc0-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bcc0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9bcc0-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9bcc0-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9bcc0-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bcc0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9bcc0-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bcc0-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9bcc0-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9bcc0-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="9bcc0-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9bcc0-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcc0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bcc0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcc0-130">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="9bcc0-130">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




