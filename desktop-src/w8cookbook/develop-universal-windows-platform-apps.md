---
title: Développer des applications plateforme Windows universelle (UWP)
description: Développer des applications plateforme Windows universelle (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "106538993"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a><span data-ttu-id="f98b1-103">Développer des applications plateforme Windows universelle (UWP)</span><span class="sxs-lookup"><span data-stu-id="f98b1-103">Develop Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="f98b1-104">Nous encourageons tous les éditeurs de logiciels indépendants (ISV) de l’application de bureau (Win32) à mettre vos applications de bureau à la [plateforme Windows universelle (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) via le pont de bureau.</span><span class="sxs-lookup"><span data-stu-id="f98b1-104">We encourage all desktop (Win32) app ISVs to bring your desktop apps to the [Universal Windows Platform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) via the Desktop Bridge.</span></span> <span data-ttu-id="f98b1-105">Comme les applications UWP sont également prises en charge dans le [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), il vous est plus facile de mettre à jour automatiquement les applications de vos utilisateurs vers une version cohérente, ce qui réduit vos coûts de support technique.</span><span class="sxs-lookup"><span data-stu-id="f98b1-105">UWP apps are also supported in the [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), so it’s easier for you to update your users to a consistent version automatically, lowering your support costs.</span></span>

<span data-ttu-id="f98b1-106">Si vos applications de bureau ne peuvent pas être converties à l’aide du pont Desktop Bridge, nous vous recommandons vivement d’utiliser un programme d’installation qui suit les meilleures pratiques et de vérifier que cela est entièrement testé.</span><span class="sxs-lookup"><span data-stu-id="f98b1-106">If your desktop apps cannot be converted using the Desktop Bridge, we highly recommend that you use an installer that follows best practices, and ensure this is fully tested.</span></span> <span data-ttu-id="f98b1-107">Un programme d’installation est la première expérience de votre utilisateur ou de votre client avec votre application.</span><span class="sxs-lookup"><span data-stu-id="f98b1-107">An installer is your user or customer's first experience with your app.</span></span> <span data-ttu-id="f98b1-108">Il arrive trop souvent qu’il ne fonctionne pas correctement ou qu’il n’a pas été complètement testé pour tous les scénarios.</span><span class="sxs-lookup"><span data-stu-id="f98b1-108">All too often, this doesn’t work well or it hasn’t been fully tested for all scenarios.</span></span> <span data-ttu-id="f98b1-109">Le [Kit de certification des applications Windows](https://dev.windows.com/develop/app-certification-kit) peut vous aider à tester l’installation et la désinstallation de votre application Win32 et vous aider à identifier l’utilisation des API non documentées, ainsi que d’autres problèmes de base liés aux performances avant les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f98b1-109">The [Windows App Certification Kit](https://dev.windows.com/develop/app-certification-kit) can help you test install and uninstall of your Win32 app and help you identify use of undocumented APIs, as well as other basic performance-related best-practice issues before your users do.</span></span>

## <a name="best-practices"></a><span data-ttu-id="f98b1-110">Meilleure pratique :</span><span class="sxs-lookup"><span data-stu-id="f98b1-110">Best practices:</span></span>

-   <span data-ttu-id="f98b1-111">Utilisez des programmes d’installation qui fonctionnent à la fois pour les versions 32 bits et 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="f98b1-111">Use installers that work for both 32-bit and 64-bit versions of Windows.</span></span>
-   <span data-ttu-id="f98b1-112">Concevez vos programmes d’installation pour qu’ils fonctionnent dans plusieurs scénarios (niveau de l’utilisateur ou de l’ordinateur).</span><span class="sxs-lookup"><span data-stu-id="f98b1-112">Design your installers to run on multiple scenarios (user or machine level).</span></span>
-   <span data-ttu-id="f98b1-113">Conservez tous les composants redistribuables de Windows dans le package d’origine. Si vous réorganisez le package de ces composants, il se peut que le programme d’installation ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="f98b1-113">Keep all Windows redistributables in the original packaging – if you repackage these, it’s possible that this will break the installer.</span></span>
-   <span data-ttu-id="f98b1-114">Planifiez le temps de développement de vos programmes d’installation ; ils sont souvent négligés en tant que livrables au cours du cycle de développement logiciel.</span><span class="sxs-lookup"><span data-stu-id="f98b1-114">Schedule development time for your installers—these are often overlooked as a deliverable during the software development lifecycle.</span></span>

 

 




