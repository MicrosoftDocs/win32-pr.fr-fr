---
title: Erreurs courantes (ADSI)
description: Toutes les erreurs spécifiques à ADSI ont une forme hexadécimale de 80005xxx. Les codes d’erreur les plus courants sont décrits dans le tableau suivant.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "104314020"
---
# <a name="common-errors-adsi"></a><span data-ttu-id="1d7fb-104">Erreurs courantes (ADSI)</span><span class="sxs-lookup"><span data-stu-id="1d7fb-104">Common Errors (ADSI)</span></span>

<span data-ttu-id="1d7fb-105">Toutes les erreurs spécifiques à ADSI ont une forme hexadécimale de 80005xxx.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-105">All ADSI-specific errors have a hexadecimal form of 80005xxx.</span></span> <span data-ttu-id="1d7fb-106">Les codes d’erreur les plus courants sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-106">The most common error codes encountered are outlined in the following table.</span></span>



| <span data-ttu-id="1d7fb-107">Code d’erreur hexadécimal ADSI</span><span class="sxs-lookup"><span data-stu-id="1d7fb-107">ADSI hex error code</span></span> | <span data-ttu-id="1d7fb-108">Description</span><span class="sxs-lookup"><span data-stu-id="1d7fb-108">Description</span></span>                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d7fb-109">80005000</span><span class="sxs-lookup"><span data-stu-id="1d7fb-109">80005000</span></span><br/> | <span data-ttu-id="1d7fb-110">Un chemin d’accès ADSI non valide a été passé.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-110">An invalid ADSI pathname was passed.</span></span> <span data-ttu-id="1d7fb-111">Cette erreur est due au passage d’un ADsPath mal formé à **GetObject** lors de la liaison à un objet.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-111">This error results from passing a poorly formed ADsPath to **GetObject** when binding to an object.</span></span><br/> |
| <span data-ttu-id="1d7fb-112">8000500D</span><span class="sxs-lookup"><span data-stu-id="1d7fb-112">8000500D</span></span><br/> | <span data-ttu-id="1d7fb-113">La propriété ADSI est introuvable dans le cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-113">The ADSI property cannot be found in the property cache.</span></span><br/>                                                                                 |
| <span data-ttu-id="1d7fb-114">8000500E</span><span class="sxs-lookup"><span data-stu-id="1d7fb-114">8000500E</span></span><br/> | <span data-ttu-id="1d7fb-115">L’objet ADSI existe.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-115">The ADSI object exists.</span></span> <span data-ttu-id="1d7fb-116">Si vous tentez de créer un objet ADSI portant le même nom qu’un objet ADSI existant, cette erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-116">If you attempt to create an ADSI object with the same name as an existing ADSI object, this error will occur.</span></span><br/>    |



 

<span data-ttu-id="1d7fb-117">Pour obtenir la liste complète des codes d’erreur ADSI, consultez [codes d’erreur ADSI génériques](generic-adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1d7fb-117">For a complete list of ADSI error codes, see [Generic ADSI Error Codes](generic-adsi-error-codes.md).</span></span>

## <a name="com-errors"></a><span data-ttu-id="1d7fb-118">Erreurs COM</span><span class="sxs-lookup"><span data-stu-id="1d7fb-118">COM Errors</span></span>

<span data-ttu-id="1d7fb-119">Étant donné que l’interface ADSI est composée d’objets COM, elle renverra des codes d’erreur COM standard.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-119">Since ADSI is composed of COM objects, it will return standard COM error codes.</span></span> <span data-ttu-id="1d7fb-120">Le tableau suivant répertorie les codes d’erreur COM les plus couramment rencontrés dans la programmation ADSI.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-120">The following table lists the COM error codes most commonly encountered in ADSI programming.</span></span>



| <span data-ttu-id="1d7fb-121">Code d’erreur hexadécimal COM</span><span class="sxs-lookup"><span data-stu-id="1d7fb-121">COM hex error code</span></span>  | <span data-ttu-id="1d7fb-122">Description</span><span class="sxs-lookup"><span data-stu-id="1d7fb-122">Description</span></span>                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d7fb-123">80004005</span><span class="sxs-lookup"><span data-stu-id="1d7fb-123">80004005</span></span><br/> | <span data-ttu-id="1d7fb-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-124">Unspecified error.</span></span> <span data-ttu-id="1d7fb-125">La cause de l’échec de l’objet COM est indéterminée par ADSI.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-125">The cause of the COM object failure is indeterminate by ADSI.</span></span> <br/>                                  |
| <span data-ttu-id="1d7fb-126">800041E4</span><span class="sxs-lookup"><span data-stu-id="1d7fb-126">800041E4</span></span><br/> | <span data-ttu-id="1d7fb-127">Objet introuvable.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-127">Object not found.</span></span> <span data-ttu-id="1d7fb-128">Cette erreur se produit principalement en raison d’une mauvaise orthographe de la chaîne ADsPath lors de la liaison à un objet.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-128">This error predominantly occurs due to misspelling the ADsPath string when binding to an object.</span></span><br/> |



 

<span data-ttu-id="1d7fb-129">Consultez [codes d’erreur com génériques](generic-com-error-codes.md) pour obtenir d’autres exemples d’erreurs com susceptibles de se produire dans la programmation ADSI.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-129">See [Generic COM Error Codes](generic-com-error-codes.md) for a few more examples of COM errors that may occur in ADSI programming.</span></span>

## <a name="win32-errors"></a><span data-ttu-id="1d7fb-130">Erreurs Win32</span><span class="sxs-lookup"><span data-stu-id="1d7fb-130">Win32 Errors</span></span>

<span data-ttu-id="1d7fb-131">Tout code d’erreur de forme hexadécimale 8007xxxx est un code d’erreur Win32 standard.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-131">Any error code of the hexadecimal form 8007xxxx is a standard Win32 error code.</span></span> <span data-ttu-id="1d7fb-132">Si vous convertissez les quatre derniers chiffres du format hexadécimal au format décimal, vous pouvez accéder à l’erreur à partir de la ligne de commande Windows 2000 :</span><span class="sxs-lookup"><span data-stu-id="1d7fb-132">If you convert the last four digits from hexadecimal to decimal, you can access the error from the Windows 2000 command line:</span></span>

<span data-ttu-id="1d7fb-133">**net helpmsg <number>**</span><span class="sxs-lookup"><span data-stu-id="1d7fb-133">**net helpmsg <number>**</span></span>

<span data-ttu-id="1d7fb-134">Dans la ligne de commande ci-dessus, « &lt; Number &gt; » est le nombre décimal obtenu en convertissant les quatre derniers chiffres du code d’erreur au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-134">In the command line above, "&lt;number&gt;" is the decimal number obtained by converting the last four digits of the error code from hexadecimal.</span></span> <span data-ttu-id="1d7fb-135">Cette ligne de commande fournit une description plus utile de l’erreur Win32, qui peut vous aider à déboguer votre script.</span><span class="sxs-lookup"><span data-stu-id="1d7fb-135">This command line will provide a more useful description of the Win32 error, which can be of great help in debugging your script.</span></span>

 

 





