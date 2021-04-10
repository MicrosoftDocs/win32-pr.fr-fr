---
description: Explique comment utiliser SignTool pour signer un fichier.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Utilisation de SignTool pour signer un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114119"
---
# <a name="using-signtool-to-sign-a-file"></a><span data-ttu-id="3470e-103">Utilisation de SignTool pour signer un fichier</span><span class="sxs-lookup"><span data-stu-id="3470e-103">Using SignTool to Sign a File</span></span>

<span data-ttu-id="3470e-104">La commande suivante signe le fichier nommé MyControl.exe à l’aide d’un [*certificat*](../secgloss/c-gly.md) stocké dans un fichier d’échange d’informations personnelles (pfx) :</span><span class="sxs-lookup"><span data-stu-id="3470e-104">The following command signs the file named MyControl.exe using a [*certificate*](../secgloss/c-gly.md) stored in a Personal Information Exchange (PFX) file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

<span data-ttu-id="3470e-105">La commande suivante signe le fichier à l’aide d’un certificat stocké dans un fichier PFX protégé par mot de passe :</span><span class="sxs-lookup"><span data-stu-id="3470e-105">The following command signs the file using a certificate stored in a password-protected PFX file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="3470e-106">Veillez à protéger correctement le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3470e-106">Ensure that you properly protect the password.</span></span>

 

<span data-ttu-id="3470e-107">La commande suivante signe et horodatage le fichier :</span><span class="sxs-lookup"><span data-stu-id="3470e-107">The following command signs and time stamps the file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="3470e-108">Pour plus d’informations sur l’horodatage d’un fichier après qu’il a déjà été signé, consultez [Ajout d’horodatages à des fichiers précédemment signés](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="3470e-108">For information about time stamping a file after it has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span>

 

<span data-ttu-id="3470e-109">La commande suivante signe le fichier à l’aide d’un certificat situé dans mon magasin avec le nom d’objet de l’éditeur de l’entreprise :</span><span class="sxs-lookup"><span data-stu-id="3470e-109">The following command signs the file using a certificate located in the My store with a subject name of My Company Publisher:</span></span>

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

<span data-ttu-id="3470e-110">La commande suivante signe un contrôle ActiveX et fournit des informations qui sont affichées par Internet Explorer lorsque l’utilisateur est invité à installer le contrôle :</span><span class="sxs-lookup"><span data-stu-id="3470e-110">The following command signs an ActiveX control and provides information that is displayed by Internet Explorer when the user is prompted to install the control:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

<span data-ttu-id="3470e-111">La commande suivante signe le fichier à l’aide d’un certificat dont les informations de [*clé privée*](../secgloss/p-gly.md) sont protégées par un module de chiffrement matériel.</span><span class="sxs-lookup"><span data-stu-id="3470e-111">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="3470e-112">À titre d’exemple, supposons que le certificat appelé « My High-Value Certificate » dispose d’une clé privée installée dans un module de chiffrement matériel et que le certificat soit correctement installé.</span><span class="sxs-lookup"><span data-stu-id="3470e-112">For example purposes, assume that the certificate called "My High-Value Certificate," has a private key installed in a hardware cryptography module, and the certificate is properly installed.</span></span>

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

<span data-ttu-id="3470e-113">La commande suivante signe le fichier à l’aide d’un certificat dont les informations de [*clé privée*](../secgloss/p-gly.md) sont protégées par un module de chiffrement matériel.</span><span class="sxs-lookup"><span data-stu-id="3470e-113">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="3470e-114">Un magasin d’ordinateurs est spécifié pour le magasin de l' [*autorité de certification*](../secgloss/c-gly.md) (ca).</span><span class="sxs-lookup"><span data-stu-id="3470e-114">A computer store is specified for the [*certification authority*](../secgloss/c-gly.md) (CA) store.</span></span>

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

<span data-ttu-id="3470e-115">La commande suivante signe le fichier à l’aide d’un certificat stocké dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="3470e-115">The following command signs the file using a certificate stored in a file.</span></span> <span data-ttu-id="3470e-116">Les informations de la clé privée sont protégées par un module de chiffrement matériel, et le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et le [*conteneur de clé*](../secgloss/k-gly.md) sont spécifiés par leur nom.</span><span class="sxs-lookup"><span data-stu-id="3470e-116">The private key information is protected by a hardware cryptography module, and the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP)and [*key container*](../secgloss/k-gly.md) are specified by name.</span></span> <span data-ttu-id="3470e-117">Cette commande est utile si le certificat n’est pas installé correctement.</span><span class="sxs-lookup"><span data-stu-id="3470e-117">This command is useful if the certificate is not properly installed.</span></span>

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

<span data-ttu-id="3470e-118">[SignTool](signtool.md) retourne le texte de ligne de commande qui indique le résultat de l’opération de signature.</span><span class="sxs-lookup"><span data-stu-id="3470e-118">[SignTool](signtool.md) returns command line text that states the result of the signing operation.</span></span> <span data-ttu-id="3470e-119">En outre, SignTool retourne un code de sortie de zéro pour une exécution réussie, un pour l’échec de l’exécution et deux pour l’exécution qui s’est terminée avec des avertissements.</span><span class="sxs-lookup"><span data-stu-id="3470e-119">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="3470e-120">Pour plus d’informations sur la vérification de la signature d’un fichier, consultez [utilisation de SignTool pour vérifier une signature de fichier](using-signtool-to-verify-a-file-signature.md).</span><span class="sxs-lookup"><span data-stu-id="3470e-120">For information about verifying a file's signature, see [Using SignTool to Verify a File Signature](using-signtool-to-verify-a-file-signature.md).</span></span> <span data-ttu-id="3470e-121">Pour plus d’informations sur l’ajout d’un horodatage si le fichier a déjà été signé, consultez [Ajout d’horodatages à des fichiers précédemment signés](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="3470e-121">For information about adding a time stamp if the file has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span> <span data-ttu-id="3470e-122">Pour plus d’informations sur [SignTool](signtool.md), consultez [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="3470e-122">For additional information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 
