---
description: Crée un certificat X. 509, signé par la clé racine de test ou une autre clé spécifiée, qui lie votre nom à la partie publique de la paire de clés. Le certificat est enregistré dans un fichier, un magasin de certificats système, ou les deux.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c15db364066d9edadb6a0c4d2c24dceab5cc9
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327143"
---
# <a name="makecert"></a><span data-ttu-id="ca27c-104">MakeCert</span><span class="sxs-lookup"><span data-stu-id="ca27c-104">MakeCert</span></span>

> [!Note]  
> <span data-ttu-id="ca27c-105">MakeCert est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="ca27c-105">MakeCert is deprecated.</span></span> <span data-ttu-id="ca27c-106">Pour créer des certificats auto-signés, utilisez l’applet de commande PowerShell [New-SelfSignedCertificate](/powershell/module/pki/new-selfsignedcertificate).</span><span class="sxs-lookup"><span data-stu-id="ca27c-106">To create self-signed certificates, use the Powershell Cmdlet [New-SelfSignedCertificate](/powershell/module/pki/new-selfsignedcertificate).</span></span>

 

<span data-ttu-id="ca27c-107">L’outil MakeCert crée un certificat [*X. 509*](../secgloss/x-gly.md) , signé par la clé racine de test ou une autre clé spécifiée, qui lie votre nom à la partie publique de la paire de clés.</span><span class="sxs-lookup"><span data-stu-id="ca27c-107">The MakeCert tool creates an [*X.509*](../secgloss/x-gly.md) certificate, signed by the test root key or other specified key, that binds your name to the public part of the key pair.</span></span> <span data-ttu-id="ca27c-108">Le certificat est enregistré dans un fichier, un magasin de certificats système, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="ca27c-108">The certificate is saved to a file, a system certificate store, or both.</span></span> <span data-ttu-id="ca27c-109">L’outil est installé dans le \\ dossier bin du chemin d’installation du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ca27c-109">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="ca27c-110">L’outil MakeCert utilise la syntaxe de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ca27c-110">The MakeCert tool uses the following command syntax:</span></span>

<span data-ttu-id="ca27c-111">**Makecert** \[ *BasicOptions* \| *ExtendedOptions* \] *FichierSortie*</span><span class="sxs-lookup"><span data-stu-id="ca27c-111">**MakeCert** \[*BasicOptions*\|*ExtendedOptions*\] *OutputFile*</span></span>

<span data-ttu-id="ca27c-112">*FichierSortie* est le nom du fichier dans lequel le certificat sera écrit.</span><span class="sxs-lookup"><span data-stu-id="ca27c-112">*OutputFile* is the name of the file where the certificate will be written.</span></span> <span data-ttu-id="ca27c-113">Vous pouvez omettre *outputfile* si le certificat ne doit pas être écrit dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="ca27c-113">You can omit *OutputFile* if the certificate is not to be written to a file.</span></span>

## <a name="options"></a><span data-ttu-id="ca27c-114">Options</span><span class="sxs-lookup"><span data-stu-id="ca27c-114">Options</span></span>

<span data-ttu-id="ca27c-115">MakeCert comprend des options de base et étendues.</span><span class="sxs-lookup"><span data-stu-id="ca27c-115">MakeCert includes basic and extended options.</span></span> <span data-ttu-id="ca27c-116">Les options de base sont celles le plus fréquemment utilisées lors de la création d'un certificat.</span><span class="sxs-lookup"><span data-stu-id="ca27c-116">Basic options are those most commonly used to create a certificate.</span></span> <span data-ttu-id="ca27c-117">Les options avancées offrent une flexibilité accrue.</span><span class="sxs-lookup"><span data-stu-id="ca27c-117">Extended options provide more flexibility.</span></span>

<span data-ttu-id="ca27c-118">Les options de MakeCert sont également divisées en trois groupes fonctionnels :</span><span class="sxs-lookup"><span data-stu-id="ca27c-118">The options for MakeCert are also divided into three functional groups:</span></span>

-   <span data-ttu-id="ca27c-119">Options de base spécifiques à la technologie du magasin de certificats uniquement.</span><span class="sxs-lookup"><span data-stu-id="ca27c-119">Basic options specific to certificate store technology only.</span></span>
-   <span data-ttu-id="ca27c-120">Options étendues spécifiques à la technologie de fichier SPC et de clé privée uniquement.</span><span class="sxs-lookup"><span data-stu-id="ca27c-120">Extended options specific to SPC-file and private key technology only.</span></span>
-   <span data-ttu-id="ca27c-121">Options étendues applicables à la technologie du fichier SPC, de la clé privée et du magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="ca27c-121">Extended options applicable to SPC-file, private key, and certificate store technology.</span></span>

<span data-ttu-id="ca27c-122">Les options indiquées dans les tableaux suivants peuvent être utilisées uniquement avec Internet Explorer 4,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ca27c-122">Options given in the following tables can be used only with Internet Explorer 4.0 or later.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca27c-123">Option de base</span><span class="sxs-lookup"><span data-stu-id="ca27c-123">Basic option</span></span></th>
<th><span data-ttu-id="ca27c-124">Description</span><span class="sxs-lookup"><span data-stu-id="ca27c-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca27c-125"><strong>-a</strong> <strong></strong> <em>Algorithme</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-125"><strong>-a</strong> <strong></strong> <em>Algorithm</em></span></span></td>
<td><span data-ttu-id="ca27c-126">Algorithme de <a href="/windows/desktop/SecGloss/h-gly"><em>hachage</em></a> .</span><span class="sxs-lookup"><span data-stu-id="ca27c-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> algorithm.</span></span> <span data-ttu-id="ca27c-127">Doit avoir la valeur <strong>SHA-1</strong> ou <strong>MD5</strong> (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="ca27c-127">Must be set to either <strong>SHA-1</strong> or <strong>MD5</strong> (default).</span></span> <span data-ttu-id="ca27c-128">Pour plus d’informations sur MD5, consultez <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span><span class="sxs-lookup"><span data-stu-id="ca27c-128">For information about MD5, see <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span></span></td>
<td><span data-ttu-id="ca27c-130">Date à laquelle le certificat devient valide.</span><span class="sxs-lookup"><span data-stu-id="ca27c-130">Date the certificate first becomes valid.</span></span> <span data-ttu-id="ca27c-131">La valeur par défaut est lorsque le certificat est créé.</span><span class="sxs-lookup"><span data-stu-id="ca27c-131">The default is when the certificate is created.</span></span> <span data-ttu-id="ca27c-132">Le format de <em>DateStart</em> est mm/jj/aaaa.</span><span class="sxs-lookup"><span data-stu-id="ca27c-132">The format of <em>DateStart</em> is mm/dd/yyyy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-133"><strong>-CY</strong> <strong></strong> <em>CertificateTypes</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span></span></td>
<td><span data-ttu-id="ca27c-134">Type de certificat.</span><span class="sxs-lookup"><span data-stu-id="ca27c-134">Certificate type.</span></span> <span data-ttu-id="ca27c-135"><em>CertificateTypes</em> peut être <strong>end</strong> pour l’entité finale ou l' <strong>autorité</strong> de <a href="/windows/desktop/SecGloss/c-gly"><em>certification</em></a>.</span><span class="sxs-lookup"><span data-stu-id="ca27c-135"><em>CertificateTypes</em> can be <strong>end</strong> for end-entity, or <strong>authority</strong> for <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span></span></td>
<td><span data-ttu-id="ca27c-137">Date de fin de la période de validité.</span><span class="sxs-lookup"><span data-stu-id="ca27c-137">Date when the validity period ends.</span></span> <span data-ttu-id="ca27c-138">La valeur par défaut est l’année 2039.</span><span class="sxs-lookup"><span data-stu-id="ca27c-138">The default is the year 2039.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-139"><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</span><span class="sxs-lookup"><span data-stu-id="ca27c-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> …</span></span></td>
<td><span data-ttu-id="ca27c-140">Insère dans le certificat une liste d’un ou de plusieurs <a href="/windows/desktop/SecGloss/o-gly"><em>identificateurs d’objet</em></a> (OID) séparés <a href="/windows/desktop/SecGloss/e-gly"><em>par des virgules, séparés</em></a> par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ca27c-140">Inserts a list of one or more comma-separated, <a href="/windows/desktop/SecGloss/e-gly"><em>enhanced key usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>object identifiers</em></a> (OIDs) into the certificate.</span></span> <span data-ttu-id="ca27c-141">Par exemple, <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> insère l’OID d’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="ca27c-141">For example, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserts the client authentication OID.</span></span> <span data-ttu-id="ca27c-142">Pour obtenir les définitions des OID autorisés, consultez le fichier Wincrypt. h dans CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="ca27c-142">For definitions of allowable OIDs, see the Wincrypt.h file in CryptoAPI 2.0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span></span></td>
<td><span data-ttu-id="ca27c-144">Hauteur maximale de l’arborescence en dessous de ce certificat.</span><span class="sxs-lookup"><span data-stu-id="ca27c-144">Maximum height of the tree below this certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span></span></td>
<td><span data-ttu-id="ca27c-146">Lien vers les informations de stratégie de l’Agence SPC (par exemple, une URL).</span><span class="sxs-lookup"><span data-stu-id="ca27c-146">Link to SPC agency policy information (for example, a URL).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span></span></td>
<td><span data-ttu-id="ca27c-148">Durée de la période de validité.</span><span class="sxs-lookup"><span data-stu-id="ca27c-148">Duration of the validity period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-149"><strong>-n</strong> <strong>&quot;</strong> <em>Nom</em><strong>&quot;</strong></span><span class="sxs-lookup"><span data-stu-id="ca27c-149"><strong>-n</strong> <strong>&quot;</strong><em>Name</em><strong>&quot;</strong></span></span></td>
<td><span data-ttu-id="ca27c-150">Nom du certificat de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-150">Name for the publisher's certificate.</span></span> <span data-ttu-id="ca27c-151">Ce nom doit être conforme à la norme <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> .</span><span class="sxs-lookup"><span data-stu-id="ca27c-151">This name must conform to the <a href="/windows/desktop/SecGloss/x-gly"><em>X.500</em></a> standard.</span></span> <span data-ttu-id="ca27c-152">La méthode la plus simple consiste à utiliser le &quot; format CN =<em>myname</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="ca27c-152">The simplest method is to use the &quot;CN=<em>MyName</em>&quot; format.</span></span> <span data-ttu-id="ca27c-153">Par exemple : <strong>-n &quot; CN = test &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="ca27c-153">For example: <strong>-n &quot;CN=Test&quot;</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-154"><strong>-nscp</strong></span><span class="sxs-lookup"><span data-stu-id="ca27c-154"><strong>-nscp</strong></span></span></td>
<td><span data-ttu-id="ca27c-155">L’extension d’authentification du client Netscape doit être incluse.</span><span class="sxs-lookup"><span data-stu-id="ca27c-155">The Netscape client authentication extension should be included.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-156"><strong>-PE</strong></span><span class="sxs-lookup"><span data-stu-id="ca27c-156"><strong>-pe</strong></span></span></td>
<td><span data-ttu-id="ca27c-157">Marque la clé privée comme étant exportable.</span><span class="sxs-lookup"><span data-stu-id="ca27c-157">Marks the private key as exportable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-158"><strong>-r</strong></span><span class="sxs-lookup"><span data-stu-id="ca27c-158"><strong>-r</strong></span></span></td>
<td><span data-ttu-id="ca27c-159">Crée un certificat auto-signé</span><span class="sxs-lookup"><span data-stu-id="ca27c-159">Creates a self-signed certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-160"><strong>-SC</strong> <strong></strong> <em>SubjectCertFile</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span></span></td>
<td><span data-ttu-id="ca27c-161">Nom du fichier de certificat avec la clé publique du sujet existant à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ca27c-161">Certificate file name with the existing subject public key to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-162"><strong>-SK</strong> <strong></strong> <em>SubjectKey</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span></span></td>
<td><span data-ttu-id="ca27c-163">Emplacement du conteneur de clé du sujet qui contient la <a href="/windows/desktop/SecGloss/p-gly"><em>clé privée</em></a>.</span><span class="sxs-lookup"><span data-stu-id="ca27c-163">Location of the subject's key container which holds the <a href="/windows/desktop/SecGloss/p-gly"><em>private key</em></a>.</span></span> <span data-ttu-id="ca27c-164">Un conteneur de clé sera créé s'il n'en existe aucun.</span><span class="sxs-lookup"><span data-stu-id="ca27c-164">If a key container does not exist, one is created.</span></span> <span data-ttu-id="ca27c-165">Si aucune des options <strong>-SK</strong> ou <strong>-SV</strong> n’est utilisée, un conteneur de clé par défaut est créé et utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca27c-165">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-166"><strong>-ciel</strong> <strong></strong> <em>SubjectKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span></span></td>
<td><span data-ttu-id="ca27c-167">Spécification de clé du sujet.</span><span class="sxs-lookup"><span data-stu-id="ca27c-167">Subject's key specification.</span></span> <span data-ttu-id="ca27c-168"><em>SubjectKeySpec</em> doit avoir l’une des trois valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="ca27c-168"><em>SubjectKeySpec</em> must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="ca27c-169"><strong>Signature</strong> (spécification de clé AT_SIGNATURE)</span><span class="sxs-lookup"><span data-stu-id="ca27c-169"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="ca27c-170"><strong>Exchange</strong> (spécification de clé AT_KEYEXCHANGE)</span><span class="sxs-lookup"><span data-stu-id="ca27c-170"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="ca27c-171">Entier, tel que <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="ca27c-171">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="ca27c-172">Pour plus d’informations, consultez la remarque qui suit ce tableau.</span><span class="sxs-lookup"><span data-stu-id="ca27c-172">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-173"><strong>-SP</strong> <strong></strong> <em>SubjectProviderName</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span></span></td>
<td><span data-ttu-id="ca27c-174">Fournisseur CryptoAPI pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca27c-174">CryptoAPI provider for subject.</span></span> <span data-ttu-id="ca27c-175">La valeur par défaut est le fournisseur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-175">The default is the user's provider.</span></span> <span data-ttu-id="ca27c-176">Pour plus d’informations sur les fournisseurs CryptoAPI, consultez la documentation CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="ca27c-176">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-177"><strong>-SR</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span></span></td>
<td><span data-ttu-id="ca27c-178">Emplacement du Registre du magasin de certificats du sujet.</span><span class="sxs-lookup"><span data-stu-id="ca27c-178">Registry location of the subject's certificate store.</span></span> <span data-ttu-id="ca27c-179"><em>SubjectCertStoreLocation</em> doit être <strong>LocalMachine</strong> (clé de Registre HKEY_LOCAL_MACHINE) ou <strong>CurrentUser</strong> (clé de Registre HKEY_CURRENT_USER).</span><span class="sxs-lookup"><span data-stu-id="ca27c-179"><em>SubjectCertStoreLocation</em> must be either <strong>LocalMachine</strong> (registry key HKEY_LOCAL_MACHINE) or <strong>CurrentUser</strong> (registry key HKEY_CURRENT_USER).</span></span> <span data-ttu-id="ca27c-180"><strong>CurrentUser</strong> est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca27c-180"><strong>CurrentUser</strong> is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-181"><strong>-SS</strong> <strong></strong> <em>SubjectCertStoreName</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span></span></td>
<td><span data-ttu-id="ca27c-182">Nom du magasin de certificats du sujet dans lequel le certificat généré sera stocké.</span><span class="sxs-lookup"><span data-stu-id="ca27c-182">Name of the subject's certificate store where the generated certificate will be stored.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-183"><strong>-SV</strong> <strong></strong> <em>SubjectKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span></span></td>
<td><span data-ttu-id="ca27c-184">Nom du fichier. pvk du sujet.</span><span class="sxs-lookup"><span data-stu-id="ca27c-184">Name of the subject's .pvk file.</span></span> <span data-ttu-id="ca27c-185">Si aucune des options <strong>-SK</strong> ou <strong>-SV</strong> n’est utilisée, un conteneur de clé par défaut est créé et utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca27c-185">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-186"><strong>-SY</strong> <strong></strong> <em>nSubjectProviderType</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span></span></td>
<td><span data-ttu-id="ca27c-187">Type de fournisseur CryptoAPI pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca27c-187">CryptoAPI provider type for subject.</span></span> <span data-ttu-id="ca27c-188">La valeur par défaut est <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="ca27c-188">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="ca27c-189">Pour plus d’informations sur les types de fournisseur CryptoAPI, consultez la documentation CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="ca27c-189">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-190"><strong>-#</strong><strong></strong> <em>SerialNumber</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-190"><strong>-#</strong> <strong></strong> <em>SerialNumber</em></span></span></td>
<td><span data-ttu-id="ca27c-191">Numéro de série du certificat.</span><span class="sxs-lookup"><span data-stu-id="ca27c-191">Serial number of the certificate.</span></span> <span data-ttu-id="ca27c-192">La valeur maximale est 2 ^ 31.</span><span class="sxs-lookup"><span data-stu-id="ca27c-192">The maximum value is 2^31.</span></span> <span data-ttu-id="ca27c-193">La valeur par défaut est une valeur générée par l’outil qui est garantie comme étant unique.</span><span class="sxs-lookup"><span data-stu-id="ca27c-193">The default is a value generated by the tool that is guaranteed to be unique.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-194"><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-194"><strong>-$</strong> <strong></strong> <em>CertificateAuthority</em></span></span></td>
<td><span data-ttu-id="ca27c-195">Type d' <a href="/windows/desktop/SecGloss/c-gly"><em>autorité de certification</em></a>.</span><span class="sxs-lookup"><span data-stu-id="ca27c-195">Type of <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span> <span data-ttu-id="ca27c-196"><em>CertificateAuthority</em> doit être défini sur <strong>commercial</strong> (pour les certificats utilisés par les éditeurs de logiciels commerciaux) ou sur <strong>individuel</strong> (pour les certificats utilisés par les éditeurs de logiciels individuels).</span><span class="sxs-lookup"><span data-stu-id="ca27c-196"><em>CertificateAuthority</em> must be set to either <strong>commercial</strong> (for certificates to be used by commercial software publishers) or <strong>individual</strong> (for certificates to be used by individual software publishers).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-197"><strong>-?</strong></span><span class="sxs-lookup"><span data-stu-id="ca27c-197"><strong>-?</strong></span></span></td>
<td><span data-ttu-id="ca27c-198">Affiche les options de base.</span><span class="sxs-lookup"><span data-stu-id="ca27c-198">Displays the basic options.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-199"><strong>-!</strong></span><span class="sxs-lookup"><span data-stu-id="ca27c-199"><strong>-!</strong></span></span></td>
<td><span data-ttu-id="ca27c-200">Affiche les options étendues.</span><span class="sxs-lookup"><span data-stu-id="ca27c-200">Displays the extended options.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="ca27c-201">Si l’option **de spécification de clé-ciel** est utilisée dans Internet Explorer version 4,0 ou ultérieure, la spécification doit correspondre à la spécification de clé indiquée par le fichier de [*clé privée*](../secgloss/p-gly.md) ou le [*conteneur de clé*](../secgloss/k-gly.md)privée.</span><span class="sxs-lookup"><span data-stu-id="ca27c-201">If the **-sky** key specification option is used in Internet Explorer version 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="ca27c-202">Si l’option de spécification de clé n’est pas utilisée, la spécification de clé indiquée par le fichier de clé privée ou le conteneur de clé privée sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="ca27c-202">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="ca27c-203">S’il existe plus d’une spécification de clé dans le conteneur de clé, MakeCert tente d’abord d’utiliser la \_ spécification de clé at signature.</span><span class="sxs-lookup"><span data-stu-id="ca27c-203">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="ca27c-204">En cas d’échec, MakeCert essaiera d’utiliser AT \_ KeyExchange.</span><span class="sxs-lookup"><span data-stu-id="ca27c-204">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="ca27c-205">Étant donné que la plupart des utilisateurs ont une clé AT de \_ signature ou une \_ clé at KeyExchange, cette option n’a pas besoin d’être utilisée dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="ca27c-205">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="ca27c-206">Les options suivantes sont uniquement destinées aux fichiers de certificat SPC ( [*Software Publisher Certificate*](../secgloss/s-gly.md) ) et à la technologie de clé privée.</span><span class="sxs-lookup"><span data-stu-id="ca27c-206">The following options are only for [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) files and private key technology.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca27c-207">Option SPC et clé privée</span><span class="sxs-lookup"><span data-stu-id="ca27c-207">SPC and private key option</span></span></th>
<th><span data-ttu-id="ca27c-208">Description</span><span class="sxs-lookup"><span data-stu-id="ca27c-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca27c-209"><strong>-IC</strong> <strong></strong> <em>IssuerCertFile</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span></span></td>
<td><span data-ttu-id="ca27c-210">Emplacement du certificat de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-210">Location of the issuer's certificate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span></span></td>
<td><span data-ttu-id="ca27c-212">Emplacement du conteneur de clé de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-212">Location of the issuer's key container.</span></span> <span data-ttu-id="ca27c-213">La valeur par défaut est la clé racine de test.</span><span class="sxs-lookup"><span data-stu-id="ca27c-213">The default is the test root key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-214"><strong>-IKY</strong> <strong></strong> <em>IssuerKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span></span></td>
<td><span data-ttu-id="ca27c-215">Spécification de clé de l’émetteur, qui doit être l’une des trois valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="ca27c-215">Issuer's key specification, which must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="ca27c-216"><strong>Signature</strong> (spécification de clé AT_SIGNATURE)</span><span class="sxs-lookup"><span data-stu-id="ca27c-216"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="ca27c-217"><strong>Exchange</strong> (spécification de clé AT_KEYEXCHANGE)</span><span class="sxs-lookup"><span data-stu-id="ca27c-217"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="ca27c-218">Entier, tel que <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="ca27c-218">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="ca27c-219">Pour plus d’informations, consultez la remarque qui suit ce tableau.</span><span class="sxs-lookup"><span data-stu-id="ca27c-219">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-220"><strong>-IP</strong> <strong></strong> <em>IssuerProviderName</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span></span></td>
<td><span data-ttu-id="ca27c-221">Fournisseur CryptoAPI pour l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-221">CryptoAPI provider for issuer.</span></span> <span data-ttu-id="ca27c-222">La valeur par défaut est le fournisseur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-222">The default is the user's provider.</span></span> <span data-ttu-id="ca27c-223">Pour plus d’informations sur les fournisseurs CryptoAPI, consultez la documentation CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="ca27c-223">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca27c-224"><strong>-IV</strong> <strong></strong> <em>IssuerKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span></span></td>
<td><span data-ttu-id="ca27c-225">Fichier de clé privée de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-225">Issuer's private key file.</span></span> <span data-ttu-id="ca27c-226">La valeur par défaut est la racine de test.</span><span class="sxs-lookup"><span data-stu-id="ca27c-226">The default is the test root.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca27c-227"><strong>-e/e</strong> <strong></strong> <em>nIssuerProviderType</em></span><span class="sxs-lookup"><span data-stu-id="ca27c-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span></span></td>
<td><span data-ttu-id="ca27c-228">Type de fournisseur CryptoAPI pour l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-228">CryptoAPI provider type for issuer.</span></span> <span data-ttu-id="ca27c-229">La valeur par défaut est <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="ca27c-229">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="ca27c-230">Pour plus d’informations sur les types de fournisseur CryptoAPI, consultez la documentation CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="ca27c-230">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="ca27c-231">Si l’option de spécification de clé **-IKY** est utilisée dans Internet Explorer 4,0 ou une version ultérieure, la spécification doit correspondre à la spécification de clé indiquée par le fichier de [*clé privée*](../secgloss/p-gly.md) ou le [*conteneur de clé*](../secgloss/k-gly.md)privée.</span><span class="sxs-lookup"><span data-stu-id="ca27c-231">If the **-iky** key specification option is used in Internet Explorer 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="ca27c-232">Si l’option de spécification de clé n’est pas utilisée, la spécification de clé indiquée par le fichier de clé privée ou le conteneur de clé privée sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="ca27c-232">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="ca27c-233">S’il existe plus d’une spécification de clé dans le conteneur de clé, MakeCert tente d’abord d’utiliser la \_ spécification de clé at signature.</span><span class="sxs-lookup"><span data-stu-id="ca27c-233">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="ca27c-234">En cas d’échec, MakeCert essaiera d’utiliser AT \_ KeyExchange.</span><span class="sxs-lookup"><span data-stu-id="ca27c-234">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="ca27c-235">Étant donné que la plupart des utilisateurs ont une clé AT de \_ signature ou une \_ clé at KeyExchange, cette option n’a pas besoin d’être utilisée dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="ca27c-235">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="ca27c-236">Les options suivantes sont destinées uniquement à la technologie du [*magasin de certificats*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ca27c-236">The following options are for [*certificate store*](../secgloss/c-gly.md) technology only.</span></span>



| <span data-ttu-id="ca27c-237">Option du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="ca27c-237">Certificate store option</span></span>          | <span data-ttu-id="ca27c-238">Description</span><span class="sxs-lookup"><span data-stu-id="ca27c-238">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca27c-239">**-IC** *IssuerCertFile*</span><span class="sxs-lookup"><span data-stu-id="ca27c-239">**-ic** *IssuerCertFile*</span></span>          | <span data-ttu-id="ca27c-240">Fichier qui contient le certificat de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-240">File that contains the issuer's certificate.</span></span> <span data-ttu-id="ca27c-241">MakeCert recherche un certificat avec une correspondance exacte dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="ca27c-241">MakeCert will search in the certificate store for a certificate with an exact match.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="ca27c-242">**-dans** *IssuerNameString*</span><span class="sxs-lookup"><span data-stu-id="ca27c-242">**-in** *IssuerNameString*</span></span>        | <span data-ttu-id="ca27c-243">Nom commun du certificat de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-243">Common name of the issuer's certificate.</span></span> <span data-ttu-id="ca27c-244">MakeCert recherche un certificat dont le nom commun comprend *IssuerNameString* dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="ca27c-244">MakeCert will search in the certificate store for a certificate whose common name includes *IssuerNameString*.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="ca27c-245">**-IR** *IssuerCertStoreLocation*</span><span class="sxs-lookup"><span data-stu-id="ca27c-245">**-ir** *IssuerCertStoreLocation*</span></span> | <span data-ttu-id="ca27c-246">Emplacement du Registre du magasin de certificats de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="ca27c-246">Registry location of the issuer's certificate store.</span></span> <span data-ttu-id="ca27c-247">*IssuerCertStoreLocation* doit être **LocalMachine** (clé de Registre HKEY \_ local \_ machine) ou **CurrentUser** (clé de Registre HKEY \_ Current \_ User).</span><span class="sxs-lookup"><span data-stu-id="ca27c-247">*IssuerCertStoreLocation* must be either **LocalMachine** (registry key HKEY\_LOCAL\_MACHINE) or **CurrentUser** (registry key HKEY\_CURRENT\_USER).</span></span> <span data-ttu-id="ca27c-248">**CurrentUser** est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca27c-248">**CurrentUser** is the default.</span></span>                                                                                                |
| <span data-ttu-id="ca27c-249">**-est** *IssuerCertStoreName*</span><span class="sxs-lookup"><span data-stu-id="ca27c-249">**-is** *IssuerCertStoreName*</span></span>     | <span data-ttu-id="ca27c-250">Magasin de certificats de l’émetteur qui comprend le certificat de l’émetteur et ses informations de clé privée associées.</span><span class="sxs-lookup"><span data-stu-id="ca27c-250">Issuer's certificate store that includes the issuer's certificate and its associated private key information.</span></span> <span data-ttu-id="ca27c-251">S’il existe plus d’un certificat dans le magasin, l’utilisateur doit l’identifier de manière unique à l’aide de l’option **-IC** ou **-in** .</span><span class="sxs-lookup"><span data-stu-id="ca27c-251">If there is more than one certificate in the store, the user must uniquely identify it by using the **-ic** or **-in** option.</span></span> <span data-ttu-id="ca27c-252">Si le certificat dans le magasin de certificats n’est pas identifié de manière unique, MakeCert échoue.</span><span class="sxs-lookup"><span data-stu-id="ca27c-252">If the certificate in the certificate store is not uniquely identified, MakeCert will fail.</span></span> |



 

 

 
