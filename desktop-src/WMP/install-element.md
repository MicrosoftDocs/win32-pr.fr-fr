---
title: Élément d’installation
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’élément install spécifie les valeurs utilisées par le lecteur Windows Media pour installer un magasin en ligne.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Installer l’élément Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540195"
---
# <a name="install-element"></a><span data-ttu-id="e25a6-106">Élément d’installation</span><span class="sxs-lookup"><span data-stu-id="e25a6-106">Install Element</span></span>

> [!Note]  
> <span data-ttu-id="e25a6-107">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="e25a6-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e25a6-108">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e25a6-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e25a6-109">L’élément **install** spécifie les valeurs utilisées par le lecteur Windows Media pour installer un magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e25a6-109">The **Install** element specifies values used by Windows Media Player to install an online store.</span></span>

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="e25a6-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="e25a6-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="e25a6-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="e25a6-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="e25a6-112">URL complète d’un fichier dont l’extension de nom de fichier. txt est utilisée par le lecteur Windows Media pour afficher un contrat de licence utilisateur final (CLUF).</span><span class="sxs-lookup"><span data-stu-id="e25a6-112">Fully qualified URL for a file with a .txt file name extension that Windows Media Player uses to display an End User License Agreement (EULA).</span></span> <span data-ttu-id="e25a6-113">Ce fichier doit être encodé au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e25a6-113">This file must be encoded in ANSI format.</span></span>

</dd> <dt>

<span data-ttu-id="e25a6-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="e25a6-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="e25a6-115">URL complète d’un package, avec une extension de nom de fichier. cab, utilisée pour installer le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e25a6-115">Fully qualified URL for a package, with a .cab file name extension, that is used to install the online store.</span></span> <span data-ttu-id="e25a6-116">Le package et tous les modules de code du package doivent être signés.</span><span class="sxs-lookup"><span data-stu-id="e25a6-116">The package and all code modules in the package must be signed.</span></span> <span data-ttu-id="e25a6-117">Pour plus d’informations sur la signature de code, consultez [Introduction à la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) dans MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="e25a6-117">For information about code signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in the MSDN Library.</span></span>

</dd> <dt>

<span data-ttu-id="e25a6-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="e25a6-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="e25a6-119">URL complète d’une page Web qui contient des informations sur les stratégies de confidentialité de la boutique en ligne.</span><span class="sxs-lookup"><span data-stu-id="e25a6-119">Fully qualified URL for a webpage that contains privacy policy information for the online store.</span></span>

</dd> <dt>

<span data-ttu-id="e25a6-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="e25a6-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (required)</span></span>
</dt> <dd>

<span data-ttu-id="e25a6-121">Nom du fichier EXE ou INF à exécuter.</span><span class="sxs-lookup"><span data-stu-id="e25a6-121">Name of the EXE or INF file to run.</span></span> <span data-ttu-id="e25a6-122">Ce fichier doit être contenu dans le fichier CAB spécifié par l’attribut **CodeURL** .</span><span class="sxs-lookup"><span data-stu-id="e25a6-122">This file must be contained in the CAB file specified by the **CodeURL** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="e25a6-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e25a6-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="e25a6-124">Chaîne de ligne de commande qui est transmise à l’application spécifiée par l’attribut **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="e25a6-124">Command-line string that is passed to the application specified by the **InstallApp** attribute.</span></span> <span data-ttu-id="e25a6-125">Cet attribut s’applique uniquement lorsque la valeur de **InstallApp** spécifie un exécutable.</span><span class="sxs-lookup"><span data-stu-id="e25a6-125">This attribute is only applicable when the value for **InstallApp** specifies an executable.</span></span>

</dd> <dt>

<span data-ttu-id="e25a6-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (obligatoire pour le type 1, ignoré pour le type 2)</span><span class="sxs-lookup"><span data-stu-id="e25a6-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (required for type 1, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="e25a6-127">URL complète du catalogue compilé de la boutique en ligne.</span><span class="sxs-lookup"><span data-stu-id="e25a6-127">Fully qualified URL for the online store's compiled catalog.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="e25a6-128">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="e25a6-128">Parent/Child Elements</span></span>



| <span data-ttu-id="e25a6-129">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="e25a6-129">Hierarchy</span></span>       | <span data-ttu-id="e25a6-130">Élément</span><span class="sxs-lookup"><span data-stu-id="e25a6-130">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="e25a6-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e25a6-131">Parent elements</span></span> | <span data-ttu-id="e25a6-132">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e25a6-132">**ServiceInfo**</span></span> |
| <span data-ttu-id="e25a6-133">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e25a6-133">Child elements</span></span>  | <span data-ttu-id="e25a6-134">Aucune</span><span class="sxs-lookup"><span data-stu-id="e25a6-134">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="e25a6-135">Notes</span><span class="sxs-lookup"><span data-stu-id="e25a6-135">Remarks</span></span>

<span data-ttu-id="e25a6-136">Si l’un des attributs requis est manquant ou n’est pas disponible, le programme d’installation du lecteur Windows Media ne tente pas de télécharger et d’installer le code du fournisseur de la Banque d’aide en ligne.</span><span class="sxs-lookup"><span data-stu-id="e25a6-136">If any of the required attributes are missing or not available, Windows Media Player setup will not attempt to download and install the online store provider code.</span></span> <span data-ttu-id="e25a6-137">Le programme d’installation configure les valeurs par défaut hors connexion comme spécifié dans le document **serviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="e25a6-137">Setup will configure the offline default values as specified in the **ServiceInfo** document.</span></span> <span data-ttu-id="e25a6-138">Vous pouvez utiliser **serviceInfo** quand vous n’êtes pas connecté à Internet en passant le nom du fournisseur par défaut et les informations **serviceInfo** en tant que paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e25a6-138">**ServiceInfo** can be used when not connected to the Internet by passing the default provider name and the **ServiceInfo** information as command-line parameters.</span></span> <span data-ttu-id="e25a6-139">Pour plus d’informations sur les options de ligne de commande, consultez [redistribution du logiciel du lecteur Windows Media](redistributing-windows-media-player-software.md) .</span><span class="sxs-lookup"><span data-stu-id="e25a6-139">See [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md) for details about command-line options.</span></span>

> [!Note]  
> <span data-ttu-id="e25a6-140">Pour utiliser cet élément, vous devez signer un contrat de redistribution auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e25a6-140">Use of this element requires that you sign a redistribution agreement with Microsoft.</span></span> <span data-ttu-id="e25a6-141">Pour plus d’informations, contactez votre représentant commercial.</span><span class="sxs-lookup"><span data-stu-id="e25a6-141">Contact your business representative for details.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e25a6-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e25a6-142">Requirements</span></span>



| <span data-ttu-id="e25a6-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e25a6-143">Requirement</span></span> | <span data-ttu-id="e25a6-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="e25a6-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="e25a6-145">Version</span><span class="sxs-lookup"><span data-stu-id="e25a6-145">Version</span></span><br/> | <span data-ttu-id="e25a6-146">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e25a6-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e25a6-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e25a6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e25a6-148">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="e25a6-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="e25a6-149">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="e25a6-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e25a6-150">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e25a6-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

