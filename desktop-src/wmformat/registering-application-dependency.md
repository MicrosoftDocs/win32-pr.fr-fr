---
title: Inscription de la dépendance d’application (SDK Windows Media format 11)
description: Inscription de la dépendance d’application
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, inscrire des dépendances d’application
- inscription des dépendances d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032166"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="510c9-105">Inscription de la dépendance d’application (SDK Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="510c9-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="510c9-106">Les applications qui utilisent des API fournies par le kit de développement logiciel (SDK) Windows Media format ou le kit de développement logiciel (SDK) Windows Media Player dépendent des composants d’exécution de ces technologies.</span><span class="sxs-lookup"><span data-stu-id="510c9-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="510c9-107">Vous pouvez inscrire votre application comme étant dépendante de ces composants dans le cadre de la configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="510c9-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="510c9-108">Lorsque vous inscrivez votre application, vous pouvez choisir l’un des deux niveaux de dépendance : blocage ou dépendant.</span><span class="sxs-lookup"><span data-stu-id="510c9-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="510c9-109">Quand une ou plusieurs applications sont inscrites avec une dépendance de blocage sur l’un des composants d’exécution, le composant est bloqué d’une restauration vers une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="510c9-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="510c9-110">Les applications dépendantes qui ne sont pas inscrites comme bloquantes ne bloquent pas la restauration.</span><span class="sxs-lookup"><span data-stu-id="510c9-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="510c9-111">Au lieu de cela, avant d’effectuer la restauration, l’utilisateur est invité à entrer un message indiquant que les applications sont dépendantes du composant.</span><span class="sxs-lookup"><span data-stu-id="510c9-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="510c9-112">Pour inscrire votre application, vous devez définir une valeur dans le Registre qui identifie votre application.</span><span class="sxs-lookup"><span data-stu-id="510c9-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="510c9-113">La valeur de Registre à définir dépend du composant dont dépend votre application.</span><span class="sxs-lookup"><span data-stu-id="510c9-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="510c9-114">Vous pouvez également définir deux valeurs supplémentaires par dépendance pour fournir des informations supplémentaires sur votre application.</span><span class="sxs-lookup"><span data-stu-id="510c9-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="510c9-115">Les valeurs de Registre suivantes sont utilisées pour inscrire la dépendance au runtime du SDK Windows Media Format :</span><span class="sxs-lookup"><span data-stu-id="510c9-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="510c9-116">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ application, «*application*»,*« \_ chaîne d’application*»</span><span class="sxs-lookup"><span data-stu-id="510c9-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="510c9-117">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ - \\ *\_* \\ descripteur de type de référence, "*application*", "*\_ descripteur de référence*"</span><span class="sxs-lookup"><span data-stu-id="510c9-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="510c9-118">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ installation \\ *\_ type de référence* \\ version,*application*, «*\_ version WMF*»</span><span class="sxs-lookup"><span data-stu-id="510c9-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="510c9-119">La valeur de Registre suivante est utilisée pour inscrire la dépendance au runtime du kit de développement logiciel (SDK) du lecteur Windows Media :</span><span class="sxs-lookup"><span data-stu-id="510c9-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="510c9-120">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ MediaPlayer \\ installation \\ *\_ type référence* \\ application, «*application*», «*\_ chaîne d’application*»</span><span class="sxs-lookup"><span data-stu-id="510c9-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="510c9-121">HKEY \_ classes \_ root \\ Software racine \\ Microsoft \\ MediaPlayer \\ programme d’installation \\ descripteur de *\_ type REF* \\ , "*app*", "*Ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="510c9-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="510c9-122">HKEY \_ classes \_ root \\ Software racine \\ Microsoft \\ MediaPlayer \\ Setup \\ *\_ type REF* \\ , "*app*", "*WMP \_ version*"</span><span class="sxs-lookup"><span data-stu-id="510c9-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="510c9-123">Les variables suivantes sont utilisées dans les valeurs de Registre répertoriées ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="510c9-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="510c9-124">*TYPE de référence \_*</span><span class="sxs-lookup"><span data-stu-id="510c9-124">*REF\_TYPE*</span></span>

<span data-ttu-id="510c9-125">Remplacez par BlockingRefCounts pour le blocage de la dépendance ou par DependentRefCounts pour une dépendance non bloquante.</span><span class="sxs-lookup"><span data-stu-id="510c9-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="510c9-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="510c9-126">*APP*</span></span>

<span data-ttu-id="510c9-127">Nom ou descripteur abrégé de votre application.</span><span class="sxs-lookup"><span data-stu-id="510c9-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="510c9-128">Cette chaîne ne sera pas utilisée dans les messages affichés pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="510c9-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="510c9-129">Cette valeur est l’identificateur utilisé dans les trois valeurs de Registre associées à chacun des composants Runtime.</span><span class="sxs-lookup"><span data-stu-id="510c9-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="510c9-130">*chaîne d’application \_*</span><span class="sxs-lookup"><span data-stu-id="510c9-130">*APP\_STRING*</span></span>

<span data-ttu-id="510c9-131">Descripteur de votre application.</span><span class="sxs-lookup"><span data-stu-id="510c9-131">Descriptor of your application.</span></span> <span data-ttu-id="510c9-132">Cette chaîne peut être utilisée dans les messages affichés pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="510c9-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="510c9-133">*descripteur de référence \_*</span><span class="sxs-lookup"><span data-stu-id="510c9-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="510c9-134">Description de la façon dont votre application utilise le composant.</span><span class="sxs-lookup"><span data-stu-id="510c9-134">Description of how your application uses the component.</span></span> <span data-ttu-id="510c9-135">Cette valeur peut inclure un maximum de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="510c9-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="510c9-136">*VERSION de WMP \_*</span><span class="sxs-lookup"><span data-stu-id="510c9-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="510c9-137">Version du lecteur Windows Media requise par votre application.</span><span class="sxs-lookup"><span data-stu-id="510c9-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="510c9-138">*\_version WMF*</span><span class="sxs-lookup"><span data-stu-id="510c9-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="510c9-139">Version du kit de développement logiciel (SDK) du format Windows Media requis par votre application.</span><span class="sxs-lookup"><span data-stu-id="510c9-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="510c9-140">Les trois exemples de valeurs de registre suivants montrent comment configurer les valeurs de votre application :</span><span class="sxs-lookup"><span data-stu-id="510c9-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="510c9-141">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ Setup \\ DependentRefCounts \\ application, "southridgevideo", "Southridge Video Player"</span><span class="sxs-lookup"><span data-stu-id="510c9-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="510c9-142">HKEY \_ classes \_ racine \\ Software \\ Microsoft \\ windowsmedia \\ Setup \\ DependentRefCounts \\ Descriptor, "southridgevideo", "Southridge Video Player utilise le kit de développement logiciel (SDK) Windows Media format pour lire des fichiers vidéo."</span><span class="sxs-lookup"><span data-stu-id="510c9-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="510c9-143">HKEY \_ classes \_ racine \\ logiciel \\ Microsoft \\ windowsmedia \\ Setup \\ DependentRefCounts \\ version, "southridgevideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="510c9-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="510c9-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="510c9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="510c9-145">**Considérations relatives aux projets**</span><span class="sxs-lookup"><span data-stu-id="510c9-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




