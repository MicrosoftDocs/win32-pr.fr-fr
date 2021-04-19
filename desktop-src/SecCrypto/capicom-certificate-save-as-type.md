---
description: Définit le format d’un fichier contenant des informations de certificat.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Énumération CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526090"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a><span data-ttu-id="acc97-103">\_Énumération du certificat \_ CAPICOM \_ en tant que \_ type</span><span class="sxs-lookup"><span data-stu-id="acc97-103">CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="acc97-104">Le type d’énumération du **\_ certificat CAPICOM \_ \_ en tant que \_** type définit le format d’un fichier contenant les informations de certificat.</span><span class="sxs-lookup"><span data-stu-id="acc97-104">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificate information.</span></span> <span data-ttu-id="acc97-105">Ce type d’énumération a été introduit par CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="acc97-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="acc97-106">Membres</span><span class="sxs-lookup"><span data-stu-id="acc97-106">Members</span></span>



| <span data-ttu-id="acc97-107">Membre</span><span class="sxs-lookup"><span data-stu-id="acc97-107">Member</span></span>                                  | <span data-ttu-id="acc97-108">Description</span><span class="sxs-lookup"><span data-stu-id="acc97-108">Description</span></span>                                                                                                                                   | <span data-ttu-id="acc97-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="acc97-109">Value</span></span> |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="acc97-110">**\_certificat CAPICOM \_ enregistré \_ en tant que \_ pfx**</span><span class="sxs-lookup"><span data-stu-id="acc97-110">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</span></span> | <span data-ttu-id="acc97-111">Le fichier de sortie sera formaté en tant que fichier PFX (PKCS 12) et toutes les clés privées associées qui peuvent être exportées seront également enregistrées.</span><span class="sxs-lookup"><span data-stu-id="acc97-111">The output file will be formatted as a PFX (PKCS 12) file and any associated private keys which are exportable will also be saved.</span></span><br/> | <span data-ttu-id="acc97-112">0</span><span class="sxs-lookup"><span data-stu-id="acc97-112">0</span></span>     |
| <span data-ttu-id="acc97-113">**\_certificat CAPICOM \_ enregistré \_ comme \_ CER**</span><span class="sxs-lookup"><span data-stu-id="acc97-113">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</span></span> | <span data-ttu-id="acc97-114">Le fichier de sortie sera formaté en tant que fichier CER sans clé privée enregistrée.</span><span class="sxs-lookup"><span data-stu-id="acc97-114">The output file will be formatted as a CER file with no private keys saved.</span></span><br/>                                                        | <span data-ttu-id="acc97-115">1</span><span class="sxs-lookup"><span data-stu-id="acc97-115">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="acc97-116">Notes</span><span class="sxs-lookup"><span data-stu-id="acc97-116">Remarks</span></span>

<span data-ttu-id="acc97-117">Le type d’énumération du **\_ certificat CAPICOM \_ \_ en tant que \_** type est utilisé par la méthode [**Certificate. Save**](certificate-save.md) .</span><span class="sxs-lookup"><span data-stu-id="acc97-117">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="acc97-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acc97-118">Requirements</span></span>



| <span data-ttu-id="acc97-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acc97-119">Requirement</span></span> | <span data-ttu-id="acc97-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="acc97-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="acc97-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="acc97-121">Redistributable</span></span><br/> | <span data-ttu-id="acc97-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="acc97-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="acc97-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="acc97-123">Header</span></span><br/>          | <dl> <span data-ttu-id="acc97-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc97-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




