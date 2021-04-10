---
title: Individualisation DRM
description: Individualisation DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Media Format SDK, individualisation DRM
- gestion des droits numériques (DRM), individualisation
- DRM (gestion des droits numériques), individualisation
- individualisation de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309614"
---
# <a name="drm-individualization"></a><span data-ttu-id="fe479-107">Individualisation DRM</span><span class="sxs-lookup"><span data-stu-id="fe479-107">DRM Individualization</span></span>

<span data-ttu-id="fe479-108">Les propriétaires de contenu protégé peuvent obliger les utilisateurs à mettre à niveau certains des composants de gestion des droits numériques (DRM) inclus dans le kit de développement logiciel (SDK) du format Windows Media avant d’accéder à leur contenu.</span><span class="sxs-lookup"><span data-stu-id="fe479-108">Owners of protected content may require users to upgrade some of the digital rights management (DRM) components included in the Windows Media Format SDK before accessing their content.</span></span> <span data-ttu-id="fe479-109">Si un utilisateur accepte la mise à niveau, une version individualisée d’un fichier de sécurité (une unique sur son ordinateur) est téléchargée à partir d’un site Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe479-109">If a user accepts the upgrade, an individualized version of a security file (one unique to their computer) will be downloaded from a Microsoft Web site.</span></span> <span data-ttu-id="fe479-110">Si l’utilisateur refuse la mise à niveau, il ne pourra pas accéder au contenu. Toutefois, ils pourront toujours accéder au contenu non protégé et au contenu protégé qui ne nécessite pas la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="fe479-110">If the user declines the upgrade, they will not be able to access the content; however, they will still be able to access unprotected content and protected content that does not require the upgrade.</span></span> <span data-ttu-id="fe479-111">L’exécution d’une mise à niveau de sécurité permet d’augmenter le niveau de protection offert par DRM.</span><span class="sxs-lookup"><span data-stu-id="fe479-111">Performing a security upgrade helps increase the level of protection offered by DRM.</span></span>

<span data-ttu-id="fe479-112">L’individualisation peut être effectuée au moment de l’installation ou lorsqu’une application rencontre pour la première fois un fichier ASF protégé qui l’exige.</span><span class="sxs-lookup"><span data-stu-id="fe479-112">Individualization can be done either at setup time or when an application first encounters a protected ASF file that requires it.</span></span> <span data-ttu-id="fe479-113">Étant donné que ce processus modifie les composants système d’un utilisateur, l’application doit avertir l’utilisateur et obtenir son consentement avant d’effectuer la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="fe479-113">Because this process modifies a user's system components, the application must notify the user and obtain their informed consent before performing the upgrade.</span></span> <span data-ttu-id="fe479-114">Le lecteur Microsoft Windows Media, par exemple, affiche une boîte de dialogue avec le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="fe479-114">Microsoft Windows Media Player, for example, shows a dialog box with the following text:</span></span>

<span data-ttu-id="fe479-115">**Mise à niveau de sécurité requise**</span><span class="sxs-lookup"><span data-stu-id="fe479-115">**Security Upgrade Required**</span></span>

<span data-ttu-id="fe479-116">**Le propriétaire du contenu protégé auquel vous essayez d’accéder nécessite d’abord la mise à niveau de certains composants de gestion des droits numériques (DRM) Microsoft sur votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="fe479-116">**The owner of the protected content you are trying to access requires you to first upgrade some of the Microsoft digital rights management (DRM) components on your computer.**</span></span>

<span data-ttu-id="fe479-117">**Cliquez sur OK pour mettre à niveau vos composants DRM.**</span><span class="sxs-lookup"><span data-stu-id="fe479-117">**Click OK to upgrade your DRM components.**</span></span>

<span data-ttu-id="fe479-118">**Plus**</span><span class="sxs-lookup"><span data-stu-id="fe479-118">**Details:**</span></span>

<span data-ttu-id="fe479-119">**Lorsque vous cliquez sur OK, un identificateur unique et un fichier de sécurité DRM sont envoyés à un service Microsoft sur Internet. Le fichier est remplacé par une version personnalisée qui contient votre identificateur unique. Cela augmente le niveau de protection fourni par DRM.**</span><span class="sxs-lookup"><span data-stu-id="fe479-119">**When you click OK, a unique identifier and a DRM security file are sent to a Microsoft service on the Internet. The file is replaced with a customized version that contains your unique identifier. This increases the level of protection provided by DRM.**</span></span>

<span data-ttu-id="fe479-120">Toute application prenant en charge l’individualisation doit utiliser la même formulation ou une autre formulation similaire.</span><span class="sxs-lookup"><span data-stu-id="fe479-120">Any application that supports individualization should use the same or similar wording.</span></span> <span data-ttu-id="fe479-121">Pour plus d’informations sur la politique de confidentialité de Microsoft, consultez la section [déclaration de confidentialité](privacy-statement.md) de cette documentation.</span><span class="sxs-lookup"><span data-stu-id="fe479-121">For more information on Microsoft's Privacy Policy, see the [Privacy Statement](privacy-statement.md) section of this documentation.</span></span>

> [!Note]  
> <span data-ttu-id="fe479-122">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="fe479-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fe479-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe479-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe479-124">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="fe479-124">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="fe479-125">**Individualiser des applications DRM**</span><span class="sxs-lookup"><span data-stu-id="fe479-125">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> </dl>

 

 




