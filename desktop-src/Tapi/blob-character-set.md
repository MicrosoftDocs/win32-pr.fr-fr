---
description: L' \_ énumération du jeu de caractères BLOB \_ indique le jeu de caractères utilisé par l’objet blob de conférence actuel.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Énumération BLOB_CHARACTER_SET (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533101"
---
# <a name="blob_character_set-enumeration"></a><span data-ttu-id="6fdcf-103">\_Énumération du jeu de caractères BLOB \_</span><span class="sxs-lookup"><span data-stu-id="6fdcf-103">BLOB\_CHARACTER\_SET enumeration</span></span>

<span data-ttu-id="6fdcf-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6fdcf-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6fdcf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6fdcf-106">L’énumération du **\_ \_ jeu de caractères BLOB** indique le jeu de caractères utilisé par l’objet blob de conférence actuel.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-106">The **BLOB\_CHARACTER\_SET** enum indicates the character set used by the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdcf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fdcf-107">Syntax</span></span>


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a><span data-ttu-id="6fdcf-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6fdcf-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6fdcf-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**\_ASCII BCS**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-109"><span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS\_ASCII**</span></span>
</dt> <dd>

<span data-ttu-id="6fdcf-110">Format ASCII standard.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-110">Standard ASCII format.</span></span>

</dd> <dt>

<span data-ttu-id="6fdcf-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**UTF7 pour BCS \_**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-111"><span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS\_UTF7**</span></span>
</dt> <dd>

<span data-ttu-id="6fdcf-112">Format de transformation 7 bits Unicode.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-112">Seven-bit transformation format of Unicode.</span></span> <span data-ttu-id="6fdcf-113">Pour plus d’informations sur ce format, lancez une recherche sur Internet pour la RFC 1642.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-113">For details on this format, conduct an Internet search for RFC 1642.</span></span>

</dd> <dt>

<span data-ttu-id="6fdcf-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**SBC \_ UTF8**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-114"><span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS\_UTF8**</span></span>
</dt> <dd>

<span data-ttu-id="6fdcf-115">Format de transformation UCS 8.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-115">UCS Transformation Format 8.</span></span> <span data-ttu-id="6fdcf-116">Pour plus d’informations sur ce format, lancez une recherche sur Internet ISO (le Organisation internationale de normalisation) et IEC (le Commission Électrotechnique Internationale) document ISO/IEC JTC1/SC2/WG2 N 1036, datée du 1er août 1994, par WG2 Project Editor.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-116">For details on this format, conduct an Internet search for ISO (the International Organization for Standardization) and IEC (the International Electrotechnical Commission) document ISO/IEC JTC1/SC2/WG2 N 1036, dated August 1, 1994, by WG2 Project Editor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fdcf-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fdcf-117">Requirements</span></span>



| <span data-ttu-id="6fdcf-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fdcf-118">Requirement</span></span> | <span data-ttu-id="6fdcf-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fdcf-119">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdcf-120">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6fdcf-120">TAPI version</span></span><br/> | <span data-ttu-id="6fdcf-121">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6fdcf-121">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="6fdcf-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fdcf-122">Header</span></span><br/>       | <dl> <span data-ttu-id="6fdcf-123"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fdcf-123"><dt>Sdpblb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fdcf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fdcf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fdcf-125">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-125">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[<span data-ttu-id="6fdcf-126">**Obtient \_ CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-126">**get\_CharacterSet**</span></span>](itconferenceblob-get-characterset.md)
</dt> <dt>

[<span data-ttu-id="6fdcf-127">**Rein**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-127">**Init**</span></span>](itconferenceblob-init.md)
</dt> <dt>

[<span data-ttu-id="6fdcf-128">**SetConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-128">**SetConferenceBlob**</span></span>](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




