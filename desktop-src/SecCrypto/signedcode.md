---
description: Fournit des fonctionnalités pour la signature des fichiers exécutables avec une signature numérique Authenticode.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Objet SignedCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544490"
---
# <a name="signedcode-object"></a><span data-ttu-id="1b879-103">Objet SignedCode</span><span class="sxs-lookup"><span data-stu-id="1b879-103">SignedCode object</span></span>

<span data-ttu-id="1b879-104">\[L’objet **SignedCode** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1b879-104">\[The **SignedCode** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1b879-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="1b879-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="1b879-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="1b879-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="1b879-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="1b879-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="1b879-108">L’objet **SignedCode** fournit des fonctionnalités pour la signature des fichiers exécutables avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="1b879-108">The **SignedCode** object provides functionality for signing executable files with an Authenticode digital signature.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="1b879-109">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="1b879-109">When to use</span></span>

<span data-ttu-id="1b879-110">L’objet **SignedCode** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b879-110">The **SignedCode** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="1b879-111">Signez les fichiers exécutables.</span><span class="sxs-lookup"><span data-stu-id="1b879-111">Sign executable files.</span></span>
-   <span data-ttu-id="1b879-112">Horodatage des fichiers exécutables.</span><span class="sxs-lookup"><span data-stu-id="1b879-112">Time stamp executable files.</span></span>
-   <span data-ttu-id="1b879-113">Déterminez si la signature du fichier exécutable est valide.</span><span class="sxs-lookup"><span data-stu-id="1b879-113">Determine whether the signature of the executable file is valid.</span></span>
-   <span data-ttu-id="1b879-114">Définissez ou récupérez le chemin d’accès au fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="1b879-114">Set or retrieve the path to the executable file.</span></span>
-   <span data-ttu-id="1b879-115">Récupérez le signataire et la matrice temporelle du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="1b879-115">Retrieve the signer and time stamper of the executable file.</span></span>
-   <span data-ttu-id="1b879-116">Récupérez une collection de certificats pour le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="1b879-116">Retrieve a collection of the certificates for the executable file.</span></span>
-   <span data-ttu-id="1b879-117">Récupérez une description ou l’URL de la description du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="1b879-117">Retrieve a description or the URL to the description of the executable file.</span></span>

## <a name="members"></a><span data-ttu-id="1b879-118">Membres</span><span class="sxs-lookup"><span data-stu-id="1b879-118">Members</span></span>

<span data-ttu-id="1b879-119">L’objet **SignedCode** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1b879-119">The **SignedCode** object has these types of members:</span></span>

-   [<span data-ttu-id="1b879-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b879-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="1b879-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1b879-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1b879-122">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b879-122">Methods</span></span>

<span data-ttu-id="1b879-123">L’objet **SignedCode** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1b879-123">The **SignedCode** object has these methods.</span></span>



| <span data-ttu-id="1b879-124">Méthode</span><span class="sxs-lookup"><span data-stu-id="1b879-124">Method</span></span>                                    | <span data-ttu-id="1b879-125">Description</span><span class="sxs-lookup"><span data-stu-id="1b879-125">Description</span></span>                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b879-126">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1b879-126">**Sign**</span></span>](signedcode-sign.md)           | <span data-ttu-id="1b879-127">Crée une signature numérique Authenticode et signe le fichier exécutable spécifié dans la propriété [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="1b879-127">Creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>    |
| [<span data-ttu-id="1b879-128">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="1b879-128">**Timestamp**</span></span>](signedcode-timestamp.md) | <span data-ttu-id="1b879-129">Crée une signature d’horodatage Authenticode sur le fichier exécutable signé spécifié dans la propriété [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="1b879-129">Creates an Authenticode time stamp signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/> |
| [<span data-ttu-id="1b879-130">**Vérifier**</span><span class="sxs-lookup"><span data-stu-id="1b879-130">**Verify**</span></span>](signedcode-verify.md)       | <span data-ttu-id="1b879-131">Vérifie la signature Authenticode sur le fichier exécutable signé spécifié dans la propriété [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="1b879-131">Verifies the Authenticode signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="1b879-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1b879-132">Properties</span></span>

<span data-ttu-id="1b879-133">L’objet **SignedCode** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1b879-133">The **SignedCode** object has these properties.</span></span>



| <span data-ttu-id="1b879-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="1b879-134">Property</span></span>                                                       | <span data-ttu-id="1b879-135">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="1b879-135">Access type</span></span>           | <span data-ttu-id="1b879-136">Description</span><span class="sxs-lookup"><span data-stu-id="1b879-136">Description</span></span>                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b879-137">**Certificats**</span><span class="sxs-lookup"><span data-stu-id="1b879-137">**Certificates**</span></span>](signedcode-certificates.md)<br/>     | <span data-ttu-id="1b879-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b879-138">Read-only</span></span><br/>  | <span data-ttu-id="1b879-139">Collection de [**certificats**](certificates.md) qui contient tous les certificats dans le fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="1b879-139">A [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span><br/>             |
| [<span data-ttu-id="1b879-140">**Description**</span><span class="sxs-lookup"><span data-stu-id="1b879-140">**Description**</span></span>](signedcode-description.md)<br/>       | <span data-ttu-id="1b879-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1b879-141">Read/write</span></span><br/> | <span data-ttu-id="1b879-142">Chaîne qui contient une description du fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="1b879-142">A string that contains a description of the signed executable file.</span></span><br/>                                                             |
| [<span data-ttu-id="1b879-143">**DescriptionURL**</span><span class="sxs-lookup"><span data-stu-id="1b879-143">**DescriptionURL**</span></span>](signedcode-descriptionurl.md)<br/> | <span data-ttu-id="1b879-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1b879-144">Read/write</span></span><br/> | <span data-ttu-id="1b879-145">Chaîne qui contient l’adresse HTTP à une description du fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="1b879-145">A string that contains the HTTP address to a description of the signed executable file.</span></span><br/>                                         |
| [<span data-ttu-id="1b879-146">**FileName**</span><span class="sxs-lookup"><span data-stu-id="1b879-146">**FileName**</span></span>](signedcode-filename.md)<br/>             | <span data-ttu-id="1b879-147">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1b879-147">Read/write</span></span><br/> | <span data-ttu-id="1b879-148">Chaîne qui contient le chemin d’accès au fichier de contenu qui contient le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="1b879-148">A string that contains the path to the content file that contains the executable file.</span></span><br/> <span data-ttu-id="1b879-149">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b879-149">This is the default property.</span></span><br/> |
| [<span data-ttu-id="1b879-150">**Signataire**</span><span class="sxs-lookup"><span data-stu-id="1b879-150">**Signer**</span></span>](signedcode-signer.md)<br/>                 | <span data-ttu-id="1b879-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b879-151">Read-only</span></span><br/>  | <span data-ttu-id="1b879-152">Objet [**signataire**](signer.md) qui fournit l’accès au signataire du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="1b879-152">A [**Signer**](signer.md) object that provides access to the signer of the executable file.</span></span><br/>                                    |
| [<span data-ttu-id="1b879-153">**Timestamper**</span><span class="sxs-lookup"><span data-stu-id="1b879-153">**Timestamper**</span></span>](signedcode-timestamper.md)<br/>       | <span data-ttu-id="1b879-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1b879-154">Read-only</span></span><br/>  | <span data-ttu-id="1b879-155">Objet [**signataire**](signer.md) qui fournit l’accès à l’horodatage du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="1b879-155">A [**Signer**](signer.md) object that provides access to the time stamper of the executable file.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="1b879-156">Notes</span><span class="sxs-lookup"><span data-stu-id="1b879-156">Remarks</span></span>

<span data-ttu-id="1b879-157">L’objet **SignedCode** peut être créé et n’est pas sûr pour l’écriture de scripts.</span><span class="sxs-lookup"><span data-stu-id="1b879-157">The **SignedCode** object can be created, and is not safe for scripting.</span></span> <span data-ttu-id="1b879-158">Le ProgID de l’objet **SignedCode** est CAPICOM. SignedCode. 1.</span><span class="sxs-lookup"><span data-stu-id="1b879-158">The ProgID for the **SignedCode** object is CAPICOM.SignedCode.1.</span></span>

<span data-ttu-id="1b879-159">Le fichier exécutable doit être d’un type qui peut être signé avec la technologie Authenticode, par exemple, des fichiers qui ont une extension de nom de fichier. cab,. cat,. exe,. dll,. vbs ou. ocx.</span><span class="sxs-lookup"><span data-stu-id="1b879-159">The executable file should be of a type that can be signed with Authenticode technology, for example, files that have a file name extension of .cab, .cat, .exe, .dll, .vbs, or .ocx.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b879-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b879-160">Requirements</span></span>



| <span data-ttu-id="1b879-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b879-161">Requirement</span></span> | <span data-ttu-id="1b879-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b879-162">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b879-163">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1b879-163">Redistributable</span></span><br/> | <span data-ttu-id="1b879-164">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="1b879-164">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1b879-165">DLL</span><span class="sxs-lookup"><span data-stu-id="1b879-165">DLL</span></span><br/>             | <dl> <span data-ttu-id="1b879-166"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b879-166"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
