---
description: Représente une propriété d’utilisation améliorée de la clé (EKU) d’un certificat.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: Objet EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531060"
---
# <a name="eku-object"></a><span data-ttu-id="8f720-103">Objet EKU</span><span class="sxs-lookup"><span data-stu-id="8f720-103">EKU object</span></span>

<span data-ttu-id="8f720-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f720-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8f720-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="8f720-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8f720-106">L’objet **EKU** représente une propriété unique de l’utilisation de la clé étendue (EKU) d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="8f720-106">The **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="8f720-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8f720-107">Members</span></span>

<span data-ttu-id="8f720-108">L’objet **EKU** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8f720-108">The **EKU** object has these types of members:</span></span>

-   [<span data-ttu-id="8f720-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f720-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f720-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f720-110">Properties</span></span>

<span data-ttu-id="8f720-111">L’objet **EKU** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8f720-111">The **EKU** object has these properties.</span></span>



| <span data-ttu-id="8f720-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="8f720-112">Property</span></span>                            | <span data-ttu-id="8f720-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="8f720-113">Access type</span></span>           | <span data-ttu-id="8f720-114">Description</span><span class="sxs-lookup"><span data-stu-id="8f720-114">Description</span></span>                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f720-115">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8f720-115">**Name**</span></span>](eku-name.md)<br/> | <span data-ttu-id="8f720-116">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f720-116">Read/write</span></span><br/> | <span data-ttu-id="8f720-117">Définit ou récupère une valeur d’énumération qui spécifie le nom CAPICOM de l’utilisation améliorée de la valeur.</span><span class="sxs-lookup"><span data-stu-id="8f720-117">Sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="8f720-118">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f720-118">This is the default property.</span></span><br/>                                                                                   |
| [<span data-ttu-id="8f720-119">**OID**</span><span class="sxs-lookup"><span data-stu-id="8f720-119">**OID**</span></span>](eku-oid.md)<br/>   | <span data-ttu-id="8f720-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f720-120">Read/write</span></span><br/> | <span data-ttu-id="8f720-121">Définit ou récupère une chaîne qui contient une valeur de chaîne d' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) EKU telle que définie dans wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="8f720-121">Sets or retrieves a string that contains an EKU [*object identifier*](../secgloss/o-gly.md) (OID) string value as defined in Wincrypt.h.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f720-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8f720-122">Remarks</span></span>

<span data-ttu-id="8f720-123">L’objet **EKU** est utilisé par la collection et la propriété suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f720-123">The **EKU** object is used by the following collection and property:</span></span>

-   <span data-ttu-id="8f720-124">Collection de [**EKU**](ekus.md)</span><span class="sxs-lookup"><span data-stu-id="8f720-124">[**EKUs**](ekus.md) collection</span></span>
-   <span data-ttu-id="8f720-125">[**CertificateStatus. EKU,**](certificatestatus-eku.md) propriété</span><span class="sxs-lookup"><span data-stu-id="8f720-125">[**CertificateStatus.EKU**](certificatestatus-eku.md) property</span></span>

<span data-ttu-id="8f720-126">Impossible de créer l’objet **EKU** .</span><span class="sxs-lookup"><span data-stu-id="8f720-126">The **EKU** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f720-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f720-127">Requirements</span></span>



| <span data-ttu-id="8f720-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f720-128">Requirement</span></span> | <span data-ttu-id="8f720-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f720-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f720-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8f720-130">End of client support</span></span><br/> | <span data-ttu-id="8f720-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f720-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8f720-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8f720-132">End of server support</span></span><br/> | <span data-ttu-id="8f720-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f720-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8f720-134">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8f720-134">Redistributable</span></span><br/>       | <span data-ttu-id="8f720-135">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f720-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8f720-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8f720-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8f720-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f720-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
