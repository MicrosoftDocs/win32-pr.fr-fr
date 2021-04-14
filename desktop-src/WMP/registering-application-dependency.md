---
title: Inscription de la dépendance d’application (kit de développement logiciel Windows Media Player)
description: Inscription de la dépendance d’application
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Lecteur Windows Media, paramètres du registre de dépendances des applications
- Windows Media Player, paramètres du registre de dépendances
- Lecteur Windows Media, registre
- Registre, paramètres de dépendance d’application
- Registre, paramètres de dépendance
- Registre, paramètres pour le lecteur Windows Media
- paramètres du registre des dépendances
- paramètres du registre de dépendances d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67aac78417f5ec8e4347b97a5c2b5f37db20183e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464154"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="26ec6-111">Inscription de la dépendance d’application (kit de développement logiciel Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="26ec6-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="26ec6-112">Les applications qui utilisent des API fournies par le kit de développement logiciel (SDK) du lecteur Windows Media ou le kit de développement logiciel (SDK) Windows Media format dépendent des composants d’exécution de ces technologies.</span><span class="sxs-lookup"><span data-stu-id="26ec6-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="26ec6-113">Vous pouvez inscrire votre application comme étant dépendante de ces composants dans le cadre de la configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="26ec6-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="26ec6-114">Lorsque vous inscrivez votre application, vous pouvez choisir l’un des deux niveaux de dépendance : blocage ou dépendant.</span><span class="sxs-lookup"><span data-stu-id="26ec6-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="26ec6-115">Quand une ou plusieurs applications sont inscrites avec une dépendance de blocage sur l’un des composants du runtime, le composant est bloqué d’une restauration vers une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="26ec6-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="26ec6-116">Les applications dépendantes qui ne sont pas inscrites comme bloquantes ne bloquent pas la restauration.</span><span class="sxs-lookup"><span data-stu-id="26ec6-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="26ec6-117">Au lieu de cela, avant d’effectuer la restauration, l’utilisateur affiche un message indiquant que les applications dépendent du composant.</span><span class="sxs-lookup"><span data-stu-id="26ec6-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="26ec6-118">Pour inscrire votre application, vous devez définir une valeur dans le Registre qui identifie votre application.</span><span class="sxs-lookup"><span data-stu-id="26ec6-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="26ec6-119">La valeur de Registre à définir dépend du composant dont dépend votre application.</span><span class="sxs-lookup"><span data-stu-id="26ec6-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="26ec6-120">Vous pouvez également définir deux valeurs supplémentaires par dépendance pour fournir des informations supplémentaires sur votre application.</span><span class="sxs-lookup"><span data-stu-id="26ec6-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="26ec6-121">Les valeurs de Registre suivantes sont utilisées pour inscrire la dépendance au runtime du kit de développement logiciel (SDK) du lecteur Windows Media :</span><span class="sxs-lookup"><span data-stu-id="26ec6-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="26ec6-122">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ MediaPlayer \\ installation \\ *\_ type référence* \\ application, «*application*», «*\_ chaîne d’application*»</span><span class="sxs-lookup"><span data-stu-id="26ec6-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="26ec6-123">HKEY \_ classes \_ root \\ Software racine \\ Microsoft \\ MediaPlayer \\ programme d’installation \\ descripteur de *\_ type REF* \\ , "*app*", "*Ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="26ec6-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="26ec6-124">HKEY \_ classes \_ root \\ Software racine \\ Microsoft \\ MediaPlayer \\ Setup \\ *\_ type REF* \\ , "*app*", "*WMP \_ version*"</span><span class="sxs-lookup"><span data-stu-id="26ec6-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="26ec6-125">Les valeurs de Registre suivantes sont utilisées pour inscrire la dépendance au runtime du SDK Windows Media Format :</span><span class="sxs-lookup"><span data-stu-id="26ec6-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="26ec6-126">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ application, «*application*»,*« \_ chaîne d’application*»</span><span class="sxs-lookup"><span data-stu-id="26ec6-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="26ec6-127">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ - \\ *\_* \\ descripteur de type de référence, "*application*", "*\_ descripteur de référence*"</span><span class="sxs-lookup"><span data-stu-id="26ec6-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="26ec6-128">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ version,*application*, «*\_ version WMF*»</span><span class="sxs-lookup"><span data-stu-id="26ec6-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="26ec6-129">Les variables suivantes sont utilisées dans les valeurs de Registre répertoriées ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="26ec6-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="26ec6-130">*TYPE de référence \_*</span><span class="sxs-lookup"><span data-stu-id="26ec6-130">*REF\_TYPE*</span></span>

<span data-ttu-id="26ec6-131">Remplacez par BlockingRefCounts pour le blocage de la dépendance ou par DependentRefCounts pour une dépendance non bloquante.</span><span class="sxs-lookup"><span data-stu-id="26ec6-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="26ec6-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="26ec6-132">*APP*</span></span>

<span data-ttu-id="26ec6-133">Nom ou descripteur abrégé de votre application.</span><span class="sxs-lookup"><span data-stu-id="26ec6-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="26ec6-134">Cette chaîne ne sera pas utilisée dans les messages affichés pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="26ec6-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="26ec6-135">Cette valeur est l’identificateur utilisé dans les trois valeurs de Registre associées à chacun des composants du Runtime.</span><span class="sxs-lookup"><span data-stu-id="26ec6-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="26ec6-136">*chaîne d’application \_*</span><span class="sxs-lookup"><span data-stu-id="26ec6-136">*APP\_STRING*</span></span>

<span data-ttu-id="26ec6-137">Descripteur de votre application.</span><span class="sxs-lookup"><span data-stu-id="26ec6-137">Descriptor of your application.</span></span> <span data-ttu-id="26ec6-138">Cette chaîne peut être utilisée dans les messages affichés pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="26ec6-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="26ec6-139">*descripteur de référence \_*</span><span class="sxs-lookup"><span data-stu-id="26ec6-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="26ec6-140">Description de la façon dont votre application utilise le composant.</span><span class="sxs-lookup"><span data-stu-id="26ec6-140">Description of how your application uses the component.</span></span> <span data-ttu-id="26ec6-141">Cette valeur peut inclure un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="26ec6-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="26ec6-142">*VERSION de WMP \_*</span><span class="sxs-lookup"><span data-stu-id="26ec6-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="26ec6-143">Version du lecteur Windows Media requise par votre application.</span><span class="sxs-lookup"><span data-stu-id="26ec6-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="26ec6-144">Si aucune version n’est spécifiée, la valeur par défaut est supposée être 9.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="26ec6-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="26ec6-145">*\_version WMF*</span><span class="sxs-lookup"><span data-stu-id="26ec6-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="26ec6-146">Version du kit de développement logiciel (SDK) du format Windows Media requis par votre application.</span><span class="sxs-lookup"><span data-stu-id="26ec6-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="26ec6-147">Les trois exemples de valeurs de registre suivants montrent comment configurer les valeurs de votre application :</span><span class="sxs-lookup"><span data-stu-id="26ec6-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="26ec6-148">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ MediaPlayer \\ programme d’installation \\ DependentRefCounts \\ , « southridgevideo », « lecteur vidéo Southridge »</span><span class="sxs-lookup"><span data-stu-id="26ec6-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="26ec6-149">HKEY \_ classes \_ root \\ Software racine \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Descriptor, « southridgevideo », « Southridge Video Player utilise le kit de développement logiciel (SDK) Windows Media format pour lire des fichiers vidéo. »</span><span class="sxs-lookup"><span data-stu-id="26ec6-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="26ec6-150">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ MediaPlayer \\ programme d’installation \\ DependentRefCounts \\ , « southridgevideo », « 9.0.0.2600 »</span><span class="sxs-lookup"><span data-stu-id="26ec6-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="26ec6-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26ec6-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ec6-152">**Paramètres du Registre**</span><span class="sxs-lookup"><span data-stu-id="26ec6-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




