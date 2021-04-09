---
description: L’authentification est la preuve de votre identité.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Authentification pour les pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952638"
---
# <a name="authentication-for-web-pages"></a><span data-ttu-id="22606-103">Authentification pour les pages Web</span><span class="sxs-lookup"><span data-stu-id="22606-103">Authentication for web pages</span></span>

<span data-ttu-id="22606-104">L’authentification est la preuve de votre identité.</span><span class="sxs-lookup"><span data-stu-id="22606-104">Authentication is proving who you are.</span></span>

<span data-ttu-id="22606-105">**Objectif :** Pour que le Service Broker d’authentification Web apparaisse dans le cadre de votre application.</span><span class="sxs-lookup"><span data-stu-id="22606-105">**Objective:** To have the web authentication broker appear as part of your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="22606-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="22606-106">Prerequisites</span></span>

<span data-ttu-id="22606-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="22606-107">None</span></span>

<span data-ttu-id="22606-108">**Durée d’exécution :** 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="22606-108">**Time to complete:** 15 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="22606-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="22606-109">Instructions</span></span>

### <a name="1-getting-started"></a><span data-ttu-id="22606-110">1. Mise en route</span><span class="sxs-lookup"><span data-stu-id="22606-110">1. Getting started</span></span>

<span data-ttu-id="22606-111">Lancez le fichier d’installation pour installer un site Web Contoso dans Internet Information Services 8 sur l’ordinateur local afin d’héberger les fichiers HTML et CSS de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="22606-111">Launch the setup file to install a Contoso website in Internet Information Services 8 on the local machine to host the sample HTML and CSS files.</span></span>

1.  <span data-ttu-id="22606-112">Des exemples de fichiers HTML et CSS seront installés dans le répertoire Program Files de Microsoft \\ contoso.</span><span class="sxs-lookup"><span data-stu-id="22606-112">Sample HTML and CSS files will be installed to the program files directory under Microsoft\\Contoso.</span></span>
2.  <span data-ttu-id="22606-113">En outre, une application du Windows Store « Fabrikam social » sera déconditionnée sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="22606-113">In addition a "Fabrikam Social"Windows Store app will be unpackaged to the desktop.</span></span>

### <a name="2-getting-familiar"></a><span data-ttu-id="22606-114">2. Familiarisez-vous avec</span><span class="sxs-lookup"><span data-stu-id="22606-114">2. Getting familiar</span></span>

<span data-ttu-id="22606-115">Pour avoir une idée de ce à quoi ressemblent les exemples de pages dans le répartiteur d’authentification Web, ouvrez le fichier solution Fabrikam de Visual Studio 11 social dans le dossier « Fabrikam social » sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="22606-115">To get a feel for what the sample pages look like in the Web Authentication Broker, open the Fabrikam Social Visual Studio 11 solution file in the "Fabrikam Social" folder on the desktop.</span></span>

1.  <span data-ttu-id="22606-116">Exécutez l’application et appuyez sur « Démarrer » pour afficher les exemples de pages dans le répartiteur d’authentification Web.</span><span class="sxs-lookup"><span data-stu-id="22606-116">Run the application and hit "Launch" to bring up the sample pages in the Web Authentication Broker.</span></span>
2.  <span data-ttu-id="22606-117">L’application peut être redimensionnée d’un côté ou activée en partageant des données à l’application.</span><span class="sxs-lookup"><span data-stu-id="22606-117">The app can be resized to one side or activated by sharing some data to the application.</span></span>

### <a name="3-authentication"></a><span data-ttu-id="22606-118">3. Authentification</span><span class="sxs-lookup"><span data-stu-id="22606-118">3. Authentication</span></span>

<span data-ttu-id="22606-119">Lorsque l’API d’authentification Web est appelée par l’application sous-jacente pour se connecter au fournisseur, « contoso social », la page de connexion s’affiche.</span><span class="sxs-lookup"><span data-stu-id="22606-119">When the Web Auth API is invoked by the underlying app to connect to the provider, "Contoso Social", the login page is shown.</span></span> <span data-ttu-id="22606-120">Cette page est conçue pour offrir une expérience de connexion rapide et fluide.</span><span class="sxs-lookup"><span data-stu-id="22606-120">This page is designed to be best at a fast and fluid login experience.</span></span> <span data-ttu-id="22606-121">Il fournit également des points d’entrée pour d’autres actions courantes de l’utilisateur, telles que la récupération des informations de mot de passe, l’inscription à un compte et la lecture d’instructions sur la confidentialité et les conditions générales qui sont terminées dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="22606-121">It also provides entry points to some other common user actions such as retrieving password details, signing up for an account, and reading statements on privacy and terms and conditions that are completed in the browser.</span></span> ![page de connexion contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a><span data-ttu-id="22606-123">Résumé et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="22606-123">Summary and next steps</span></span>

<span data-ttu-id="22606-124">[Didacticiel Résumé pour l’authentification des pages Web](tutorial-for-authenticating-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="22606-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="22606-125">[Autorisation suivante pour les pages Web](authorization-for-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="22606-125">Next [Authorization for web pages](authorization-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="22606-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22606-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22606-127">Considérations sur le développement de pages web</span><span class="sxs-lookup"><span data-stu-id="22606-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="22606-128">Exemple d’application du SDK du Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="22606-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="22606-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="22606-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
