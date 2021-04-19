---
description: Représente le modèle d’extension de certificat du certificat.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Objet de modèle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544345"
---
# <a name="template-object"></a><span data-ttu-id="68188-103">Objet de modèle</span><span class="sxs-lookup"><span data-stu-id="68188-103">Template object</span></span>

<span data-ttu-id="68188-104">\[L’objet **modèle** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="68188-104">\[The **Template** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="68188-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="68188-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="68188-106">L’objet **modèle** représente le modèle d’extension de certificat du certificat.</span><span class="sxs-lookup"><span data-stu-id="68188-106">The **Template** object represents the certificate extension template of the certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="68188-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="68188-107">When to use</span></span>

<span data-ttu-id="68188-108">L’objet de **modèle** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="68188-108">The **Template** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="68188-109">Déterminez si le modèle est marqué comme critique ou présent.</span><span class="sxs-lookup"><span data-stu-id="68188-109">Determine whether the template is marked critical or present.</span></span>
-   <span data-ttu-id="68188-110">Récupérez l' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) ou le nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="68188-110">Retrieve the [*object identifier*](../secgloss/o-gly.md) (OID) or name of the template.</span></span>
-   <span data-ttu-id="68188-111">Récupérez la version mineure ou majeure du modèle.</span><span class="sxs-lookup"><span data-stu-id="68188-111">Retrieve the minor or major version of the template.</span></span>

## <a name="members"></a><span data-ttu-id="68188-112">Membres</span><span class="sxs-lookup"><span data-stu-id="68188-112">Members</span></span>

<span data-ttu-id="68188-113">L’objet de **modèle** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="68188-113">The **Template** object has these types of members:</span></span>

-   [<span data-ttu-id="68188-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68188-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68188-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68188-115">Properties</span></span>

<span data-ttu-id="68188-116">L’objet de **modèle** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="68188-116">The **Template** object has these properties.</span></span>



| <span data-ttu-id="68188-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="68188-117">Property</span></span>                                                 | <span data-ttu-id="68188-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="68188-118">Access type</span></span>          | <span data-ttu-id="68188-119">Description</span><span class="sxs-lookup"><span data-stu-id="68188-119">Description</span></span>                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68188-120">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="68188-120">**IsCritical**</span></span>](template-iscritical.md)<br/>     | <span data-ttu-id="68188-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68188-121">Read-only</span></span><br/> | <span data-ttu-id="68188-122">Récupère une valeur booléenne qui indique si l’extension de modèle est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="68188-122">Retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="68188-123">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="68188-123">**IsPresent**</span></span>](template-ispresent.md)<br/>       | <span data-ttu-id="68188-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68188-124">Read-only</span></span><br/> | <span data-ttu-id="68188-125">Récupère une valeur booléenne qui indique si l’extension de modèle est présente.</span><span class="sxs-lookup"><span data-stu-id="68188-125">Retrieves a Boolean value that indicates whether the template extension is present.</span></span><br/>         |
| [<span data-ttu-id="68188-126">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="68188-126">**MajorVersion**</span></span>](template-majorversion.md)<br/> | <span data-ttu-id="68188-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68188-127">Read-only</span></span><br/> | <span data-ttu-id="68188-128">Récupère le numéro de version principale du modèle.</span><span class="sxs-lookup"><span data-stu-id="68188-128">Retrieves the major version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="68188-129">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="68188-129">**MinorVersion**</span></span>](template-minorversion.md)<br/> | <span data-ttu-id="68188-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68188-130">Read-only</span></span><br/> | <span data-ttu-id="68188-131">Récupère le numéro de version mineure du modèle.</span><span class="sxs-lookup"><span data-stu-id="68188-131">Retrieves the minor version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="68188-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="68188-132">**Name**</span></span>](template-name.md)<br/>                 | <span data-ttu-id="68188-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68188-133">Read-only</span></span><br/> | <span data-ttu-id="68188-134">Récupère une chaîne qui contient le nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="68188-134">Retrieves a string that contains the name of the template.</span></span><br/>                                  |
| [<span data-ttu-id="68188-135">**OID**</span><span class="sxs-lookup"><span data-stu-id="68188-135">**OID**</span></span>](template-oid.md)<br/>                   | <span data-ttu-id="68188-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68188-136">Read-only</span></span><br/> | <span data-ttu-id="68188-137">Récupère un objet [**OID**](oid.md) qui identifie l’objet de **modèle** .</span><span class="sxs-lookup"><span data-stu-id="68188-137">Retrieves an [**OID**](oid.md) object that identifies the **Template** object.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="68188-138">Notes</span><span class="sxs-lookup"><span data-stu-id="68188-138">Remarks</span></span>

<span data-ttu-id="68188-139">Impossible de créer l’objet de **modèle** .</span><span class="sxs-lookup"><span data-stu-id="68188-139">The **Template** object cannot be created.</span></span>

<span data-ttu-id="68188-140">Un objet **modèle** est retourné par la méthode [**Certificate. Template**](certificate-template.md) .</span><span class="sxs-lookup"><span data-stu-id="68188-140">A **Template** object is returned by the [**Certificate.Template**](certificate-template.md) method.</span></span>

<span data-ttu-id="68188-141">CAPICOM utilise deux versions différentes de modèles de certificats.</span><span class="sxs-lookup"><span data-stu-id="68188-141">CAPICOM uses two different versions of certificate templates.</span></span> <span data-ttu-id="68188-142">Le tableau suivant indique le nom et l’OID de chaque version de modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="68188-142">The following table shows the name and OID for each certificate template version.</span></span>



| <span data-ttu-id="68188-143">Version</span><span class="sxs-lookup"><span data-stu-id="68188-143">Version</span></span> | <span data-ttu-id="68188-144">Nom</span><span class="sxs-lookup"><span data-stu-id="68188-144">Name</span></span>                               | <span data-ttu-id="68188-145">OID</span><span class="sxs-lookup"><span data-stu-id="68188-145">OID</span></span>                    |
|---------|------------------------------------|------------------------|
| <span data-ttu-id="68188-146">V1</span><span class="sxs-lookup"><span data-stu-id="68188-146">V1</span></span>      | <span data-ttu-id="68188-147">EXTENSION szOID d' \_ inscription \_ le type \_</span><span class="sxs-lookup"><span data-stu-id="68188-147">szOID\_ENROLL\_CERTTYPE\_EXTENSION</span></span> | <span data-ttu-id="68188-148">"1.3.6.1.4.1.311.20.2"</span><span class="sxs-lookup"><span data-stu-id="68188-148">"1.3.6.1.4.1.311.20.2"</span></span> |
| <span data-ttu-id="68188-149">V2</span><span class="sxs-lookup"><span data-stu-id="68188-149">V2</span></span>      | <span data-ttu-id="68188-150">\_modèle de certificat szOID \_</span><span class="sxs-lookup"><span data-stu-id="68188-150">szOID\_CERTIFICATE\_TEMPLATE</span></span>       | <span data-ttu-id="68188-151">"1.3.6.1.4.1.311.21.7"</span><span class="sxs-lookup"><span data-stu-id="68188-151">"1.3.6.1.4.1.311.21.7"</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="68188-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68188-152">Requirements</span></span>



| <span data-ttu-id="68188-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68188-153">Requirement</span></span> | <span data-ttu-id="68188-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="68188-154">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68188-155">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="68188-155">Redistributable</span></span><br/> | <span data-ttu-id="68188-156">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="68188-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="68188-157">DLL</span><span class="sxs-lookup"><span data-stu-id="68188-157">DLL</span></span><br/>             | <dl> <span data-ttu-id="68188-158"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68188-158"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
