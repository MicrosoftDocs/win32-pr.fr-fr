---
description: L’accès aux applications COM+ exposées en tant que services Web XML est contrôlé par le serveur Web IIS, qui traite les demandes entrantes.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Sécurisation des services Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544207"
---
# <a name="securing-xml-web-services"></a><span data-ttu-id="7996e-103">Sécurisation des services Web XML</span><span class="sxs-lookup"><span data-stu-id="7996e-103">Securing XML Web Services</span></span>

<span data-ttu-id="7996e-104">L’accès aux applications COM+ exposées en tant que services Web XML est contrôlé par le serveur Web IIS, qui traite les demandes entrantes.</span><span class="sxs-lookup"><span data-stu-id="7996e-104">Access to COM+ applications exposed as XML web services is controlled by the IIS web server, which processes the incoming requests.</span></span> <span data-ttu-id="7996e-105">Vous pouvez également configurer IIS pour exiger que les communications avec l’appelant s’effectuent sur un canal sécurisé établi à l’aide du protocole SSL (Secure Sockets Layer) (SSL).</span><span class="sxs-lookup"><span data-stu-id="7996e-105">You can also configure IIS to require the communications with the caller take place over a secure channel established using the Secure Sockets Layer (SSL) protocol.</span></span>

> [!Note]  
> <span data-ttu-id="7996e-106">Un service Web XML sécurisé ne prend pas en charge l’accès WKO via WSDL.</span><span class="sxs-lookup"><span data-stu-id="7996e-106">A secured XML web service does not support WKO access via WSDL.</span></span> <span data-ttu-id="7996e-107">Au lieu de cela, les clients qui ont installé la version de .NET Framework 1,1 peuvent l’appeler en mode CAO.</span><span class="sxs-lookup"><span data-stu-id="7996e-107">Instead, clients that have installed the .NET Framework version 1.1 can call it in CAO mode.</span></span> <span data-ttu-id="7996e-108">Si des clients tiers ont besoin d’accéder à votre service Web XML via WSDL, vous devez autoriser l’accès anonyme.</span><span class="sxs-lookup"><span data-stu-id="7996e-108">If third-party clients need to access your XML web service via WSDL, you must allow anonymous access.</span></span>

 

> [!Note]  
> <span data-ttu-id="7996e-109">Pour utiliser le protocole SSL afin d’établir un canal de communication sécurisé, vous devez obtenir et installer un certificat SSL.</span><span class="sxs-lookup"><span data-stu-id="7996e-109">To use the SSL protocol to establish a secure communication channel, you must obtain and install an SSL certificate.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="7996e-110">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="7996e-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="7996e-111">Pour sélectionner le mécanisme d’authentification d’un service Web XML, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7996e-111">To select the authentication mechanism for an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="7996e-112">Cliquez avec le bouton droit sur l’icône de **poste de travail** sur votre bureau, puis cliquez sur **gérer**.</span><span class="sxs-lookup"><span data-stu-id="7996e-112">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="7996e-113">Sous **services et applications** et **Internet Information Services**, recherchez l’icône correspondant au répertoire racine virtuel de votre service Web XML.</span><span class="sxs-lookup"><span data-stu-id="7996e-113">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="7996e-114">Cliquez avec le bouton droit sur l’icône du répertoire, puis choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="7996e-114">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="7996e-115">Sous l’onglet **sécurité de répertoire** de la boîte de dialogue Propriétés, recherchez **authentification et contrôle d’accès** , puis cliquez sur le bouton **modifier** correspondant.</span><span class="sxs-lookup"><span data-stu-id="7996e-115">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span>

4.  <span data-ttu-id="7996e-116">Dans la boîte de dialogue **méthodes d’authentification** , sous **accès authentifié**, utilisez les cases à cocher pour sélectionner les mécanismes d’authentification que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="7996e-116">In the **Authentication Methods** dialog box, under **Authenticated access**, use the check boxes to select the authentication mechanisms you wish to allow.</span></span> <span data-ttu-id="7996e-117">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7996e-117">Click **OK**.</span></span>

    > [!Note]  
    > <span data-ttu-id="7996e-118">Vous pouvez configurer IIS pour authentifier les appelants en utilisant l’une des options suivantes dans la boîte de dialogue **méthodes d’authentification** IIS : **authentification Windows intégrée**, **authentification Digest pour les serveurs de domaine Windows**, **authentification de base (mot de passe envoyé en texte clair)** ou **authentification .NET Passport**.</span><span class="sxs-lookup"><span data-stu-id="7996e-118">You can configure IIS to authenticate callers by using any of the following options on the IIS **Authentication Methods** dialog: **Integrated Windows authentication**, **Digest authentication for Windows domain servers**, **Basic authentication (password is sent in clear text)**, or **.NET Passport authentication**.</span></span> <span data-ttu-id="7996e-119">Vous pouvez également autoriser l’accès anonyme.</span><span class="sxs-lookup"><span data-stu-id="7996e-119">You can also allow anonymous access.</span></span>

     

5.  <span data-ttu-id="7996e-120">Dans la boîte de dialogue Propriétés, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7996e-120">In the properties dialog, click **OK**.</span></span>

<span data-ttu-id="7996e-121">Pour autoriser un accès anonyme non sécurisé à un service Web XML, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7996e-121">To allow nonsecure, anonymous access to an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="7996e-122">Cliquez avec le bouton droit sur l’icône de **poste de travail** sur votre bureau, puis cliquez sur **gérer**.</span><span class="sxs-lookup"><span data-stu-id="7996e-122">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="7996e-123">Sous **services et applications** et **Internet Information Services**, recherchez l’icône correspondant au répertoire racine virtuel de votre service Web XML.</span><span class="sxs-lookup"><span data-stu-id="7996e-123">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="7996e-124">Cliquez avec le bouton droit sur l’icône du répertoire, puis choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="7996e-124">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="7996e-125">Sous l’onglet **sécurité de répertoire** de la boîte de dialogue Propriétés, recherchez **authentification et contrôle d’accès**, puis cliquez sur le bouton **modifier** correspondant.</span><span class="sxs-lookup"><span data-stu-id="7996e-125">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="7996e-126">Activez la case à cocher **activer la connexion anonyme** .</span><span class="sxs-lookup"><span data-stu-id="7996e-126">Select the **Enable anonymous access** check box.</span></span> <span data-ttu-id="7996e-127">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7996e-127">Click **OK**.</span></span>

4.  <span data-ttu-id="7996e-128">Sous l’onglet **sécurité de répertoire** de la boîte de dialogue Propriétés, localisez **communications sécurisées** , puis cliquez sur le bouton **modifier** correspondant.</span><span class="sxs-lookup"><span data-stu-id="7996e-128">On the **Directory Security** tab of the properties dialog, locate **Secure communications** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="7996e-129">Désactivez la case à cocher **exiger un canal sécurisé (SSL)** .</span><span class="sxs-lookup"><span data-stu-id="7996e-129">Uncheck the **Require secure channel (SSL)** check box.</span></span> <span data-ttu-id="7996e-130">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7996e-130">Click **OK**.</span></span>

5.  <span data-ttu-id="7996e-131">Dans la boîte de dialogue Propriétés, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7996e-131">In the properties dialog, click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="7996e-132">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7996e-132">Visual Basic</span></span>

<span data-ttu-id="7996e-133">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="7996e-133">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="7996e-134">C/C++</span><span class="sxs-lookup"><span data-stu-id="7996e-134">C/C++</span></span>

<span data-ttu-id="7996e-135">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="7996e-135">Does not apply.</span></span>

## <a name="additional-security-considerations"></a><span data-ttu-id="7996e-136">Considérations supplémentaires sur la sécurité</span><span class="sxs-lookup"><span data-stu-id="7996e-136">Additional Security Considerations</span></span>

<span data-ttu-id="7996e-137">En exigeant un canal sécurisé, vous contribuez à protéger la confidentialité des données échangées en chiffrant les communications entre le client et votre service Web XML.</span><span class="sxs-lookup"><span data-stu-id="7996e-137">By requiring a secure channel, you help protect the confidentiality of the data exchanged by encrypting the communications between the client and your XML web service.</span></span> <span data-ttu-id="7996e-138">Si vous autorisez l’authentification à l’aide de mots de passe en texte clair, vous devez exiger un canal sécurisé afin d’éviter d’exposer les mots de passe sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="7996e-138">If you allow authentication using clear text passwords, you should require a secure channel in order to avoid exposing passwords on the network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7996e-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7996e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7996e-140">Accès aux services Web XML en mode CAO</span><span class="sxs-lookup"><span data-stu-id="7996e-140">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="7996e-141">Accès aux services Web XML en mode WKO</span><span class="sxs-lookup"><span data-stu-id="7996e-141">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="7996e-142">Considérations sur la sécurité du service SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="7996e-142">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="7996e-143">Création de services Web XML</span><span class="sxs-lookup"><span data-stu-id="7996e-143">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> </dl>

 

 



