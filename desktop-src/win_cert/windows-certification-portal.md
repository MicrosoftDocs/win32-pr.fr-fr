---
title: Certifier votre application de bureau
description: Suivez ces étapes pour obtenir votre application de bureau certifiée pour Windows 7, Windows 8, Windows 8.1 et Windows 10. Si vous souhaitez convertir votre application de bureau pour qu’elle soit compatible avec le plateforme Windows universelle et le Windows Store, vous utiliserez le pont de bureau Windows. dans ce cas, vous devez suivre les conseils sur le pont Desktop pour les étapes de certification. Si vous développez et certifiez une application UWP à partir du début, consultez conseils pour la certification des applications Windows dans UWP pour plus d’informations sur la certification.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734557"
---
# <a name="certify-your-desktop-application"></a><span data-ttu-id="b2a3a-103">Certifier votre application de bureau</span><span class="sxs-lookup"><span data-stu-id="b2a3a-103">Certify your desktop application</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2a3a-104">La certification pour les applications de bureau Win32 est [déconseillée](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span><span class="sxs-lookup"><span data-stu-id="b2a3a-104">Certification for Win32 desktop apps is [deprecated](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span></span> <span data-ttu-id="b2a3a-105">À la place, [envoyez les fichiers ici](https://www.microsoft.com/wdsi/filesubmission/).</span><span class="sxs-lookup"><span data-stu-id="b2a3a-105">Instead, [submit files here](https://www.microsoft.com/wdsi/filesubmission/).</span></span>

<span data-ttu-id="b2a3a-106">Suivez ces étapes pour obtenir votre application de bureau certifiée pour Windows 7, Windows 8, Windows 8.1 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-106">Follow these steps to get your desktop app certified for Windows 7, Windows 8, Windows 8.1, and Windows 10.</span></span>

<span data-ttu-id="b2a3a-107">Si vous souhaitez convertir votre application de bureau pour qu’elle soit compatible avec le plateforme Windows universelle et le Windows Store, vous utiliserez le [pont de bureau Windows](https://developer.microsoft.com/windows/bridges/desktop). dans ce cas, vous devez suivre les conseils relatifs au [pont de bureau](/windows/uwp/porting/desktop-to-uwp-root) pour les étapes de certification.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-107">If you wish to convert your desktop app to be compatible with the Universal Windows Platform and Windows Store, you will use the [Windows Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop), in which case you should follow the [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) guidance for certification steps.</span></span>

<span data-ttu-id="b2a3a-108">Si vous développez et certifiez une application UWP à partir du début, consultez [conseils pour la certification des applications Windows dans UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) pour plus d’informations sur la certification.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-108">If you are developing and certifying a UWP app from the start, see [Guidance for Windows App Certification in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) for info on certification.</span></span>

## <a name="step-1-prepare-for-certification"></a><span data-ttu-id="b2a3a-109">Étape 1 : préparer la certification</span><span class="sxs-lookup"><span data-stu-id="b2a3a-109">Step 1: Prepare for certification</span></span>



| <span data-ttu-id="b2a3a-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b2a3a-110">Topic</span></span>                                                                                       | <span data-ttu-id="b2a3a-111">Description</span><span class="sxs-lookup"><span data-stu-id="b2a3a-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2a3a-112">Quels sont les avantages ?</span><span class="sxs-lookup"><span data-stu-id="b2a3a-112">What are the benefits?</span></span>](what-are-the-benefits-.md)<br/>                             | <span data-ttu-id="b2a3a-113">La certification de votre application de bureau offre plusieurs avantages à vous et à vos clients.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-113">Certifying your desktop app provides several benefits for you and your customers.</span></span>              |
| [<span data-ttu-id="b2a3a-114">Lire les spécifications</span><span class="sxs-lookup"><span data-stu-id="b2a3a-114">Read the requirements</span></span>](certification-requirements-for-windows-desktop-apps.md)<br/> | <span data-ttu-id="b2a3a-115">Passez en revue les conditions techniques et les qualifications d’éligibilité qu’une application de bureau doit respecter.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-115">Review the technical requirements and eligibility qualifications that a desktop app must meet.</span></span> |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a><span data-ttu-id="b2a3a-116">Étape 2 : tester votre application avec le kit de certification des applications Windows</span><span class="sxs-lookup"><span data-stu-id="b2a3a-116">Step 2: Test your app with the Windows App Certification Kit</span></span>



| <span data-ttu-id="b2a3a-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b2a3a-117">Topic</span></span>                                                          | <span data-ttu-id="b2a3a-118">Description</span><span class="sxs-lookup"><span data-stu-id="b2a3a-118">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2a3a-119">Procurez-vous le kit</span><span class="sxs-lookup"><span data-stu-id="b2a3a-119">Get the Kit</span></span>](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | <span data-ttu-id="b2a3a-120">Pour certifier votre application, vous devez installer et exécuter le kit de certification des applications Windows (inclus dans le SDK Windows).</span><span class="sxs-lookup"><span data-stu-id="b2a3a-120">To certify your app, you have to install and run the Windows App Certification Kit (included in the Windows SDK).</span></span>                                                                     |
| [<span data-ttu-id="b2a3a-121">Utilisation du kit</span><span class="sxs-lookup"><span data-stu-id="b2a3a-121">Using the Kit</span></span>](using-the-windows-app-certification-kit.md)   | <span data-ttu-id="b2a3a-122">Avant de pouvoir envoyer votre application, vous devez la tester à des fins de préparation.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-122">Before you can submit your app, you must test it for readiness.</span></span> <span data-ttu-id="b2a3a-123">Vous pouvez également télécharger une copie du livre [blanc](https://www.microsoft.com/download/details.aspx?id=27414)sur la certification de l’application.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-123">You can also download a copy of the [app certification white paper](https://www.microsoft.com/download/details.aspx?id=27414).</span></span> |
| [<span data-ttu-id="b2a3a-124">Examiner les détails du test</span><span class="sxs-lookup"><span data-stu-id="b2a3a-124">Review test details</span></span>](windows-app-certification-kit-tests.md) | <span data-ttu-id="b2a3a-125">Obtenir la liste des tests que votre application doit passer pour bénéficier d’une compatibilité avec le système d’exploitation Windows le plus récent.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-125">Get the list of the tests your app needs to pass to qualify for compatibility with the latest Windows operating system.</span></span>                                                               |



 

<span data-ttu-id="b2a3a-126">Remarque : les pilotes de filtre doivent également passer le [Kit de certification matérielle](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span><span class="sxs-lookup"><span data-stu-id="b2a3a-126">Note: Filter drivers must also pass the [Hardware Certification Kit](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span></span> <span data-ttu-id="b2a3a-127">(Voir [conditions de certification pour les applications de bureau Windows, section 6,2](certification-requirements-for-windows-desktop-apps.md).)</span><span class="sxs-lookup"><span data-stu-id="b2a3a-127">(See [Certification requirements for Windows desktop apps, section 6.2](certification-requirements-for-windows-desktop-apps.md).)</span></span>

## <a name="step-3-use-the-windows-certification-dashboard"></a><span data-ttu-id="b2a3a-128">Étape 3 : utiliser le tableau de bord de certification Windows</span><span class="sxs-lookup"><span data-stu-id="b2a3a-128">Step 3: Use the Windows Certification Dashboard</span></span>

<span data-ttu-id="b2a3a-129">Pour soumettre votre application à des fins de certification, vous devez vous connecter ou inscrire un compte d’entreprise dans le [tableau de bord de certification Windows](/previous-versions/hh833792(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="b2a3a-129">To submit your app for certification, you'll need to log in or register a company account on the [Windows Certification Dashboard](/previous-versions/hh833792(v=msdn.10)).</span></span> <span data-ttu-id="b2a3a-130">Une fois que vous avez fait, non seulement vous serez en mesure d’obtenir la certification de votre application, mais vous aurez également accès à des outils pour examiner et gérer votre application à toutes les étapes du processus.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-130">Once you do, not only will you be able to get your app certified, but you'll also gain access to tools to review and manage your app at all stages of the process.</span></span>



| <span data-ttu-id="b2a3a-131">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b2a3a-131">Topic</span></span>                                                                                                                   | <span data-ttu-id="b2a3a-132">Description</span><span class="sxs-lookup"><span data-stu-id="b2a3a-132">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2a3a-133">Configurer votre compte</span><span class="sxs-lookup"><span data-stu-id="b2a3a-133">Set up your account</span></span>](/windows-hardware/drivers/dashboard/)                 | <span data-ttu-id="b2a3a-134">Si votre entreprise n’est pas encore inscrite, vous devez l’inscrire via le tableau de bord de certification Windows.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-134">If your company isn't already registered, you must register it through the Windows Certification Dashboard.</span></span>                                        |
| [<span data-ttu-id="b2a3a-135">Obtenir un certificat de signature de code</span><span class="sxs-lookup"><span data-stu-id="b2a3a-135">Get a code signing certificate</span></span>](/windows-hardware/drivers/dashboard/)      | <span data-ttu-id="b2a3a-136">Avant de pouvoir établir un compte de tableau de bord de certification Windows, vous devez obtenir un certificat de signature de code pour sécuriser vos informations numériques.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-136">Before you can establish a Windows Certification Dashboard account, you need to get a code signing certificate to secure your digital information.</span></span> |
| [<span data-ttu-id="b2a3a-137">Tester localement et charger les résultats</span><span class="sxs-lookup"><span data-stu-id="b2a3a-137">Test locally and upload the results</span></span>](/windows-hardware/drivers/dashboard/) | <span data-ttu-id="b2a3a-138">Une fois que vous avez exécuté les tests du kit de certification des applications Windows, téléchargez les résultats dans le tableau de bord de certification Windows.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-138">After your run the Windows App Certification Kit tests, upload the results to the Windows Certification Dashboard.</span></span>                                 |
| [<span data-ttu-id="b2a3a-139">Gérer votre soumission</span><span class="sxs-lookup"><span data-stu-id="b2a3a-139">Manage your submission</span></span>](/windows-hardware/drivers/dashboard/)              | <span data-ttu-id="b2a3a-140">Une fois que vous avez envoyé votre application pour certification, vous pouvez passer en revue votre soumission via le tableau de bord de certification Windows.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-140">After you submit your app for certification, you can review your submission through the Windows Certification Dashboard.</span></span>                           |



 

## <a name="step-4-promote-your-desktop-app"></a><span data-ttu-id="b2a3a-141">Étape 4 : promouvoir votre application de bureau</span><span class="sxs-lookup"><span data-stu-id="b2a3a-141">Step 4: Promote your desktop app</span></span>



| <span data-ttu-id="b2a3a-142">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b2a3a-142">Topic</span></span>                                                                      | <span data-ttu-id="b2a3a-143">Description</span><span class="sxs-lookup"><span data-stu-id="b2a3a-143">Description</span></span>                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2a3a-144">Vérifier la compatibilité des applications</span><span class="sxs-lookup"><span data-stu-id="b2a3a-144">Check app compatibility</span></span>](/windows/compatibility/windows-8-1-introduction) | <span data-ttu-id="b2a3a-145">Si vous générez une application pour Windows 8.1, examinez les problèmes de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-145">If you are building an app for Windows 8.1, investigate compatibility concerns.</span></span>                                           |
| [<span data-ttu-id="b2a3a-146">Utiliser le logo avec votre application</span><span class="sxs-lookup"><span data-stu-id="b2a3a-146">Use the logo with your app</span></span>](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | <span data-ttu-id="b2a3a-147">Affichez le logo sur l’emballage, sur les publicités et d’autres documents promotionnels conformément aux instructions.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-147">Display the logo on packaging and in ads and other promotional materials according to the guidelines.</span></span> <span data-ttu-id="b2a3a-148">Pour Windows 7 uniquement.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-148">For Windows 7 only.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b2a3a-149">Voir aussi :</span><span class="sxs-lookup"><span data-stu-id="b2a3a-149">See also:</span></span>

<span data-ttu-id="b2a3a-150">[Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility)sur la compatibilité des applications : recherchez de l’aide auprès de la communauté sur la compatibilité et la certification du logo.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-150">[App compatibility forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): Find support from the community about compatibility and logo certification.</span></span>

<span data-ttu-id="b2a3a-151">[SDK Windows blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Découvrez les conseils et les actualités relatifs à la certification des applications.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-151">[Windows SDK blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Find tips and news related to app certification.</span></span>

<span data-ttu-id="b2a3a-152">[Forum Windows Server]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): visitez le Forum de certification pour obtenir des réponses.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-152">[Windows Server forum]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): Visit the Certification forum to get answers.</span></span>

<span data-ttu-id="b2a3a-153">Guide de [compatibilité](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): obtenir des informations sur les nouveautés ou les modifications apportées à la dernière version de Windows.</span><span class="sxs-lookup"><span data-stu-id="b2a3a-153">[Compatibility cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Get info about what's new or changed in the latest version of Windows.</span></span>

 

