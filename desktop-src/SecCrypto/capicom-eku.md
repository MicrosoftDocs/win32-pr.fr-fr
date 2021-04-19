---
description: Définit les noms de l’utilisation de la clé étendue en fonction de l’emplacement où ils peuvent être utilisés.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: Énumération CAPICOM_EKU (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539664"
---
# <a name="capicom_eku-enumeration"></a><span data-ttu-id="8fb80-103">CAPICOM \_ , énumération EKU</span><span class="sxs-lookup"><span data-stu-id="8fb80-103">CAPICOM\_EKU enumeration</span></span>

<span data-ttu-id="8fb80-104">Le type d’énumération **\_ EKU** d’un CAPICOM définit les noms de l’utilisation de la clé étendue en fonction de l’endroit où ils peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="8fb80-104">The **CAPICOM\_EKU** enumeration type defines the extended key usage names based on where they can be used.</span></span>

## <a name="members"></a><span data-ttu-id="8fb80-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8fb80-105">Members</span></span>



| <span data-ttu-id="8fb80-106">Membre</span><span class="sxs-lookup"><span data-stu-id="8fb80-106">Member</span></span>                                     | <span data-ttu-id="8fb80-107">Description</span><span class="sxs-lookup"><span data-stu-id="8fb80-107">Description</span></span>                                                                                                                                                 | <span data-ttu-id="8fb80-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fb80-108">Value</span></span> |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="8fb80-109">**\_autre utilisation améliorée de la EKU \_**</span><span class="sxs-lookup"><span data-stu-id="8fb80-109">**CAPICOM\_EKU\_OTHER**</span></span>                    | <span data-ttu-id="8fb80-110">Le certificat utilise le défini dans la stratégie locale.</span><span class="sxs-lookup"><span data-stu-id="8fb80-110">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="8fb80-111">Utilisé si l’utilisation améliorée de la valeur requise n’est pas prédéfinie et que la valeur OID doit être définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="8fb80-111">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> | <span data-ttu-id="8fb80-112">0</span><span class="sxs-lookup"><span data-stu-id="8fb80-112">0</span></span>     |
| <span data-ttu-id="8fb80-113">**authentification du serveur de l' \_ utilisation améliorée de la EKU CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fb80-113">**CAPICOM\_EKU\_SERVER\_AUTH**</span></span>             | <span data-ttu-id="8fb80-114">Le certificat peut être utilisé pour authentifier un serveur.</span><span class="sxs-lookup"><span data-stu-id="8fb80-114">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                | <span data-ttu-id="8fb80-115">1</span><span class="sxs-lookup"><span data-stu-id="8fb80-115">1</span></span>     |
| <span data-ttu-id="8fb80-116">**authentification du client de l' \_ utilisation améliorée de la EKU CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fb80-116">**CAPICOM\_EKU\_CLIENT\_AUTH**</span></span>             | <span data-ttu-id="8fb80-117">Le certificat peut être utilisé pour authentifier un client.</span><span class="sxs-lookup"><span data-stu-id="8fb80-117">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                | <span data-ttu-id="8fb80-118">2</span><span class="sxs-lookup"><span data-stu-id="8fb80-118">2</span></span>     |
| <span data-ttu-id="8fb80-119">**signature du code de l' \_ utilisation améliorée de la \_ \_ connexion**</span><span class="sxs-lookup"><span data-stu-id="8fb80-119">**CAPICOM\_EKU\_CODE\_SIGNING**</span></span>            | <span data-ttu-id="8fb80-120">Le certificat peut être utilisé pour créer une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="8fb80-120">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           | <span data-ttu-id="8fb80-121">3</span><span class="sxs-lookup"><span data-stu-id="8fb80-121">3</span></span>     |
| <span data-ttu-id="8fb80-122">**\_protection par e-mail de l’utilisation améliorée de la \_ sécurité pour CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="8fb80-122">**CAPICOM\_EKU\_EMAIL\_PROTECTION**</span></span>        | <span data-ttu-id="8fb80-123">Le certificat peut être utilisé pour la protection de la messagerie.</span><span class="sxs-lookup"><span data-stu-id="8fb80-123">Certificate can be used for email protection.</span></span><br/>                                                                                                    | <span data-ttu-id="8fb80-124">4</span><span class="sxs-lookup"><span data-stu-id="8fb80-124">4</span></span>     |
| <span data-ttu-id="8fb80-125">**\_connexion par carte à \_ puce pour CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="8fb80-125">**CAPICOM\_EKU\_SMARTCARD\_LOGON**</span></span>         | <span data-ttu-id="8fb80-126">Le certificat peut être utilisé pour l’ouverture de session par carte à puce.</span><span class="sxs-lookup"><span data-stu-id="8fb80-126">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="8fb80-127">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="8fb80-127">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         | <span data-ttu-id="8fb80-128">5</span><span class="sxs-lookup"><span data-stu-id="8fb80-128">5</span></span>     |
| <span data-ttu-id="8fb80-129">**\_système de fichiers de \_ chiffrement \_ EKU \_ de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="8fb80-129">**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</span></span> | <span data-ttu-id="8fb80-130">Le certificat peut être utilisé pour EFS.</span><span class="sxs-lookup"><span data-stu-id="8fb80-130">Certificate can be used for EFS.</span></span> <span data-ttu-id="8fb80-131">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="8fb80-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      | <span data-ttu-id="8fb80-132">6</span><span class="sxs-lookup"><span data-stu-id="8fb80-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="8fb80-133">Notes</span><span class="sxs-lookup"><span data-stu-id="8fb80-133">Remarks</span></span>

<span data-ttu-id="8fb80-134">Le type d’énumération **\_ EKU CAPICOM** est utilisé par l' [**utilisation améliorée de la EKU. Propriété Name**](eku-name.md) .</span><span class="sxs-lookup"><span data-stu-id="8fb80-134">The **CAPICOM\_EKU** enumeration type is used by the [**EKU.Name**](eku-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb80-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fb80-135">Requirements</span></span>



| <span data-ttu-id="8fb80-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fb80-136">Requirement</span></span> | <span data-ttu-id="8fb80-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fb80-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb80-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8fb80-138">Redistributable</span></span><br/> | <span data-ttu-id="8fb80-139">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="8fb80-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="8fb80-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fb80-140">Header</span></span><br/>          | <dl> <span data-ttu-id="8fb80-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb80-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 




