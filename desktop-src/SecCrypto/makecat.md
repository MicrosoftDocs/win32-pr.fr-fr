---
description: Outil CryptoAPI qui crée un fichier de catalogue.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862842"
---
# <a name="makecat"></a><span data-ttu-id="662f7-103">MakeCat</span><span class="sxs-lookup"><span data-stu-id="662f7-103">MakeCat</span></span>

<span data-ttu-id="662f7-104">L’outil MakeCat est un outil CryptoAPI qui crée un fichier de catalogue.</span><span class="sxs-lookup"><span data-stu-id="662f7-104">The MakeCat tool is a CryptoAPI tool that creates a catalog file.</span></span> <span data-ttu-id="662f7-105">MakeCat est disponible dans le cadre du kit de développement logiciel (SDK) Microsoft Windows pour Windows 7 et .NET Framework 4,0 et est installé, par défaut, dans le \\ dossier bin du chemin d’installation du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="662f7-105">MakeCat is available as part of the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 and is installed, by default, in the \\Bin folder of the SDK installation path.</span></span>

<span data-ttu-id="662f7-106">L’outil MakeCat utilise la syntaxe de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="662f7-106">The MakeCat tool uses the following command syntax:</span></span>

<span data-ttu-id="662f7-107">**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Nom du fichier*</span><span class="sxs-lookup"><span data-stu-id="662f7-107">**MakeCat** \[**-n**\|**-r**\|**-v**\] *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="662f7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="662f7-108">Parameters</span></span>



| <span data-ttu-id="662f7-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="662f7-109">Parameter</span></span>             | <span data-ttu-id="662f7-110">Description</span><span class="sxs-lookup"><span data-stu-id="662f7-110">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="662f7-111">**-n**</span><span class="sxs-lookup"><span data-stu-id="662f7-111">**-n**</span></span><br/>     | <span data-ttu-id="662f7-112">Ne s’arrête pas sur une erreur récupérable.</span><span class="sxs-lookup"><span data-stu-id="662f7-112">Do not stop on a recoverable error.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="662f7-113">**-r**</span><span class="sxs-lookup"><span data-stu-id="662f7-113">**-r**</span></span><br/>     | <span data-ttu-id="662f7-114">Force MakeCat à se terminer s’il rencontre des erreurs récupérables.</span><span class="sxs-lookup"><span data-stu-id="662f7-114">Forces MakeCat to end if it encounters recoverable errors.</span></span> <span data-ttu-id="662f7-115">Plus précisément, il se termine lors du traitement des entrées dans la section des fichiers de catalogue d’un fichier. CDF.</span><span class="sxs-lookup"><span data-stu-id="662f7-115">Specifically, it will end when processing the entries in the catalog files section of a .cdf file.</span></span><br/> |
| <span data-ttu-id="662f7-116">**-v**</span><span class="sxs-lookup"><span data-stu-id="662f7-116">**-v**</span></span><br/>     | <span data-ttu-id="662f7-117">Verbose.</span><span class="sxs-lookup"><span data-stu-id="662f7-117">Verbose.</span></span> <span data-ttu-id="662f7-118">Affiche tous les messages de progression et d’erreur.</span><span class="sxs-lookup"><span data-stu-id="662f7-118">Displays all progress and error messages.</span></span><br/>                                                                                                            |
| <span data-ttu-id="662f7-119">*FileName*</span><span class="sxs-lookup"><span data-stu-id="662f7-119">*FileName*</span></span><br/> | <span data-ttu-id="662f7-120">Nom du fichier. CDF à analyser.</span><span class="sxs-lookup"><span data-stu-id="662f7-120">Name of the .cdf file to be parsed.</span></span> <span data-ttu-id="662f7-121">Pour connaître la structure et le contenu requis, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="662f7-121">For required structure and contents, see Remarks.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="662f7-122">Notes</span><span class="sxs-lookup"><span data-stu-id="662f7-122">Remarks</span></span>

<span data-ttu-id="662f7-123">Le fichier. CDF doit être généré avec les spécifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="662f7-123">The .cdf file must be built with the following specifications.</span></span>

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> <span data-ttu-id="662f7-124">La dernière entrée dans le fichier. CDF doit toujours avoir un caractère de saut de ligne explicite à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="662f7-124">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

<span data-ttu-id="662f7-125">La \[ \] section CatalogHeader définit des informations sur l’ensemble du fichier catalogue.</span><span class="sxs-lookup"><span data-stu-id="662f7-125">The \[CatalogHeader\] section defines information about the entire catalog file.</span></span>



| <span data-ttu-id="662f7-126">Option</span><span class="sxs-lookup"><span data-stu-id="662f7-126">Option</span></span>                    | <span data-ttu-id="662f7-127">Description</span><span class="sxs-lookup"><span data-stu-id="662f7-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="662f7-128">Nom</span><span class="sxs-lookup"><span data-stu-id="662f7-128">Name</span></span><br/>           | <span data-ttu-id="662f7-129">Nom du fichier catalogue, y compris son extension.</span><span class="sxs-lookup"><span data-stu-id="662f7-129">Name of the catalog file, including its extension.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="662f7-130">ResultDir</span><span class="sxs-lookup"><span data-stu-id="662f7-130">ResultDir</span></span><br/>      | <span data-ttu-id="662f7-131">Répertoire dans lequel le fichier. cat créé sera placé.</span><span class="sxs-lookup"><span data-stu-id="662f7-131">Directory where the created .cat file will be placed.</span></span> <span data-ttu-id="662f7-132">Si ce paramètre n’est pas indiqué, le répertoire actif par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="662f7-132">If not indicated, the default current directory is used.</span></span> <span data-ttu-id="662f7-133">Si le répertoire n’existe pas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="662f7-133">If the directory does not exist, it is created.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="662f7-134">PublicVersion</span><span class="sxs-lookup"><span data-stu-id="662f7-134">PublicVersion</span></span><br/>  | <span data-ttu-id="662f7-135">Cette option n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="662f7-135">This option is not supported.</span></span> <br/> <span data-ttu-id="662f7-136">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Version du catalogue.</span><span class="sxs-lookup"><span data-stu-id="662f7-136">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** Catalog version.</span></span> <span data-ttu-id="662f7-137">Si le champ n’est pas renseigné, la valeur par défaut, 1, est utilisée.</span><span class="sxs-lookup"><span data-stu-id="662f7-137">If left blank, the default value, 1, is used.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="662f7-138">CatalogVersion</span><span class="sxs-lookup"><span data-stu-id="662f7-138">CatalogVersion</span></span><br/> | <span data-ttu-id="662f7-139">Version du catalogue.</span><span class="sxs-lookup"><span data-stu-id="662f7-139">Catalog version.</span></span> <span data-ttu-id="662f7-140">Si la version n’est pas présente ou a la valeur 1, « 0x100 » est passé au paramètre *dwPublicVersion* de la fonction [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) et un fichier catalogue de la version 1 est créé.</span><span class="sxs-lookup"><span data-stu-id="662f7-140">If the version is not present or is set to 1, then "0x100" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 1 catalog file is created.</span></span> <span data-ttu-id="662f7-141">L’option HashAlgorithms doit être vide ou contenir SHA1.</span><span class="sxs-lookup"><span data-stu-id="662f7-141">The HashAlgorithms option must be empty or contain SHA1.</span></span><br/> <span data-ttu-id="662f7-142">Si la version est définie sur 2, « 0x200 » est passé au paramètre *dwPublicVersion* de la fonction [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) et un fichier catalogue de la version 2 est créé.</span><span class="sxs-lookup"><span data-stu-id="662f7-142">If the version is set to 2, then "0x200" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 2 catalog file is created.</span></span> <span data-ttu-id="662f7-143">L’option HashAlgorithms doit contenir SHA256.</span><span class="sxs-lookup"><span data-stu-id="662f7-143">The HashAlgorithms option must contain SHA256.</span></span><br/> <span data-ttu-id="662f7-144">Si cette option est présente mais contient une valeur autre que 1 ou 2, l’outil MakeCat génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="662f7-144">If this option is present but contains any value other than 1 or 2, the MakeCat tool will error out.</span></span><br/> <span data-ttu-id="662f7-145">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Cette option n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="662f7-145">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/> |
| <span data-ttu-id="662f7-146">HashAlgorithms</span><span class="sxs-lookup"><span data-stu-id="662f7-146">HashAlgorithms</span></span><br/> | <span data-ttu-id="662f7-147">Nom de l’algorithme de hachage utilisé.</span><span class="sxs-lookup"><span data-stu-id="662f7-147">Name of the hashing algorithm used.</span></span> <span data-ttu-id="662f7-148">Pour plus d’informations, consultez l’option CatalogVersion.</span><span class="sxs-lookup"><span data-stu-id="662f7-148">For more information, see the CatalogVersion option.</span></span><br/> <span data-ttu-id="662f7-149">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Cette option n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="662f7-149">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="662f7-150">PageHashes</span><span class="sxs-lookup"><span data-stu-id="662f7-150">PageHashes</span></span><br/>     | <span data-ttu-id="662f7-151">Spécifie s’il faut hacher les fichiers listés dans l' <HASH> option de la \[ \] section CatalogFiles</span><span class="sxs-lookup"><span data-stu-id="662f7-151">Specifies whether to hash the files listed in the <HASH> option in the \[CatalogFiles\] section</span></span><br/> <span data-ttu-id="662f7-152">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP :** Cette option n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="662f7-152">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="662f7-153">EncodingType</span><span class="sxs-lookup"><span data-stu-id="662f7-153">EncodingType</span></span><br/>   | <span data-ttu-id="662f7-154">Type d’encodage de message utilisé.</span><span class="sxs-lookup"><span data-stu-id="662f7-154">Type of message encoding used.</span></span> <span data-ttu-id="662f7-155">Si le champ n’est pas renseigné, la valeur par défaut de EncodingType est PKCS \_ 7 \_ ASN \_ Encoding \| x509 \_ ASN \_ , 0x00010001.</span><span class="sxs-lookup"><span data-stu-id="662f7-155">If left blank, the default EncodingType is PKCS\_7\_ASN\_ENCODING \| X509\_ASN\_ENCODING, 0x00010001.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="662f7-156">La \[ \] section CatalogFiles définit chaque membre du fichier catalogue avec des fichiers de types différents et des attributs de différents types dans des groupes distincts.</span><span class="sxs-lookup"><span data-stu-id="662f7-156">The \[CatalogFiles\] section defines each member of the catalog file with files of various types and attributes of various types in separate groups.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="662f7-157">Option</span><span class="sxs-lookup"><span data-stu-id="662f7-157">Option</span></span></th>
<th><span data-ttu-id="662f7-158">Description</span><span class="sxs-lookup"><span data-stu-id="662f7-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="662f7-159">balise de référence</span><span class="sxs-lookup"><span data-stu-id="662f7-159">reference tag</span></span><br/></td>
<td><span data-ttu-id="662f7-160">Référence de texte au fichier.</span><span class="sxs-lookup"><span data-stu-id="662f7-160">Text reference to the file.</span></span> <span data-ttu-id="662f7-161">Il peut s’agir de caractères de texte ASCII, à l’exception du signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="662f7-161">This can include any ASCII text characters except the equal sign (=).</span></span> <span data-ttu-id="662f7-162">Le système doit être en mesure de reproduire cette balise après l’installation.</span><span class="sxs-lookup"><span data-stu-id="662f7-162">The system must be able to reproduce this tag after installation.</span></span> <br/> <span data-ttu-id="662f7-163">Utilisez <HASH> comme préfixe du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="662f7-163">Use <HASH> as a prefix of the file name.</span></span> <span data-ttu-id="662f7-164">La balise est alors le hachage du fichier sous forme de chaîne ASCII.</span><span class="sxs-lookup"><span data-stu-id="662f7-164">This results in the tag being the file's hash in ASCII string form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="662f7-165">nom et chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="662f7-165">file path and name</span></span><br/></td>
<td><span data-ttu-id="662f7-166">Nom du fichier, y compris l’extension à analyser et le chemin d’accès relatif au fichier.</span><span class="sxs-lookup"><span data-stu-id="662f7-166">The file name, including the extension to be parsed and the relative path to the file.</span></span> <span data-ttu-id="662f7-167">Tout type de fichier pouvant être signé avec SignTool peut être ajouté à un catalogue.</span><span class="sxs-lookup"><span data-stu-id="662f7-167">Any type of file that can be signed with SignTool can be added to a catalog.</span></span> <span data-ttu-id="662f7-168">Par exemple, les noms de fichiers avec les extensions suivantes, entre autres, peuvent être ajoutés à un catalogue :. exe,. cab,. cat,. ocx,. dll et. STL.</span><span class="sxs-lookup"><span data-stu-id="662f7-168">For example, file names with the following extensions, among others, can be added to a catalog: .exe, .cab, .cat, .ocx, .dll, and .stl.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="662f7-169">ALTSIPID</span><span class="sxs-lookup"><span data-stu-id="662f7-169">ALTSIPID</span></span><br/></td>
<td><span data-ttu-id="662f7-170">GUID SIP qui doit être utilisé pour le hachage au lieu du SIP standard en fonction du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="662f7-170">SIP GUID that is to be used for hashing instead of the standard SIP based on file type.</span></span> <span data-ttu-id="662f7-171">Cette entrée est facultative.</span><span class="sxs-lookup"><span data-stu-id="662f7-171">This entry is optional.</span></span> <span data-ttu-id="662f7-172">Si cette entrée est omise, le membre sera haché à l’aide du SIP par défaut.</span><span class="sxs-lookup"><span data-stu-id="662f7-172">If this entry is omitted, the member will be hashed using the default SIP.</span></span> <span data-ttu-id="662f7-173">Si aucun SIP installé par défaut n’est trouvé, le SIP plat sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="662f7-173">If no default installed SIP is found, the Flat SIP will be used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="662f7-174">guid</span><span class="sxs-lookup"><span data-stu-id="662f7-174">guid</span></span><br/></td>
<td><span data-ttu-id="662f7-175">Représentation textuelle d’un GUID.</span><span class="sxs-lookup"><span data-stu-id="662f7-175">Text representation of a GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="662f7-176">ATTRx</span><span class="sxs-lookup"><span data-stu-id="662f7-176">ATTRx</span></span><br/></td>
<td><span data-ttu-id="662f7-177">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="662f7-177">Optional.</span></span> <span data-ttu-id="662f7-178">Attribut ou instruction sur le fichier ou le contenu.</span><span class="sxs-lookup"><span data-stu-id="662f7-178">Attribute or statement about the file or content.</span></span> <span data-ttu-id="662f7-179">Il peut y avoir un nombre quelconque d’attributs, y compris aucun.</span><span class="sxs-lookup"><span data-stu-id="662f7-179">There can be any number of attributes, including none.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="662f7-180">type</span><span class="sxs-lookup"><span data-stu-id="662f7-180">type</span></span><br/></td>
<td><span data-ttu-id="662f7-181">Définit le type d’attribut qui est ajouté au format 0x00000000 (texte).</span><span class="sxs-lookup"><span data-stu-id="662f7-181">Defines what type of attribute is being added in the format 0x00000000 (text).</span></span> <span data-ttu-id="662f7-182">Cette option peut être<strong>une combinaison or au niveau</strong> du bit de zéro ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="662f7-182">This option can be a bitwise-<strong>OR</strong> combination of zero or more of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="662f7-183">0x10000000 attribut authentifié (signé, inclus dans le hachage).</span><span class="sxs-lookup"><span data-stu-id="662f7-183">0x10000000 Authenticated attribute (signed, included in the hash).</span></span></li>
<li><span data-ttu-id="662f7-184">0x20000000 attribut non authentifié (non signé, non inclus dans le hachage, non vérifiable).</span><span class="sxs-lookup"><span data-stu-id="662f7-184">0x20000000 Unauthenticated attribute (unsigned, not included in the hash, not verifiable).</span></span></li>
<li><span data-ttu-id="662f7-185">l’attribut 0x01000000 n’est pas répliqué sur les entrées SHA1 dans un catalogue CatalogVersion 2.</span><span class="sxs-lookup"><span data-stu-id="662f7-185">0x01000000 Attribute will not be replicated to SHA1 entries in a CatalogVersion 2 catalog.</span></span></li>
<li><span data-ttu-id="662f7-186">l’attribut 0x00010000 est représenté en texte brut.</span><span class="sxs-lookup"><span data-stu-id="662f7-186">0x00010000 Attribute is represented in plaintext.</span></span> <span data-ttu-id="662f7-187">Aucune conversion n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="662f7-187">No conversion will be done.</span></span></li>
<li><span data-ttu-id="662f7-188">l’attribut 0x00020000 est représenté dans l’encodage de base 64.</span><span class="sxs-lookup"><span data-stu-id="662f7-188">0x00020000 Attribute is represented in base-64 encoding.</span></span> <span data-ttu-id="662f7-189">Utilisé pour représenter des données binaires.</span><span class="sxs-lookup"><span data-stu-id="662f7-189">This is used to represent binary data.</span></span></li>
<li><span data-ttu-id="662f7-190">l’attribut 0x00000001 est une paire nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="662f7-190">0x00000001 Attribute is a name-value pair.</span></span> <span data-ttu-id="662f7-191">Utilisez l’option OID pour le nom.</span><span class="sxs-lookup"><span data-stu-id="662f7-191">Use the oid option for the name.</span></span> <span data-ttu-id="662f7-192">Cet attribut est lent ; par conséquent, utilisez cette option avec modération.</span><span class="sxs-lookup"><span data-stu-id="662f7-192">This attribute is slow; therefore, use this option sparingly.</span></span></li>
<li><span data-ttu-id="662f7-193">l’attribut 0x00000002 est référencé par un <a href="/windows/desktop/SecGloss/o-gly"><em>identificateur d’objet</em></a> (OID).</span><span class="sxs-lookup"><span data-stu-id="662f7-193">0x00000002 Attribute is referenced by an <a href="/windows/desktop/SecGloss/o-gly"><em>object identifier</em></a> (OID).</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="662f7-194">oid</span><span class="sxs-lookup"><span data-stu-id="662f7-194">oid</span></span><br/></td>
<td><span data-ttu-id="662f7-195">Représentation textuelle de la clé de référence de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="662f7-195">The text representation of the attribute's reference key.</span></span> <span data-ttu-id="662f7-196">Il s’agit d’un OID sous la forme d’une chaîne de texte en notation à quatre points (par exemple, a. b. c. d) ou d’un nom de texte.</span><span class="sxs-lookup"><span data-stu-id="662f7-196">It is an OID in the form of a text string in dotted quad notation (for example, a.b.c.d) or a text Name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="662f7-197">value</span><span class="sxs-lookup"><span data-stu-id="662f7-197">value</span></span><br/></td>
<td><span data-ttu-id="662f7-198">Représentation textuelle de la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="662f7-198">The text representation of the value of the attribute.</span></span> <span data-ttu-id="662f7-199">Le type de représentation textuelle utilisé dépend de la valeur de l’option type.</span><span class="sxs-lookup"><span data-stu-id="662f7-199">The type of text representation used depends on the value of the type option.</span></span> <span data-ttu-id="662f7-200">Les caractères EOL déterminent la longueur.</span><span class="sxs-lookup"><span data-stu-id="662f7-200">The EOL characters determine the length.</span></span><br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td><span data-ttu-id="662f7-201">Hache le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="662f7-201">Hashes the specified file.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="662f7-202">Le fichier catalogue généré n’est pas signé.</span><span class="sxs-lookup"><span data-stu-id="662f7-202">The generated catalog file is unsigned.</span></span> <span data-ttu-id="662f7-203">S’il doit être signé avant de transmettre, il est signé à l’aide de [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="662f7-203">If it is to be signed prior to transmittal, it is signed by using [SignTool](signtool.md).</span></span>

 

 
