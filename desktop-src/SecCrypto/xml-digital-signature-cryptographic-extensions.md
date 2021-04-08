---
description: CryptXML permet aux développeurs d’étendre les algorithmes de chiffrement pris en charge en mode natif en inscrivant une DLL d’extension de chiffrement à l’ensemble du système.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Extensions de chiffrement de signature numérique XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869329"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a><span data-ttu-id="d3da4-103">Extensions de chiffrement de signature numérique XML</span><span class="sxs-lookup"><span data-stu-id="d3da4-103">XML Digital Signature Cryptographic Extensions</span></span>

<span data-ttu-id="d3da4-104">CryptXML permet aux développeurs d’étendre les algorithmes de chiffrement pris en charge en mode natif en inscrivant une DLL d’extension de chiffrement à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="d3da4-104">CryptXML allows developers to extend natively supported cryptographic algorithms by registering a system wide cryptographic extension DLL.</span></span> <span data-ttu-id="d3da4-105">Les dll d’extension étendent les algorithmes pris en charge par les éléments XML **SignatureMethod** et **DigestMethod** .</span><span class="sxs-lookup"><span data-stu-id="d3da4-105">Extension DLLs extend the algorithms supported by **SignatureMethod** and **DigestMethod** XML elements.</span></span> <span data-ttu-id="d3da4-106">Les dll d’extension peuvent prendre en charge des algorithmes qui encodent des paramètres supplémentaires dans la signature numérique XML.</span><span class="sxs-lookup"><span data-stu-id="d3da4-106">Extension DLLs can support algorithms that encode additional parameters into the XML digital signature.</span></span>

<span data-ttu-id="d3da4-107">Toutes les dll d’extension doivent prendre en charge la fonction [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , qui retourne un pointeur vers une structure d' [**\_ \_ \_ interface de chiffrement XML énigmatique**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) .</span><span class="sxs-lookup"><span data-stu-id="d3da4-107">All extensions DLLs must support the [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) function, which returns a pointer to a [**CRYPT\_XML\_CRYPTOGRAPHIC\_INTERFACE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) structure.</span></span> <span data-ttu-id="d3da4-108">Cette structure fournit des pointeurs de fonction vers les fonctions d’extension de chiffrement implémentées.</span><span class="sxs-lookup"><span data-stu-id="d3da4-108">This structure provides function pointers to implemented cryptographic extension functions.</span></span> <span data-ttu-id="d3da4-109">Les fonctions prises en charge dépendent du type d’algorithme de chiffrement pris en charge et de la nécessité de coder les paramètres dans la signature numérique XML.</span><span class="sxs-lookup"><span data-stu-id="d3da4-109">The functions supported depend on the type of cryptographic algorithm supported and whether the algorithm must encode parameters into the XML digital signature.</span></span>

<span data-ttu-id="d3da4-110">Les fonctions d’extensions de chiffrement incluent les pointeurs de fonction suivants :</span><span class="sxs-lookup"><span data-stu-id="d3da4-110">Cryptographic extensions functions include the following function pointers:</span></span>

<dl> <dt>

<span data-ttu-id="d3da4-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Fonctions requises</span><span class="sxs-lookup"><span data-stu-id="d3da4-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Required functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="d3da4-112">**CryptXmlDllGetInterface**</span><span class="sxs-lookup"><span data-stu-id="d3da4-112">**CryptXmlDllGetInterface**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [<span data-ttu-id="d3da4-113">**CryptXmlDllGetAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="d3da4-113">**CryptXmlDllGetAlgorithmInfo**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span data-ttu-id="d3da4-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Fonctions de méthode Digest</span><span class="sxs-lookup"><span data-stu-id="d3da4-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest Method functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="d3da4-115">**CryptXmlDllCloseDigest**</span><span class="sxs-lookup"><span data-stu-id="d3da4-115">**CryptXmlDllCloseDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [<span data-ttu-id="d3da4-116">**CryptXmlDllCreateDigest**</span><span class="sxs-lookup"><span data-stu-id="d3da4-116">**CryptXmlDllCreateDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [<span data-ttu-id="d3da4-117">**CryptXmlDllDigestData**</span><span class="sxs-lookup"><span data-stu-id="d3da4-117">**CryptXmlDllDigestData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [<span data-ttu-id="d3da4-118">**CryptXmlDllFinalizeDigest**</span><span class="sxs-lookup"><span data-stu-id="d3da4-118">**CryptXmlDllFinalizeDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span data-ttu-id="d3da4-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Fonctions de méthode de signature</span><span class="sxs-lookup"><span data-stu-id="d3da4-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature Method Functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="d3da4-120">**CryptXmlDllSignData**</span><span class="sxs-lookup"><span data-stu-id="d3da4-120">**CryptXmlDllSignData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [<span data-ttu-id="d3da4-121">**CryptXmlDllVerifySignature**</span><span class="sxs-lookup"><span data-stu-id="d3da4-121">**CryptXmlDllVerifySignature**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [<span data-ttu-id="d3da4-122">**CryptXmlDllCreateKey**</span><span class="sxs-lookup"><span data-stu-id="d3da4-122">**CryptXmlDllCreateKey**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [<span data-ttu-id="d3da4-123">**CryptXmlDllEncodeKeyValue**</span><span class="sxs-lookup"><span data-stu-id="d3da4-123">**CryptXmlDllEncodeKeyValue**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span data-ttu-id="d3da4-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Pour les algorithmes avec des paramètres encodés par défaut</span><span class="sxs-lookup"><span data-stu-id="d3da4-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>For algorithms with default encoded parameters</span></span>
</dt> <dd>

-   [<span data-ttu-id="d3da4-125">**CryptXmlDllEncodeAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="d3da4-125">**CryptXmlDllEncodeAlgorithm**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

<span data-ttu-id="d3da4-126">Les dll d’extension de chiffrement sont inscrites à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="d3da4-126">Cryptographic extension DLLs are registered on a system-wide basis.</span></span> <span data-ttu-id="d3da4-127">Des privilèges d’administrateur sont nécessaires pour inscrire une DLL d’extension de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d3da4-127">Administrator privileges are required to register a cryptographic extension DLL.</span></span>

<span data-ttu-id="d3da4-128">Toutes les extensions de chiffrement CryptXML sont inscrites par la valeur d’URI définie dans le champ **SignatureMethod** ou attribut d’algorithme de l’élément **DigestMethod** .</span><span class="sxs-lookup"><span data-stu-id="d3da4-128">All CryptXML cryptographic extensions are registered by the URI value set in the **SignatureMethod** or the algorithm attribute field of the **DigestMethod** element.</span></span>

<span data-ttu-id="d3da4-129">Les chemins d’accès au registre des dll d’extension sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d3da4-129">The registry paths for the extension DLLs are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="d3da4-130"><span id="32-bit"></span><span id="32-BIT"></span>32 bits</span><span class="sxs-lookup"><span data-stu-id="d3da4-130"><span id="32-bit"></span><span id="32-BIT"></span>32-bit</span></span>
</dt> <dd>

<span data-ttu-id="d3da4-131">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="d3da4-131">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> <dt>

<span data-ttu-id="d3da4-132"><span id="64-bit"></span><span id="64-BIT"></span>64 bits</span><span class="sxs-lookup"><span data-stu-id="d3da4-132"><span id="64-bit"></span><span id="64-BIT"></span>64-bit</span></span>
</dt> <dd>

<span data-ttu-id="d3da4-133">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="d3da4-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

<span data-ttu-id="d3da4-134">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="d3da4-134">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**WOW6432NODE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> </dl>

<span data-ttu-id="d3da4-135">Chaque clé contient les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="d3da4-135">Each key contains the following settings.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3da4-136">Nom</span><span class="sxs-lookup"><span data-stu-id="d3da4-136">Name</span></span></th>
<th><span data-ttu-id="d3da4-137">Type</span><span class="sxs-lookup"><span data-stu-id="d3da4-137">Type</span></span></th>
<th><span data-ttu-id="d3da4-138">Données</span><span class="sxs-lookup"><span data-stu-id="d3da4-138">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3da4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d3da4-139">DLL</span></span><br/></td>
<td><span data-ttu-id="d3da4-140">Chaîne extensible</span><span class="sxs-lookup"><span data-stu-id="d3da4-140">Expandable string</span></span><br/></td>
<td><span data-ttu-id="d3da4-141">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3da4-141">Required.</span></span><br/><span data-ttu-id="d3da4-142">Chemin d’accès absolu à la DLL du fournisseur de services de chiffrement XML.</span><span class="sxs-lookup"><span data-stu-id="d3da4-142">The absolute path to the XML Cryptographic Provider DLL.</span></span>
<blockquote>
<p><span data-ttu-id="d3da4-143"><b>Remarque : </b> Nous vous recommandons de placer les dll d’extension de chiffrement dans les répertoires qui peuvent uniquement être écrits par les applications avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d3da4-143"><b>Note: </b>We recommend that cryptographic extension DLLs be located in directories that can only be written to by applications with administrative privilege.</span></span></p>
<p><span data-ttu-id="d3da4-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> est utilisé pour charger la dll d’extension de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d3da4-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> is used to load the cryptographic extension DLL.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3da4-145">Nom</span><span class="sxs-lookup"><span data-stu-id="d3da4-145">Name</span></span><br/></td>
<td><span data-ttu-id="d3da4-146"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="d3da4-146"><strong>String</strong></span></span></td>
<td><span data-ttu-id="d3da4-147">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d3da4-147">Optional.</span></span><br/> <span data-ttu-id="d3da4-148">Nom complet associé à cet URI.</span><span class="sxs-lookup"><span data-stu-id="d3da4-148">The display name associated with this URI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3da4-149">GroupId</span><span class="sxs-lookup"><span data-stu-id="d3da4-149">GroupId</span></span><br/></td>
<td><span data-ttu-id="d3da4-150"><strong>GRANDE</strong></span><span class="sxs-lookup"><span data-stu-id="d3da4-150"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="d3da4-151">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3da4-151">Required.</span></span><br/> <span data-ttu-id="d3da4-152">Identificateur de groupe associé à cet algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d3da4-152">The group identifier associated with this cryptographic algorithm.</span></span> <span data-ttu-id="d3da4-153">Les valeurs possibles sont les suivantes :<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1</span><span class="sxs-lookup"><span data-stu-id="d3da4-153">Possible values include the following:<strong>CRYPT_XML_GROUP_ID_HASH</strong>\<strong></strong> = 1</span></span><br/><span data-ttu-id="d3da4-154"><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2</span><span class="sxs-lookup"><span data-stu-id="d3da4-154"><strong>CRYPT_XML_GROUP_ID_SIGN</strong>\<strong></strong> = 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3da4-155">CNGAlgid</span><span class="sxs-lookup"><span data-stu-id="d3da4-155">CNGAlgid</span></span><br/></td>
<td><span data-ttu-id="d3da4-156"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="d3da4-156"><strong>String</strong></span></span></td>
<td><span data-ttu-id="d3da4-157">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3da4-157">Required.</span></span><br/> <span data-ttu-id="d3da4-158">Nom de l’algorithme CNG à transmettre aux fonctions BCrypt ou NCrypt.</span><span class="sxs-lookup"><span data-stu-id="d3da4-158">The CNG algorithm name to be passed to BCrypt or NCrypt functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3da4-159">CNGExtraAlgid</span><span class="sxs-lookup"><span data-stu-id="d3da4-159">CNGExtraAlgid</span></span><br/></td>
<td><span data-ttu-id="d3da4-160"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="d3da4-160"><strong>String</strong></span></span></td>
<td><span data-ttu-id="d3da4-161">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d3da4-161">Optional.</span></span><br/> <span data-ttu-id="d3da4-162">Chaîne d’algorithme supplémentaire, autre que la chaîne du membre CNGAlgid, qui peut être passée aux fonctions CNG.</span><span class="sxs-lookup"><span data-stu-id="d3da4-162">An extra algorithm string, other than the string in the CNGAlgid member, that can be passed to the CNG functions.</span></span><br/> <span data-ttu-id="d3da4-163">Pour les algorithmes de signature (CRYPT_XML_GROUP_ID_SIGN), ce membre est la chaîne de l’algorithme de clé publique à passer aux fonctions CNG.</span><span class="sxs-lookup"><span data-stu-id="d3da4-163">For the signature algorithms (CRYPT_XML_GROUP_ID_SIGN), this member is the public key algorithm string to pass to the CNG functions.</span></span><br/> <span data-ttu-id="d3da4-164">Pour les autres valeurs de GroupId, définissez le membre <strong>pwszCNGExtraAlgid</strong> sur la chaîne vide, L &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="d3da4-164">For the other values of GroupId, set the <strong>pwszCNGExtraAlgid</strong> member to the empty string, L&quot;&quot;.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d3da4-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3da4-165">Related topics</span></span>

<dl> <span data-ttu-id="d3da4-166"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d3da4-166"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="d3da4-167">Algorithmes de chiffrement de signature numérique XML</span><span class="sxs-lookup"><span data-stu-id="d3da4-167">XML Digital Signature Cryptographic Algorithms</span></span>](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
