---
description: Spécification du protocole d’authentification
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Spécification du protocole d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483424"
---
# <a name="specifying-the-authentication-protocol"></a><span data-ttu-id="88c5d-103">Spécification du protocole d’authentification</span><span class="sxs-lookup"><span data-stu-id="88c5d-103">Specifying the Authentication Protocol</span></span>

<span data-ttu-id="88c5d-104">En fonction des exigences de sécurité de votre site, vous pouvez exiger que le service des composants en file d’attente vérifie toujours l’identité d’un client, ne jamais vérifier l’identité d’un client, ou pour vérifier l’identité d’un client uniquement si le composant est configuré pour exiger une authentification même lorsqu’il n’est pas accessible par le biais d’une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="88c5d-104">Depending on the security requirements at your site, you can require the queued components service always to verify a client's identity, never to verify a client's identity, or to verify a client's identity only if the component is configured to require authentication even when not accessed through a queue.</span></span>

> [!Note]  
> <span data-ttu-id="88c5d-105">Pour pouvoir utiliser un composant mis en file d’attente en mode groupe de travail, le niveau d’authentification doit être défini sur aucun.</span><span class="sxs-lookup"><span data-stu-id="88c5d-105">In order to use a queued component in workgroup mode, the authentication level must be set to none.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="88c5d-106">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="88c5d-106">Component Services Administrative Tool</span></span>

<span data-ttu-id="88c5d-107">Pour spécifier le protocole d’authentification, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="88c5d-107">To specify the authentication protocol, use the following steps:</span></span>

1.  <span data-ttu-id="88c5d-108">Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="88c5d-108">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="88c5d-109">Cliquez avec le bouton droit sur l’application en file d’attente pour laquelle vous souhaitez spécifier le protocole d’authentification, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="88c5d-109">Right-click the queued application for which you want to specify the authentication protocol, and then click **Properties**.</span></span>

3.  <span data-ttu-id="88c5d-110">Sélectionnez l’onglet mise en **file d’attente** dans la boîte de dialogue Propriétés.</span><span class="sxs-lookup"><span data-stu-id="88c5d-110">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="88c5d-111">Sous **authentification des messages MSMQ**, sélectionnez la case d’option associée au protocole d’authentification que vous souhaitez implémenter.</span><span class="sxs-lookup"><span data-stu-id="88c5d-111">Under **MSMQ Message Authentication**, select the radio button associated with the authentication protocol you want to implement.</span></span>

5.  <span data-ttu-id="88c5d-112">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="88c5d-112">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="88c5d-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="88c5d-113">Visual Basic</span></span>

<span data-ttu-id="88c5d-114">Utilisez le paramètre *AuthLevel* lors de l’activation de l’application en file d’attente comme décrit dans la section [utilisation du moniker de la file d’attente](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="88c5d-114">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="cc"></a><span data-ttu-id="88c5d-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="88c5d-115">C/C++</span></span>

<span data-ttu-id="88c5d-116">Utilisez le paramètre *AuthLevel* lors de l’activation de l’application en file d’attente comme décrit dans la section [utilisation du moniker de la file d’attente](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="88c5d-116">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="88c5d-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88c5d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88c5d-118">Sécurité des composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="88c5d-118">Queued Components Security</span></span>](queued-components-security.md)
</dt> <dt>

[<span data-ttu-id="88c5d-119">Limitations de sécurité en mode groupe de travail</span><span class="sxs-lookup"><span data-stu-id="88c5d-119">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



