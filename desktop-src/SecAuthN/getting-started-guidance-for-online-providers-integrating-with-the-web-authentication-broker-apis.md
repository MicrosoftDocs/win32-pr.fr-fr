---
description: Instructions pour les développeurs Web et les fournisseurs en ligne pour créer des pages Web adaptées aux API du Service Broker d’authentification Web de Windows 8 pour les fonctionnalités d’authentification unique (SSO).
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: Guide de prise en main pour les fournisseurs en ligne intégrant les API du Service Broker d’authentification Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842f3c562d2ad288efaecec82f8da8ca771886a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867265"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="d13ea-103">Guide de prise en main pour les fournisseurs en ligne intégrant les API du Service Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="d13ea-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="d13ea-104">Cette section guide les développeurs Web et les fournisseurs en ligne pour la création de pages Web adaptées aux API du Service Broker d’authentification Web de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d13ea-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="d13ea-105">Il fournit des recommandations visuelles et interactives pour une expérience utilisateur de bout en bout de la page Web, ainsi que l’activation des fonctionnalités d’authentification unique (SSO).</span><span class="sxs-lookup"><span data-stu-id="d13ea-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d13ea-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d13ea-106">In this section</span></span>



| <span data-ttu-id="d13ea-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d13ea-107">Topic</span></span>                                                                                                     | <span data-ttu-id="d13ea-108">Description</span><span class="sxs-lookup"><span data-stu-id="d13ea-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d13ea-109">Considérations sur le développement de pages web</span><span class="sxs-lookup"><span data-stu-id="d13ea-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="d13ea-110">Le Service Broker d’authentification Web est basé sur les technologies qui alimentent Internet Explorer dans Windows.</span><span class="sxs-lookup"><span data-stu-id="d13ea-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="d13ea-111">Toutefois, en raison d’un objectif très spécial de ce composant, certaines fonctionnalités d’Internet Explorer ont été désactivées ou verrouillées à une configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="d13ea-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="d13ea-112">Guide pratique pour personnaliser les éléments de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d13ea-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="d13ea-113">Une page Web personnalise l’interface utilisateur avec le titre, l’icône et la couleur d’en-tête à l’aide des balises de métadonnées définies sur la page Web.</span><span class="sxs-lookup"><span data-stu-id="d13ea-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="d13ea-114">Didacticiel sur l’authentification des pages Web</span><span class="sxs-lookup"><span data-stu-id="d13ea-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="d13ea-115">Problèmes d’authentification web</span><span class="sxs-lookup"><span data-stu-id="d13ea-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="d13ea-116">Cette rubrique décrit des conseils de dépannage pour l’utilisation des API du Service Broker d’authentification Web pour vos pages Web.</span><span class="sxs-lookup"><span data-stu-id="d13ea-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="d13ea-117">Forum aux questions sur le Service Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="d13ea-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)<br/>                     | <span data-ttu-id="d13ea-118">Forum aux questions sur le Service Broker d’authentification Web.</span><span class="sxs-lookup"><span data-stu-id="d13ea-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="d13ea-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d13ea-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d13ea-120">[Vue d’ensemble du répartiteur d’authentification Web](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d13ea-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="d13ea-121">Exemple d’application du SDK du Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="d13ea-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="d13ea-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="d13ea-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

