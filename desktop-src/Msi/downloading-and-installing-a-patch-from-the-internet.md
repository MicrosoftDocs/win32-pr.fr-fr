---
description: Microsoft Windows Installer accepte une Uniform Resource Locator (URL) comme source valide d’un correctif.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Téléchargement et installation d’un correctif à partir d’Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113859"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a><span data-ttu-id="58bb3-103">Téléchargement et installation d’un correctif à partir d’Internet</span><span class="sxs-lookup"><span data-stu-id="58bb3-103">Downloading and Installing a Patch From the Internet</span></span>

<span data-ttu-id="58bb3-104">Microsoft Windows Installer accepte une Uniform Resource Locator (URL) comme source valide d’un [correctif](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="58bb3-104">Microsoft Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for a [patch](patch-packages.md).</span></span> <span data-ttu-id="58bb3-105">Pour installer un correctif situé sur un serveur Web à https://MyWeb/MyPatch.msp l’adresse, utilisez la ligne de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="58bb3-105">To install a patch located on a web server at https://MyWeb/MyPatch.msp, use the following command line:</span></span>

<span data-ttu-id="58bb3-106">**msiexec/p https://MyWeb/MyPatch.msp**</span><span class="sxs-lookup"><span data-stu-id="58bb3-106">**msiexec /p https://MyWeb/MyPatch.msp**</span></span>

<span data-ttu-id="58bb3-107">Pour éviter des résultats inattendus, ne lancez pas un correctif en cliquant sur le lien de la page Web qui indique l’URL du fichier correctif.</span><span class="sxs-lookup"><span data-stu-id="58bb3-107">To avoid unexpected results, do not launch a patch by clicking the link on the webpage showing the patch file's URL.</span></span> <span data-ttu-id="58bb3-108">Vous pouvez également installer un correctif à l’aide d’un script similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="58bb3-108">You can also install a patch by using a script like the following:</span></span>


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="58bb3-109">Notez que, étant donné que l’objet [**installer**](installer-object.md) n’est pas marqué comme [SafeForScripting](safeforscripting.md) sur l’ordinateur de l’utilisateur, les utilisateurs doivent ajuster les paramètres de sécurité de leur navigateur pour que l’exemple fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="58bb3-109">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="58bb3-110">Pour plus d’informations, consultez [instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md) et de [Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="58bb3-110">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="58bb3-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58bb3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58bb3-112">Packages de correctifs</span><span class="sxs-lookup"><span data-stu-id="58bb3-112">Patch Packages</span></span>](patch-packages.md)
</dt> <dt>

[<span data-ttu-id="58bb3-113">Création d’un package de correctifs</span><span class="sxs-lookup"><span data-stu-id="58bb3-113">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="58bb3-114">Mise à jour corrective des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="58bb3-114">Patching Customized Applications</span></span>](patching-customized-applications.md)
</dt> <dt>

[<span data-ttu-id="58bb3-115">Téléchargement d’une installation à partir d’Internet</span><span class="sxs-lookup"><span data-stu-id="58bb3-115">Downloading an Installation From the Internet</span></span>](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



