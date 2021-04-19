---
title: Connexion Bureau à distance par le Web
description: Connexion Bureau à distance par le Web est une application Web composée d’un contrôle ActiveX et d’un exemple de page de connexion.
ms.assetid: f9d252b0-205a-47df-9eca-d5744c09e079
ms.tgt_platform: multiple
keywords:
- Connexion Bureau à distance par le Web Services Bureau à distance
- Services Bureau à distance protocole RDP (Remote Desktop Protocol) (RDP), Connexion Bureau à distance par le Web vue d’ensemble
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bb1e8f562e3e5c47c6050f550fe3c7090446be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511499"
---
# <a name="remote-desktop-web-connection"></a><span data-ttu-id="4511f-105">Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="4511f-105">Remote Desktop Web Connection</span></span>

<span data-ttu-id="4511f-106">Connexion Bureau à distance par le Web est une application Web composée d’un contrôle ActiveX et d’un exemple de page de connexion.</span><span class="sxs-lookup"><span data-stu-id="4511f-106">Remote Desktop Web Connection is a web application consisting of an ActiveX control and a sample connection page.</span></span> <span data-ttu-id="4511f-107">Lorsque vous déployez des Connexion Bureau à distance par le Web sur un serveur Web, vous pouvez fournir une connectivité client aux serveurs Bureau à distance hôte de session (hôte de session Bureau à distance) et à d’autres ordinateurs à l’aide d’Internet Explorer et de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4511f-107">When you deploy Remote Desktop Web Connection on a web server, you can provide client connectivity to Remote Desktop Session Host (RD Session Host) servers and other computers using Internet Explorer and TCP/IP.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4511f-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4511f-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4511f-109">Configuration requise pour Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="4511f-109">Requirements for Remote Desktop Web Connection</span></span>](requirements-for-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="4511f-110">Répertorie la configuration requise pour un Connexion Bureau à distance par le Web.</span><span class="sxs-lookup"><span data-stu-id="4511f-110">Lists the requirements for a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="4511f-111">Canaux virtuels scriptables</span><span class="sxs-lookup"><span data-stu-id="4511f-111">Scriptable virtual channels</span></span>](scriptable-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="4511f-112">Décrit les modifications apportées au modèle de programmation pour l’implémentation d’applications de canal virtuel fournies par les services Terminal Server client avancé (TSAC).</span><span class="sxs-lookup"><span data-stu-id="4511f-112">Describes changes to the programming model for implementing virtual channel applications that are provided by the Terminal Services Advanced Client (TSAC).</span></span>

</dd> </dl>

<span data-ttu-id="4511f-113">La documentation de référence de Connexion Bureau à distance par le Web est incluse dans la section [référence de connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="4511f-113">The reference material for Remote Desktop Web Connection is included in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) section.</span></span>

<span data-ttu-id="4511f-114">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4511f-114">For more information, see these topics:</span></span>

-   [<span data-ttu-id="4511f-115">Implémentation de canaux virtuels scriptables à l’aide de Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="4511f-115">Implementing Scriptable Virtual Channels Using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
-   [<span data-ttu-id="4511f-116">Incorporation du contrôle Bureau à distance ActiveX dans une page Web</span><span class="sxs-lookup"><span data-stu-id="4511f-116">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
-   <span data-ttu-id="4511f-117">[Téléchargement et utilisation du contrôle ActiveX Bureau à distance](/previous-versions//aa380808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4511f-117">[Downloading and Using the Remote Desktop ActiveX Control](/previous-versions//aa380808(v=vs.85))</span></span>
-   [<span data-ttu-id="4511f-118">Utilisation du contrôle ActiveX Bureau à distance avec des canaux virtuels</span><span class="sxs-lookup"><span data-stu-id="4511f-118">Using the Remote Desktop ActiveX Control with Virtual Channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
-   [<span data-ttu-id="4511f-119">Fournir la sécurité du client RDP</span><span class="sxs-lookup"><span data-stu-id="4511f-119">Providing for RDP Client Security</span></span>](providing-for-rdp-client-security.md)
-   [<span data-ttu-id="4511f-120">Désactivation des fonctionnalités de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="4511f-120">Disabling Remote Desktop Services Features</span></span>](disabling-terminal-services-features.md)

## <a name="installing-remote-desktop-web-connection"></a><span data-ttu-id="4511f-121">Installation de Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="4511f-121">Installing Remote Desktop Web Connection</span></span>

<span data-ttu-id="4511f-122">La procédure suivante permet d’installer le contrôle ActiveX Bureau à distance et l’exemple de page Web dans le répertoire% SystemRoot% \\ Web \\ TSWeb.</span><span class="sxs-lookup"><span data-stu-id="4511f-122">The following steps install the Remote Desktop ActiveX control and sample webpage to the %systemroot%\\Web\\Tsweb directory.</span></span> <span data-ttu-id="4511f-123">Ils partagent la page Web dans le répertoire TSWeb sur votre serveur, par exemple, sur https://*MyServer*/TSWeb.</span><span class="sxs-lookup"><span data-stu-id="4511f-123">They share the webpage in the Tsweb directory on your server, for example, at https://*MyServer*/tsweb.</span></span> <span data-ttu-id="4511f-124">Le contrôle (msrdp. ocx) et le code Connexion Bureau à distance par le Web se trouvent dans Msrdp.cab.</span><span class="sxs-lookup"><span data-stu-id="4511f-124">The control (Msrdp.ocx) and the Remote Desktop Web Connection code are located in Msrdp.cab.</span></span>

<span data-ttu-id="4511f-125">**Pour installer Connexion Bureau à distance par le Web**</span><span class="sxs-lookup"><span data-stu-id="4511f-125">**To install Remote Desktop Web Connection**</span></span>

1.  <span data-ttu-id="4511f-126">Dans l’élément Ajout/suppression de programmes du panneau de configuration, sous ajouter/supprimer des composants Windows, installez Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="4511f-126">In the Add/Remove Programs item in Control Panel, under Add/Remove Windows Components, install Microsoft Internet Information Services (IIS).</span></span>
2.  <span data-ttu-id="4511f-127">Installez le sous-composant World Wide Web service d’IIS.</span><span class="sxs-lookup"><span data-stu-id="4511f-127">Install the World Wide Web Service subcomponent of IIS.</span></span>
3.  <span data-ttu-id="4511f-128">Installez le sous-composant Connexion Bureau à distance par le Web du service World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="4511f-128">Install the Remote Desktop Web Connection subcomponent of World Wide Web Service.</span></span>

<span data-ttu-id="4511f-129">Pour obtenir une description de la page Web qui est incluse dans l’installation de Connexion Bureau à distance par le Web, consultez [exemple de page Web inclus avec le contrôle ActiveX Bureau à distance](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span><span class="sxs-lookup"><span data-stu-id="4511f-129">For a description of the webpage that is included with the installation of Remote Desktop Web Connection, see [Sample Webpage Included with the Remote Desktop ActiveX Control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 