---
title: Utilisation des listes de révocation
description: Utilisation des listes de révocation
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows Media Format SDK, listes de révocation
- ASF (Advanced Systems Format), listes de révocation
- ASF (format des systèmes avancés), listes de révocation
- listes de révocation
- gestion des droits numériques (DRM), listes de révocation
- DRM (gestion des droits numériques), listes de révocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507775"
---
# <a name="working-with-revocation-lists"></a><span data-ttu-id="4bc5f-109">Utilisation des listes de révocation</span><span class="sxs-lookup"><span data-stu-id="4bc5f-109">Working with Revocation Lists</span></span>

<span data-ttu-id="4bc5f-110">Pour répondre aux violations de sécurité et garantir que les applications de lecteur connues pour être endommagées ou compromises ne peuvent pas lire ou utiliser des fichiers protégés, chaque licence émise contient une liste de révocation.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-110">To respond to security breaches and to ensure that player applications known to be broken or compromised cannot play or use protected files, each license that is issued contains a revocation list.</span></span> <span data-ttu-id="4bc5f-111">Une liste de révocation contient les certificats d’application de toutes les applications de lecteur connues pour être endommagées ou endommagées.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-111">A revocation list contains the application certificates of all those player applications known to be broken or corrupted.</span></span> <span data-ttu-id="4bc5f-112">Lors de la réception d’une nouvelle licence, le composant DRM de l’application du lecteur recherche une liste de révocation.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-112">When a new license is received, the DRM component of the player application checks for a revocation list.</span></span> <span data-ttu-id="4bc5f-113">Si une version plus récente que celle actuellement présente sur l’ordinateur est trouvée, la liste la plus récente est stockée.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-113">If one is found that is newer than the one currently on the computer, the newer list is stored.</span></span> <span data-ttu-id="4bc5f-114">La prochaine fois que le consommateur lit un fichier ASF protégé, le composant DRM compare l’application de lecteur à la liste de révocation.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-114">The next time the consumer plays a protected ASF file, the DRM component compares the player application to the revocation list.</span></span> <span data-ttu-id="4bc5f-115">Si l’application de lecteur est révoquée, le composant DRM envoie un message d’erreur à l’application.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-115">If the player application is revoked, the DRM component sends an error message to the application.</span></span>

<span data-ttu-id="4bc5f-116">Les applications de lecteur peuvent recevoir un message d’erreur de révocation dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="4bc5f-116">Player applications can receive a revocation error message in the following scenarios:</span></span>

-   <span data-ttu-id="4bc5f-117">Le message d’erreur est reçu après que l’application a appelé la méthode [**IWMDRMReader :: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) pour un fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-117">The error message is received after the application calls the [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) method for a protected file.</span></span> <span data-ttu-id="4bc5f-118">L’appel échoue avec le code **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ révoqué, qui est fourni à la fonction de rappel **OnStatus** avec l’état de la licence d' \_ acquisition WMT \_ .</span><span class="sxs-lookup"><span data-stu-id="4bc5f-118">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the **OnStatus** callback function with WMT\_ACQUIRE\_LICENSE status.</span></span> <span data-ttu-id="4bc5f-119">Si ce code **HRESULT** est ignoré, des erreurs continuent de se produire.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-119">If this **HRESULT** code is ignored, errors will continue to occur.</span></span>
-   <span data-ttu-id="4bc5f-120">Le message d’erreur est reçu lorsque l’application crée le lecteur compatible DRM et appelle la méthode [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) pour un fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-120">The error message is received when the application creates the DRM-enabled reader and calls the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method for a protected file.</span></span> <span data-ttu-id="4bc5f-121">L’appel échoue avec le code **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ révoqué, qui est fourni à la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) avec l' \_ état ouvert de WMT.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-121">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method with WMT\_OPENED status.</span></span> <span data-ttu-id="4bc5f-122">Quand une application de lecteur reçoit ce message d’erreur, l’application doit avertir les utilisateurs finaux et leur permettre de restaurer les fonctionnalités sur leur lecteur.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-122">When a player application receives this error message, the application should notify end users and provide a way for them to restore functionality to their player.</span></span> <span data-ttu-id="4bc5f-123">Par exemple, l’application peut ouvrir une URL où les utilisateurs finaux peuvent télécharger une mise à niveau pour l’application compromise.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-123">For example, the application can open a URL where end users can download an upgrade for the compromised application.</span></span>

<span data-ttu-id="4bc5f-124">**Remarque** DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="4bc5f-124">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bc5f-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4bc5f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bc5f-126">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-126">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="4bc5f-127">**Gestion des événements d’acquisition de licence**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-127">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> </dl>

 

 




