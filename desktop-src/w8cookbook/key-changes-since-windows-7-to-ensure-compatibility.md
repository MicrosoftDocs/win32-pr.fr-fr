---
title: Modifications clés depuis Windows 7 pour garantir la compatibilité
description: Modifications clés depuis Windows 7 pour garantir la compatibilité
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee24b18be55ff498d6c3870f77a32270df68284
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310849"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a><span data-ttu-id="8fca2-103">Modifications clés depuis Windows 7 pour garantir la compatibilité</span><span class="sxs-lookup"><span data-stu-id="8fca2-103">Key changes since Windows 7 to ensure compatibility</span></span>

<span data-ttu-id="8fca2-104">Nous comprenons que la compatibilité est importante pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="8fca2-104">We understand that compatibility matters to developers.</span></span> <span data-ttu-id="8fca2-105">Les éditeurs de logiciels indépendants et les développeurs veulent garantir que leurs applications s’exécuteront comme prévu sur toutes les versions prises en charge du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="8fca2-105">ISVs and developers want to ensure their apps will run as expected on all supported versions of the Windows OS.</span></span> <span data-ttu-id="8fca2-106">L’investissement des consommateurs et des entreprises est essentiel ici : ils veulent être sûrs que les applications qu’ils ont payées continueront de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="8fca2-106">Consumers and businesses have a key investment here—they want to ensure that the apps they have paid for will continue to work.</span></span> <span data-ttu-id="8fca2-107">Nous savons que la compatibilité est le principal critère motivant les décisions d’achat.</span><span class="sxs-lookup"><span data-stu-id="8fca2-107">We know that compatibility is the primary criteria for purchase decisions.</span></span> <span data-ttu-id="8fca2-108">Les applications bien écrites sur la base des meilleures pratiques aboutiront à une plus grande quantité d’évolution du code lors de la publication d’une nouvelle version de Windows et réduiront la fragmentation : ces applications ont un investissement d’ingénierie réduit pour la maintenance et un délai de mise sur le marché plus rapide.</span><span class="sxs-lookup"><span data-stu-id="8fca2-108">Apps that are well written based on best practices will lead to much less code churn when a new Windows version is released, and will reduce fragmentation—these apps have a reduced engineering investment to maintain, and a faster time to market.</span></span>

<span data-ttu-id="8fca2-109">À l’époque de Windows 7, la compatibilité était une approche extrêmement réactive.</span><span class="sxs-lookup"><span data-stu-id="8fca2-109">In the Windows 7 timeframe, compatibility was very much a reactive approach.</span></span> <span data-ttu-id="8fca2-110">Dans Windows 8, nous avons commencé à l’envisager différemment, en travaillant dans Windows pour nous assurer que la compatibilité tenait plus de la conception que d’un ajout ultérieur.</span><span class="sxs-lookup"><span data-stu-id="8fca2-110">In Windows 8, we started looking at this differently, working within Windows to ensure that compatibility was by design rather than an afterthought.</span></span> <span data-ttu-id="8fca2-111">Windows 10 est la version du système d’exploitation relevant de la conception la plus compatible à ce jour.</span><span class="sxs-lookup"><span data-stu-id="8fca2-111">Windows 10 is the most compatible-by-design version of the OS to date.</span></span> <span data-ttu-id="8fca2-112">Voici quelques moyens clés qui nous ont permis d’atteindre cet objectif :</span><span class="sxs-lookup"><span data-stu-id="8fca2-112">Here are some key ways we accomplished this:</span></span>

-   <span data-ttu-id="8fca2-113">Télémétrie de l’application : cela nous aide à comprendre la popularité de l’application dans l’écosystème Windows pour informer les tests de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="8fca2-113">App telemetry: this helps us understand app popularity in the Windows ecosystem to inform compatibility testing.</span></span>
-   <span data-ttu-id="8fca2-114">Partenariats ISV : travaillez directement avec des partenaires externes pour leur fournir des données et résoudre les problèmes rencontrés par nos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8fca2-114">ISV partnerships: work directly with external partners to provide them with data and help fix issues that our users experience.</span></span>
-   <span data-ttu-id="8fca2-115">Révision de conception, détection amont : partenaire avec des équipes de fonctionnalités pour réduire le nombre de modifications avec rupture dans Windows.</span><span class="sxs-lookup"><span data-stu-id="8fca2-115">Design reviews, upstream detection: partner with feature teams to reduce the number of breaking changes in Windows.</span></span> <span data-ttu-id="8fca2-116">La vérification de la compatibilité est l’une des étapes que doivent effectuer nos équipes chargées des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="8fca2-116">Compatibility review is a gate that our feature teams must pass.</span></span>
-   <span data-ttu-id="8fca2-117">Contrôle plus étroit des modifications d’API & communication améliorée</span><span class="sxs-lookup"><span data-stu-id="8fca2-117">Tighter control over API changes & improved communication</span></span>
-   <span data-ttu-id="8fca2-118">Boucle de vol et de commentaires : la population Windows Insider reçoit des builds en vol qui contribuent à améliorer notre capacité à trouver des problèmes de compatibilité avant la publication d’une version finale pour les clients.</span><span class="sxs-lookup"><span data-stu-id="8fca2-118">Flighting and feedback loop: The Windows Insider population receives flighted builds that help improve our ability to find compatibility issues before a final build is released to customers.</span></span> <span data-ttu-id="8fca2-119">Ce processus de feedback ne révèle pas seulement les bogues : il nous permet également de garantir que nous fournissons à nos clients les fonctionnalités qu’ils souhaitent.</span><span class="sxs-lookup"><span data-stu-id="8fca2-119">This feedback process not only exposes bugs, but ensures we are shipping features our users want.</span></span>

 

 




