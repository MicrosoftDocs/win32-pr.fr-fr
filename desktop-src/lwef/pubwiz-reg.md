---
title: Inscription d’un service
description: Pour ajouter votre service à la liste des fournisseurs dans l’Assistant Publication de sites Web ou l’Assistant commande d’impression en ligne, vous devez ajouter la clé appropriée et ses valeurs au registre Windows.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- inscription, services
- Assistant Publication de sites Web, inscription
- Assistant commande d’impression en ligne, inscription
- inscrire, Assistant Publication de sites Web
- inscrire, Assistant commande d’impression en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104211655"
---
# <a name="registering-a-service"></a><span data-ttu-id="7bc3f-108">Inscription d’un service</span><span class="sxs-lookup"><span data-stu-id="7bc3f-108">Registering a Service</span></span>

<span data-ttu-id="7bc3f-109">Pour ajouter votre service à la liste des fournisseurs dans l’Assistant Publication de sites Web ou l’Assistant commande d’impression en ligne, vous devez ajouter la clé appropriée et ses valeurs au registre Windows.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-109">To add your service to the list of providers in either the Web Publishing Wizard or the Online Print Ordering Wizard, you must add the appropriate key and its values to the Windows registry.</span></span>

## <a name="required-keys-and-values"></a><span data-ttu-id="7bc3f-110">Clés et valeurs requises</span><span class="sxs-lookup"><span data-stu-id="7bc3f-110">Required Keys and Values</span></span>

<span data-ttu-id="7bc3f-111">Pour ajouter votre service à la liste des fournisseurs de l’Assistant Publication de sites Web, ajoutez une clé comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-111">To add your service to the list of providers for the Web Publishing Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="7bc3f-112">Pour ajouter votre service à la liste des fournisseurs de l’Assistant commande d’impression en ligne, ajoutez une clé comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-112">To add your service to the list of providers for the Online Print Ordering Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="7bc3f-113">Chacune des valeurs est une chaîne de type REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-113">Each of the values is a string of type REG\_SZ.</span></span> <span data-ttu-id="7bc3f-114">Fournissez ses données comme expliqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-114">Provide its data as explained in the following table.</span></span> 

| <span data-ttu-id="7bc3f-115">Nom de la valeur</span><span class="sxs-lookup"><span data-stu-id="7bc3f-115">Value Name</span></span>     | <span data-ttu-id="7bc3f-116">Explication</span><span class="sxs-lookup"><span data-stu-id="7bc3f-116">Explanation</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc3f-117">IconPath</span><span class="sxs-lookup"><span data-stu-id="7bc3f-117">IconPath</span></span>       | <span data-ttu-id="7bc3f-118">Chemin d’accès complet au fichier d’icône, y compris le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-118">The full path to the icon file, including the file name.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7bc3f-119">DisplayName</span><span class="sxs-lookup"><span data-stu-id="7bc3f-119">DisplayName</span></span>    | <span data-ttu-id="7bc3f-120">Nom affiché pour votre service dans la liste des fournisseurs de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-120">The name displayed for your service in the wizard's providers list.</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="7bc3f-121">Description</span><span class="sxs-lookup"><span data-stu-id="7bc3f-121">Description</span></span>    | <span data-ttu-id="7bc3f-122">Brève description de votre service.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-122">A short description for your service.</span></span> <span data-ttu-id="7bc3f-123">Cette description s’affiche également dans la liste des fournisseurs de l’Assistant, directement sous le nom de votre service.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-123">This description also displays in the wizard's providers list directly below the name of your service.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="7bc3f-124">HREF</span><span class="sxs-lookup"><span data-stu-id="7bc3f-124">HREF</span></span>           | <span data-ttu-id="7bc3f-125">URL de la première page de votre service.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-125">The URL of the first page of your service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7bc3f-126">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="7bc3f-126">SupportedTypes</span></span> | <span data-ttu-id="7bc3f-127">Types de fichiers pris en charge par votre service.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-127">The file types supported by your service.</span></span> <span data-ttu-id="7bc3f-128">Par exemple, *\* . jpg*.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-128">For instance, *\*.jpg*.</span></span> <span data-ttu-id="7bc3f-129">En spécifiant uniquement certains types de fichiers, votre service s’affiche uniquement lorsque ces types de fichiers ont été sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-129">By specifying only certain file types, your service only appears when those file types have been selected.</span></span> <span data-ttu-id="7bc3f-130">Si plusieurs types de fichier ont été sélectionnés, votre service s’affiche si l’un de ces types de fichiers est pris en charge par votre service.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-130">If more than one file type has been selected, your service appears if any of those file types are supported by your service.</span></span> <span data-ttu-id="7bc3f-131">Si vous souhaitez spécifier plusieurs types de fichiers, séparez-les par des points-virgules dans la liste.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-131">If you want to specify multiple file types, separate them in the list with semicolons.</span></span> <span data-ttu-id="7bc3f-132">Par exemple, *\* . jpg ; \* . BMP*.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-132">For example, *\*.jpg; \*.bmp*.</span></span> |



 

<span data-ttu-id="7bc3f-133">Voici un exemple complet pour un service de traitement des photos nommé « MyProvider ».</span><span class="sxs-lookup"><span data-stu-id="7bc3f-133">The following is a complete example for a photo processing service entitled "MyProvider."</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

<span data-ttu-id="7bc3f-134">Lorsque l’URL de votre service est appelée, deux valeurs sont ajoutées à la fin de l’URL : LCID et langid.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-134">When the URL of your service is called, two values are added to the end of the URL—lcid and langid.</span></span> <span data-ttu-id="7bc3f-135">Par exemple, la chaîne d’URL de l’exemple ci-dessus peut être https : \/ /www.MyProvider.com/Intro.htm ? LCID = 1033&LangID = 1033.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-135">For example, the URL string for the example above might be https:\//www.MyProvider.com/Intro.htm?lcid=1033&langid=1033.</span></span> <span data-ttu-id="7bc3f-136">Ces variables sont utilisées pour les informations de langue et de localisation.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-136">These variables are used for language and localization information.</span></span>

-   <span data-ttu-id="7bc3f-137">**LCID** est utilisé pour informer le serveur des paramètres pays/région et langue du client.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-137">**lcid** is used to inform the server of the client's country/region and language settings.</span></span> <span data-ttu-id="7bc3f-138">Elle n’est pas utilisée pour déterminer la langue de l’interface utilisateur du client, mais elle est utilisée pour déterminer le format approprié pour la devise, la date et l’heure, ainsi que pour d’autres données spécifiques à la région.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-138">It is not used to determine the language of the client's UI, but is used to determine the proper format for currency, date and time, and other region-specific data.</span></span>
-   <span data-ttu-id="7bc3f-139">**LangID** est utilisé pour informer le serveur du paramètre de langue par défaut du client afin qu’il puisse utiliser la langue appropriée dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7bc3f-139">**langid** is used to inform the server of the client's default language setting so that it can use the proper language in the UI.</span></span>

 

 




