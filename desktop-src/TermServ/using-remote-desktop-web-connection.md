---
title: Utilisation du contrôle ActiveX Bureau à distance
description: Comment vous pouvez utiliser le contrôle ActiveX Bureau à distance pour personnaliser l’expérience utilisateur Services Bureau à distance.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance à l’aide du contrôle ActiveX Bureau à distance
- Services Bureau à distance Connexion Bureau à distance par le Web, utilisation
- protocole RDP (Remote Desktop Protocol) Services Bureau à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511006"
---
# <a name="using-the-remote-desktop-activex-control"></a><span data-ttu-id="fb807-106">Utilisation du contrôle ActiveX Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="fb807-106">Using the Remote Desktop ActiveX control</span></span>

<span data-ttu-id="fb807-107">Les rubriques suivantes contiennent des informations sur la façon dont vous pouvez utiliser le contrôle ActiveX Bureau à distance pour personnaliser l’expérience utilisateur Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fb807-107">The following topics contain information about how you can use the Remote Desktop ActiveX control to customize the Remote Desktop Services user experience.</span></span>

<span data-ttu-id="fb807-108">Le contrôle ActiveX Bureau à distance est disponible sous les formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb807-108">The Remote Desktop ActiveX control is available in the following forms:</span></span>

-   <span data-ttu-id="fb807-109">**Le contrôle scriptable**: implémente des interfaces sécurisées pour l’écriture de scripts.</span><span class="sxs-lookup"><span data-stu-id="fb807-109">**The scriptable control**—implements interfaces that are safe for scripting.</span></span> <span data-ttu-id="fb807-110">Cette forme du contrôle peut être utilisée par les clients Web ou les hôtes de script (tels que VBScript).</span><span class="sxs-lookup"><span data-stu-id="fb807-110">This form of the control can be used by web clients or scripting (such as VBScript) hosts.</span></span>
-   <span data-ttu-id="fb807-111">**Le contrôle non scriptable**, offre des fonctionnalités supplémentaires qui ne sont pas sûres pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="fb807-111">**The nonscriptable control**—offers additional functionality that is not safe for scripting.</span></span> <span data-ttu-id="fb807-112">Cette forme du contrôle peut être utilisée à partir du code natif ou managé, mais ce formulaire ne peut pas être utilisé par les clients Web ou les hôtes de script uniquement.</span><span class="sxs-lookup"><span data-stu-id="fb807-112">This form of the control can be used from native or managed code, but this form cannot be used by web clients or scripting-only hosts.</span></span>

<span data-ttu-id="fb807-113">La liste suivante contient les **CLSID** des différents contrôles pour les différentes versions de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fb807-113">The following list contains the **CLSID** s for the different controls for different operating system versions.</span></span> <span data-ttu-id="fb807-114">Chacun des **CLSID** s est compatible avec les versions ultérieures du système.</span><span class="sxs-lookup"><span data-stu-id="fb807-114">Each of the **CLSID** s is compatible with later system versions.</span></span> <span data-ttu-id="fb807-115">Par exemple, le **CLSID** du contrôle scriptable sur Windows Vista fonctionnera sur les versions ultérieures du système, telles que Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb807-115">For example, the **CLSID** for the scriptable control on Windows Vista will work on later system versions, such as Windows 7.</span></span>



| <span data-ttu-id="fb807-116">Version du système</span><span class="sxs-lookup"><span data-stu-id="fb807-116">System version</span></span>                          | <span data-ttu-id="fb807-117">CLSID du contrôle scriptable</span><span class="sxs-lookup"><span data-stu-id="fb807-117">Scriptable control CLSID</span></span>             | <span data-ttu-id="fb807-118">CLSID de contrôle ne pouvant pas être scriptable</span><span class="sxs-lookup"><span data-stu-id="fb807-118">Nonscriptable control CLSID</span></span>          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| <span data-ttu-id="fb807-119">Windows 8.1, Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fb807-119">Windows 8.1, Windows Server 2012 R2</span></span>     | <span data-ttu-id="fb807-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="fb807-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span> | <span data-ttu-id="fb807-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="fb807-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span> |
| <span data-ttu-id="fb807-122">Windows 8, Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb807-122">Windows 8, Windows Server 2012</span></span>          | <span data-ttu-id="fb807-123">5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="fb807-123">5F681803-2900-4C43-A1CC-CF405404A676</span></span> | <span data-ttu-id="fb807-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="fb807-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span> |
| <span data-ttu-id="fb807-125">Windows 7, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb807-125">Windows 7, Windows Server 2008</span></span>          | <span data-ttu-id="fb807-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="fb807-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span> | <span data-ttu-id="fb807-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="fb807-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span> |
| <span data-ttu-id="fb807-128">Windows Vista Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="fb807-128">Windows Vista with Service Pack 1 (SP1)</span></span> | <span data-ttu-id="fb807-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span><span class="sxs-lookup"><span data-stu-id="fb807-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span></span> | <span data-ttu-id="fb807-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span><span class="sxs-lookup"><span data-stu-id="fb807-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span></span> |
| <span data-ttu-id="fb807-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb807-131">Windows Vista</span></span>                           | <span data-ttu-id="fb807-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span><span class="sxs-lookup"><span data-stu-id="fb807-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span></span> | <span data-ttu-id="fb807-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span><span class="sxs-lookup"><span data-stu-id="fb807-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="fb807-134">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fb807-134">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="fb807-135">Incorporation du contrôle Bureau à distance ActiveX dans une page Web</span><span class="sxs-lookup"><span data-stu-id="fb807-135">Embedding the Remote Desktop ActiveX control in a webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

<span data-ttu-id="fb807-136">Exemple illustrant l’utilisation des interfaces scriptables.</span><span class="sxs-lookup"><span data-stu-id="fb807-136">Example that demonstrates the use of the scriptable interfaces.</span></span>

</dd> <dt>

[<span data-ttu-id="fb807-137">Implémentation de canaux virtuels scriptables à l’aide de Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="fb807-137">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="fb807-138">Exemples de code qui illustrent les étapes d’implémentation de canaux virtuels scriptables avec Connexion Bureau à distance par le Web.</span><span class="sxs-lookup"><span data-stu-id="fb807-138">Code examples that show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="fb807-139">Utilisation du contrôle ActiveX Bureau à distance avec des canaux virtuels</span><span class="sxs-lookup"><span data-stu-id="fb807-139">Using the Remote Desktop ActiveX control with virtual channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="fb807-140">Si vous avez activé une application de canaux virtuels dans votre déploiement Services Bureau à distance, vous pouvez mettre cette application à la disposition des ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="fb807-140">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers.</span></span>

</dd> <dt>

[<span data-ttu-id="fb807-141">Exemple de page Web inclus avec le contrôle ActiveX Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="fb807-141">Sample webpage included with the Remote Desktop ActiveX control</span></span>](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="fb807-142">Un exemple de page Web (Default.htm) se trouve dans le répertoire d’installation de Connexion Bureau à distance par le Web.</span><span class="sxs-lookup"><span data-stu-id="fb807-142">A sample webpage (Default.htm) is in the directory where Remote Desktop Web Connection is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="fb807-143">Fournir la sécurité du client RDP</span><span class="sxs-lookup"><span data-stu-id="fb807-143">Providing for RDP client security</span></span>](providing-for-rdp-client-security.md)
</dt> <dd>

<span data-ttu-id="fb807-144">Certaines propriétés de l’objet de contrôle ActiveX Bureau à distance sont limitées à des zones de sécurité d’URL Internet Explorer spécifiques.</span><span class="sxs-lookup"><span data-stu-id="fb807-144">Some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span>

</dd> <dt>

[<span data-ttu-id="fb807-145">Désactivation des fonctionnalités de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="fb807-145">Disabling Remote Desktop Services features</span></span>](disabling-terminal-services-features.md)
</dt> <dd>

<span data-ttu-id="fb807-146">Pour renforcer la sécurité, vous pouvez choisir de désactiver les fonctionnalités de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="fb807-146">For enhanced security, you might choose to disable Remote Desktop Services features.</span></span>

</dd> </dl>

<span data-ttu-id="fb807-147">Pour plus d’informations sur l’exemple de page Web inclus avec l’installation du contrôle ActiveX Bureau à distance, consultez [exemple de page Web inclus avec le contrôle activex Bureau à distance](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span><span class="sxs-lookup"><span data-stu-id="fb807-147">For more information about the sample webpage that is included with the installation of the Remote Desktop ActiveX control, see [Sample webpage included with the Remote Desktop ActiveX control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 




