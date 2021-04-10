---
description: L’outil de configuration de certificat Microsoft Windows HTTP Services (WinHTTP), &\# 0034 ; WinHttpCertCfg.exe&\# 0034 ;, permet aux administrateurs d’installer et de configurer des certificats clients dans n’importe quel magasin de certificats accessible par le compte IWAM (Internet Server Web Application Manager). L’outil élimine également la nécessité d’effectuer des opérations spéciales pour les comptes, tels que le compte IWAM, pour accéder à des certificats lors de l’utilisation de pages d’Active Server (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, un outil de configuration de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4250cd717b9f611f4f23f17c93069760c283c97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113135"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a><span data-ttu-id="30045-104">WinHttpCertCfg.exe, un outil de configuration de certificat</span><span class="sxs-lookup"><span data-stu-id="30045-104">WinHttpCertCfg.exe, a Certificate Configuration Tool</span></span>

<span data-ttu-id="30045-105">L’outil de configuration de certificat [Microsoft Windows http services (WinHTTP)](about-winhttp.md) , « WinHttpCertCfg.exe », permet aux administrateurs d’installer et de configurer des certificats clients dans n’importe quel [*magasin de certificats*](glossary.md) accessible par le compte IWAM (Internet Server Web Application Manager).</span><span class="sxs-lookup"><span data-stu-id="30045-105">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) certificate configuration tool, "WinHttpCertCfg.exe", enables administrators to install and configure client certificates in any [*certificate store*](glossary.md) that can be accessed by the Internet Server Web Application Manager (IWAM) account.</span></span> <span data-ttu-id="30045-106">L’outil élimine également la nécessité d’effectuer des opérations spéciales pour les comptes, tels que le compte IWAM, pour accéder à des certificats lors de l’utilisation de pages d’Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="30045-106">The tool also eliminates the need to do anything special to accounts such as the IWAM account to gain access to certificates when using Active Server Pages (ASP).</span></span>

<span data-ttu-id="30045-107">La console MMC (Microsoft Management Console) permet aux administrateurs d’importer des certificats client sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="30045-107">The Microsoft Management Console (MMC) enables administrators to import client certificates to a local computer.</span></span> <span data-ttu-id="30045-108">Toutefois, l’importation d’un certificat n’accorde pas automatiquement l’accès à la clé privée pour d’autres comptes.</span><span class="sxs-lookup"><span data-stu-id="30045-108">However, importing a certificate does not automatically grant access to the private key for other accounts.</span></span> <span data-ttu-id="30045-109">Cette clé privée est requise pour l’authentification par certificat client.</span><span class="sxs-lookup"><span data-stu-id="30045-109">This private key is required for client certificate authentication.</span></span> <span data-ttu-id="30045-110">L’outil de configuration de certificat Microsoft Windows HTTP Services (WinHTTP) offre la possibilité d’accorder l’accès à des comptes supplémentaires, tels que le compte IWAM, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="30045-110">The Microsoft Windows HTTP Services (WinHTTP) certificate configuration tool provides the ability to grant access to additional accounts, such as the IWAM account, when required.</span></span>

-   [<span data-ttu-id="30045-111">Utilisation de l’outil de configuration de certificat</span><span class="sxs-lookup"><span data-stu-id="30045-111">Using the Certificate Configuration Tool</span></span>](#using-the-certificate-configuration-tool)
-   [<span data-ttu-id="30045-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="30045-112">Examples</span></span>](#examples)

## <a name="using-the-certificate-configuration-tool"></a><span data-ttu-id="30045-113">Utilisation de l’outil de configuration de certificat</span><span class="sxs-lookup"><span data-stu-id="30045-113">Using the Certificate Configuration Tool</span></span>

<span data-ttu-id="30045-114">L’outil de configuration de certificat WinHTTP, WinHttpCertCfg.exe, est disponible en téléchargement sur le site Web des [outils du kit de ressources Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="30045-114">The WinHTTP certificate configuration tool, WinHttpCertCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="30045-115">L’exemple de code suivant montre les paramètres de ligne de commande valides à utiliser avec cet outil.</span><span class="sxs-lookup"><span data-stu-id="30045-115">The following example code shows the valid command line parameters to use with this tool.</span></span>

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

<span data-ttu-id="30045-116">Le tableau suivant répertorie les paramètres de l’outil de configuration de.</span><span class="sxs-lookup"><span data-stu-id="30045-116">The following table lists parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30045-117">Paramètre</span><span class="sxs-lookup"><span data-stu-id="30045-117">Parameter</span></span></th>
<th><span data-ttu-id="30045-118">Description</span><span class="sxs-lookup"><span data-stu-id="30045-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30045-119">-?</span><span class="sxs-lookup"><span data-stu-id="30045-119">-?</span></span></td>
<td><span data-ttu-id="30045-120">Affiche les données de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="30045-120">Displays syntax data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30045-121">-i</span><span class="sxs-lookup"><span data-stu-id="30045-121">-i</span></span></td>
<td><span data-ttu-id="30045-122">Spécifie que le certificat doit être importé à partir d’un fichier d’échange d’informations personnelles (PFX).</span><span class="sxs-lookup"><span data-stu-id="30045-122">Specifies that the certificate is to be imported from a Personal Information Exchange (PFX) file.</span></span> <span data-ttu-id="30045-123">Ce paramètre doit être suivi du nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="30045-123">This parameter must be followed by the name of the file.</span></span> <span data-ttu-id="30045-124">Lorsque ce paramètre est spécifié, &quot; -a &quot; et &quot; -c &quot; doivent également être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="30045-124">When this parameter is specified, &quot;-a&quot; and &quot;-c&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30045-125">-g</span><span class="sxs-lookup"><span data-stu-id="30045-125">-g</span></span></td>
<td><span data-ttu-id="30045-126">Spécifie que l’accès est accordé à une clé privée.</span><span class="sxs-lookup"><span data-stu-id="30045-126">Specifies that access is granted to a private key.</span></span> <span data-ttu-id="30045-127">Lorsque ce paramètre est spécifié, &quot; -a &quot; , &quot; -c &quot; et &quot; -s &quot; doivent également être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="30045-127">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30045-128">-r</span><span class="sxs-lookup"><span data-stu-id="30045-128">-r</span></span></td>
<td><span data-ttu-id="30045-129">Spécifie que l’accès est supprimé pour une clé privée.</span><span class="sxs-lookup"><span data-stu-id="30045-129">Specifies that access is removed for a private key.</span></span> <span data-ttu-id="30045-130">Lorsque ce paramètre est spécifié, &quot; -a &quot; , &quot; -c &quot; et &quot; -s &quot; doivent également être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="30045-130">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30045-131">-l</span><span class="sxs-lookup"><span data-stu-id="30045-131">-l</span></span></td>
<td><span data-ttu-id="30045-132">Spécifie que les comptes ayant accès à une clé privée sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="30045-132">Specifies that accounts with access to a private key are listed.</span></span> <span data-ttu-id="30045-133">Lorsque ce paramètre est spécifié, &quot; -c &quot; et &quot; -s &quot; doivent également être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="30045-133">When this parameter is specified, &quot;-c&quot; and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30045-134">-a</span><span class="sxs-lookup"><span data-stu-id="30045-134">-a</span></span></td>
<td><span data-ttu-id="30045-135">Spécifie le compte d’utilisateur sur l’ordinateur en cours de configuration.</span><span class="sxs-lookup"><span data-stu-id="30045-135">Specifies the user account on the machine being configured.</span></span> <span data-ttu-id="30045-136">Il peut s’agir d’un ordinateur local ou d’un compte de domaine, tel que &quot; IWAM_TESTMACHINE &quot; , &quot; TESTUSER &quot; ou &quot; TESTDOMAIN\DOMAINUSER &quot; .</span><span class="sxs-lookup"><span data-stu-id="30045-136">This could be a local machine or domain account, such as &quot;IWAM_TESTMACHINE&quot;, &quot;TESTUSER&quot;, or &quot;TESTDOMAIN\DOMAINUSER&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30045-137">-c</span><span class="sxs-lookup"><span data-stu-id="30045-137">-c</span></span></td>
<td><span data-ttu-id="30045-138">Spécifie l’emplacement et le nom du <a href="glossary.md"><em>magasin de certificats</em></a>.</span><span class="sxs-lookup"><span data-stu-id="30045-138">Specifies the location and name of the <a href="glossary.md"><em>certificate store</em></a>.</span></span> <span data-ttu-id="30045-139">Utilisez &quot; LOCAL_MACHINE &quot; ou &quot; CURRENT_USER &quot; pour désigner la branche du Registre à utiliser pour l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="30045-139">Use &quot;LOCAL_MACHINE&quot; or &quot;CURRENT_USER&quot; to designate which registry branch to use for the location.</span></span> <span data-ttu-id="30045-140">Le <em>magasin de certificats</em> peut être installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30045-140">The <em>certificate store</em> can be any installed on the machine.</span></span> <span data-ttu-id="30045-141">Les exemples de noms standard sont &quot; My &quot; , &quot; root &quot; et &quot; TrustedPeople &quot; .</span><span class="sxs-lookup"><span data-stu-id="30045-141">Typical name examples are &quot;MY&quot;, &quot;Root&quot;, and &quot;TrustedPeople&quot;.</span></span> <span data-ttu-id="30045-142">L’emplacement et le nom du <em>magasin de certificats</em> sont séparés par une barre oblique inverse, par exemple, &quot; LOCAL_MACHINE \Root &quot; .</span><span class="sxs-lookup"><span data-stu-id="30045-142">The location and name of the <em>certificate store</em> are separated with a backward slash, for example, &quot;LOCAL_MACHINE\Root&quot;.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="30045-143">Bien que la &quot; CURRENT_USER &quot; branche du Registre puisse être spécifiée avec ce paramètre, l’extension de l’accès aux clés privées est principalement destinée aux certificats installés dans un <a href="glossary.md"><em>magasin de certificats</em></a> d’ordinateur local accessible par plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="30045-143">Although the &quot;CURRENT_USER&quot; branch of the registry can be specified with this parameter, extending access to private keys is primarily intended for certificates installed in a local computer <a href="glossary.md"><em>certificate store</em></a> that can be accessed by multiple users.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30045-144">-S</span><span class="sxs-lookup"><span data-stu-id="30045-144">-s</span></span></td>
<td><span data-ttu-id="30045-145">Spécifie une chaîne de recherche ne respectant pas la casse pour rechercher le premier certificat énuméré avec un nom d’objet qui contient cette sous-chaîne.</span><span class="sxs-lookup"><span data-stu-id="30045-145">Specifies a case-insensitive search string for finding the first enumerated certificate with a subject name that contains this substring.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30045-146">-p</span><span class="sxs-lookup"><span data-stu-id="30045-146">-p</span></span></td>
<td><span data-ttu-id="30045-147">Spécifie un mot de passe utilisé pour importer le certificat et la clé privée.</span><span class="sxs-lookup"><span data-stu-id="30045-147">Specifies a password that is used to import the certificate and the private key.</span></span> <span data-ttu-id="30045-148">Utilisé uniquement avec l’option d’importation.</span><span class="sxs-lookup"><span data-stu-id="30045-148">This is only used with the import option.</span></span></td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> <span data-ttu-id="30045-149">L’utilisateur doit disposer des privilèges suffisants pour utiliser cet outil, ce qui nécessite que l’utilisateur soit un administrateur et le même utilisateur qui a installé le certificat client, s’il est installé.</span><span class="sxs-lookup"><span data-stu-id="30045-149">The user must have sufficient privileges to use this tool, which requires the user to be an administrator and the same user who installed the client certificate, if installed.</span></span>
>
> <span data-ttu-id="30045-150">L’outil « WinHttpCertCfg.exe » n’est pas utile pour configurer des certificats stockés dans un système de fichiers tel que FAT32, qui ne prend pas en charge les listes de contrôle d’accès (ACL).</span><span class="sxs-lookup"><span data-stu-id="30045-150">The "WinHttpCertCfg.exe" tool is not useful to configure certificates stored in a file system such as FAT32, which does not support access control lists (ACL).</span></span>

## <a name="examples"></a><span data-ttu-id="30045-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="30045-151">Examples</span></span>

<span data-ttu-id="30045-152">Les exemples suivants illustrent quelques-unes des façons dont l’outil de configuration peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="30045-152">The following examples show some of the ways in which the configuration tool can be used.</span></span>

1.  <span data-ttu-id="30045-153">Cette commande répertorie les comptes qui ont accès à la clé privée pour le certificat « MyCertificate » dans le [*magasin de certificats*](glossary.md) « racine » de la \_ branche de l’ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="30045-153">This command lists accounts that have access to the private key for the "MyCertificate" certificate in the "Root" [*certificate store*](glossary.md) of the LOCAL\_MACHINE branch of the registry.</span></span>

    <span data-ttu-id="30045-154">**WinHttpCertCfg-l-c \_ racine de l’ordinateur local \\ -s MyCertificate**</span><span class="sxs-lookup"><span data-stu-id="30045-154">**winhttpcertcfg -l -c LOCAL\_MACHINE\\Root -s MyCertificate**</span></span>

2.  <span data-ttu-id="30045-155">Cette commande accorde l’accès à la clé privée du certificat « MyCertificate » dans le [*magasin de certificats*](glossary.md) « My » pour le compte Utilisateurtest.</span><span class="sxs-lookup"><span data-stu-id="30045-155">This command grants access to the private key of the "MyCertificate" certificate in the "My" [*certificate store*](glossary.md) for the TESTUSER account.</span></span>

    <span data-ttu-id="30045-156">**WinHttpCertCfg-g-c \_ machine locale \\ My-s MyCertificate-a TESTUSER**</span><span class="sxs-lookup"><span data-stu-id="30045-156">**winhttpcertcfg -g -c LOCAL\_MACHINE\\My -s MyCertificate -a TESTUSER**</span></span>

3.  <span data-ttu-id="30045-157">Cette commande importe un certificat et une clé privée à partir d’un fichier PFX et étend l’accès à la clé privée à un autre compte.</span><span class="sxs-lookup"><span data-stu-id="30045-157">This command imports a certificate and private key from a PFX file and extends private key access to another account.</span></span>

    <span data-ttu-id="30045-158">**WinHttpCertCfg-i PFXFile-c \_ ordinateur local \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**</span><span class="sxs-lookup"><span data-stu-id="30045-158">**winhttpcertcfg -i PFXFile -c LOCAL\_MACHINE\\My -a IWAM\_TESTMACHINE -p PFXPassword**</span></span>

4.  <span data-ttu-id="30045-159">Cette commande refuse l’accès à la clé privée pour le \_ compte IWAM TESTMACHINE avec le certificat spécifié.</span><span class="sxs-lookup"><span data-stu-id="30045-159">This command denies access to the private key for the IWAM\_TESTMACHINE account with the specified certificate.</span></span>

    <span data-ttu-id="30045-160">**WinHttpCertCfg-r-c \_ racine de l’ordinateur local \\ -s MyCertificate-a IWAM \_ TESTMACHINE**</span><span class="sxs-lookup"><span data-stu-id="30045-160">**winhttpcertcfg -r -c LOCAL\_MACHINE\\Root -s MyCertificate -a IWAM\_TESTMACHINE**</span></span>

 

 




