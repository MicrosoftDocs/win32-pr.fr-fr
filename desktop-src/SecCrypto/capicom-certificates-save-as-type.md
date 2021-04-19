---
description: Définit le format d’un fichier contenant des informations sur les certificats.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Énumération CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520924"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a><span data-ttu-id="79d2b-103">L' \_ énumération des certificats CAPICOM \_ \_ en tant que \_ type</span><span class="sxs-lookup"><span data-stu-id="79d2b-103">CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="79d2b-104">Le type d’énumération des **\_ certificats CAPICOM \_ \_ en tant que \_** type définit le format d’un fichier contenant des informations sur les certificats.</span><span class="sxs-lookup"><span data-stu-id="79d2b-104">The **CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificates information.</span></span> <span data-ttu-id="79d2b-105">Ce type d’énumération a été introduit par CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="79d2b-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="79d2b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="79d2b-106">Members</span></span>



| <span data-ttu-id="79d2b-107">Membre</span><span class="sxs-lookup"><span data-stu-id="79d2b-107">Member</span></span>                                          | <span data-ttu-id="79d2b-108">Description</span><span class="sxs-lookup"><span data-stu-id="79d2b-108">Description</span></span>                                          | <span data-ttu-id="79d2b-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="79d2b-109">Value</span></span> |
|-------------------------------------------------|------------------------------------------------------|-------|
| <span data-ttu-id="79d2b-110">**\_certificats CAPICOM \_ enregistrés \_ sous forme \_ sérialisée**</span><span class="sxs-lookup"><span data-stu-id="79d2b-110">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</span></span> | <span data-ttu-id="79d2b-111">Les certificats enregistrés sont sérialisés.</span><span class="sxs-lookup"><span data-stu-id="79d2b-111">The saved certificates are serialized.</span></span><br/>    | <span data-ttu-id="79d2b-112">0</span><span class="sxs-lookup"><span data-stu-id="79d2b-112">0</span></span>     |
| <span data-ttu-id="79d2b-113">**\_Certificats CAPICOM \_ enregistrés \_ en tant que \_ PKCS7**</span><span class="sxs-lookup"><span data-stu-id="79d2b-113">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</span></span>      | <span data-ttu-id="79d2b-114">Les certificats sont enregistrés sous la forme d’un fichier PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="79d2b-114">The certificates are saved as a PKCS \#7.</span></span><br/> | <span data-ttu-id="79d2b-115">1</span><span class="sxs-lookup"><span data-stu-id="79d2b-115">1</span></span>     |
| <span data-ttu-id="79d2b-116">**\_certificats CAPICOM \_ Enregistrer \_ comme \_ pfx**</span><span class="sxs-lookup"><span data-stu-id="79d2b-116">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</span></span>        | <span data-ttu-id="79d2b-117">Les certificats sont enregistrés en tant que PFX.</span><span class="sxs-lookup"><span data-stu-id="79d2b-117">The certificates are saved as a PFX.</span></span><br/>      | <span data-ttu-id="79d2b-118">2</span><span class="sxs-lookup"><span data-stu-id="79d2b-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="79d2b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="79d2b-119">Remarks</span></span>

<span data-ttu-id="79d2b-120">Le \_ \_ \_ \_ type d’énumération certificats Save As type est utilisé par la méthode [**Certificates. Save**](certificates-save.md) .</span><span class="sxs-lookup"><span data-stu-id="79d2b-120">The CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration type is used by the [**Certificates.Save**](certificates-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="79d2b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79d2b-121">Requirements</span></span>



| <span data-ttu-id="79d2b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79d2b-122">Requirement</span></span> | <span data-ttu-id="79d2b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="79d2b-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79d2b-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="79d2b-124">Redistributable</span></span><br/> | <span data-ttu-id="79d2b-125">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="79d2b-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="79d2b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="79d2b-126">Header</span></span><br/>          | <dl> <span data-ttu-id="79d2b-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="79d2b-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




