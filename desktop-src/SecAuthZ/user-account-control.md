---
description: Permet aux utilisateurs d’effectuer des tâches courantes en tant que non-administrateurs, appelées utilisateurs standard et en tant qu’administrateurs sans avoir à changer d’utilisateur, à fermer la session ou à utiliser exécuter en tant que.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Contrôle de compte d’utilisateur (autorisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952718"
---
# <a name="user-account-control-authorization"></a><span data-ttu-id="a7ff6-103">Contrôle de compte d’utilisateur (autorisation)</span><span class="sxs-lookup"><span data-stu-id="a7ff6-103">User Account Control (Authorization)</span></span>

<span data-ttu-id="a7ff6-104">Le contrôle de compte d’utilisateur (UAC) permet aux utilisateurs d’effectuer des tâches courantes en tant que non-administrateurs, appelées utilisateurs standard et en tant qu’administrateurs sans avoir à changer d’utilisateur, à fermer la session ou à utiliser **exécuter en tant que**.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-104">User Account Control (UAC) enables users to perform common tasks as nonadministrators, called standard users, and as administrators without having to switch users, log off, or use **Run As**.</span></span> <span data-ttu-id="a7ff6-105">Le comportement du contrôle de compte d’utilisateur pour le paramètre « ne jamais notifier » ne désactive plus le contrôle de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-105">The behavior of UAC for the "Never notify" setting no longer disables UAC.</span></span> <span data-ttu-id="a7ff6-106">Le paramètre « ne jamais notifier » vous donne un jeton de fractionnement et élève toujours automatiquement le privilège requis.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-106">The "Never notify" setting gives you a split token and always automatically elevates the privilege required.</span></span> <span data-ttu-id="a7ff6-107">Cette subtilité peut entraîner des problèmes de compatibilité avec votre application.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-107">This subtlety may cause your app to have compatibility problems.</span></span> <span data-ttu-id="a7ff6-108">Vous pouvez toujours désactiver le contrôle de compte d’utilisateur en utilisant des stratégies de groupe ou en définissant manuellement la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-108">You can still disable UAC by using Group Policies or manually setting the registry key.</span></span>

<span data-ttu-id="a7ff6-109">**Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Le paramètre « ne jamais notifier » désactive le contrôle de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-109">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** The "Never notify" setting disables UAC.</span></span>

<span data-ttu-id="a7ff6-110">Par exemple, si vous effectuez les étapes suivantes pour modifier le paramètre « ne jamais notifier », vous pouvez obtenir des résultats différents lorsque vous essayez de créer un fichier dans un dossier qui nécessite des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-110">For example, if you perform the following steps to change the "Never notify" setting, you get different outcomes when you attempt to create a file in a folder that requires elevated privileges.</span></span> <span data-ttu-id="a7ff6-111">Le comportement de Windows 8 est de refuser l’accès.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-111">The Windows 8 behavior is to deny access.</span></span> <span data-ttu-id="a7ff6-112">Le comportement de Windows 7 vous permet de créer le fichier File.txt.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-112">The Windows 7 behavior allows you to create the File.txt file.</span></span>

1.  <span data-ttu-id="a7ff6-113">Cliquez ou appuyez sur **Start**.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-113">Click or tap **Start**.</span></span> <span data-ttu-id="a7ff6-114">Dans la zone de recherche, tapez « modifier les paramètres de contrôle de compte d’utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="a7ff6-114">In the search box, type "Change User Account Control settings".</span></span>
2.  <span data-ttu-id="a7ff6-115">Cliquez ou appuyez sur **modifier les paramètres du contrôle de compte d’utilisateur** pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-115">Click or tap **Change User Account Control settings** to open it.</span></span>
3.  <span data-ttu-id="a7ff6-116">Déplacez le curseur sur **ne jamais notifier**.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-116">Move the slider to **Never notify**.</span></span>
4.  <span data-ttu-id="a7ff6-117">Cliquez ou appuyez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-117">Click or tap **OK**.</span></span>
5.  <span data-ttu-id="a7ff6-118">Redémarrez votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-118">Restart your computer.</span></span>
6.  <span data-ttu-id="a7ff6-119">Cliquez ou appuyez sur **Démarrer** , puis sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-119">Click or tap **Start** and then **Run**.</span></span> <span data-ttu-id="a7ff6-120">Dans la zone **ouvrir** , tapez « Cmd.exe ».</span><span class="sxs-lookup"><span data-stu-id="a7ff6-120">In the **Open** box, type "Cmd.exe".</span></span> <span data-ttu-id="a7ff6-121">Notez que le titre de la fenêtre ne contient pas la chaîne « administrateur ».</span><span class="sxs-lookup"><span data-stu-id="a7ff6-121">Note that the title of the window doesn't contain the string "Administrator".</span></span>
7.  <span data-ttu-id="a7ff6-122">Tapez « Echo >% windir% \\ system32 \\File.txt ».</span><span class="sxs-lookup"><span data-stu-id="a7ff6-122">Type "echo > %windir%\\system32\\File.txt".</span></span>

<span data-ttu-id="a7ff6-123">Le contrôle de compte d’utilisateur a été ajouté dans Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-123">UAC was added in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="a7ff6-124">Un compte d’utilisateur standard est synonyme d’un compte d’utilisateur dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-124">A standard user account is synonymous with a user account in Windows XP.</span></span> <span data-ttu-id="a7ff6-125">Les comptes d’utilisateurs qui sont membres du groupe Administrateurs local exécutent la plupart des applications en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-125">User accounts that are members of the local Administrators group will run most applications as a standard user.</span></span>

<span data-ttu-id="a7ff6-126">Pour plus d’informations sur le contrôle de compte d’utilisateur, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-126">For information about UAC, see the following topics.</span></span>



| <span data-ttu-id="a7ff6-127">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a7ff6-127">Topic</span></span>                                                                                                                                        | <span data-ttu-id="a7ff6-128">Description</span><span class="sxs-lookup"><span data-stu-id="a7ff6-128">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ff6-129">[Instructions pour le contrôle de compte d’utilisateur dans le développement d’interface utilisateur](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="a7ff6-129">[Guidelines for User Account Control in UI Development](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span></span><br/> | <span data-ttu-id="a7ff6-130">Informations générales sur le contrôle de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-130">General information about UAC.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="a7ff6-131">Développement d’applications nécessitant des privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="a7ff6-131">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)<br/>  | <span data-ttu-id="a7ff6-132">Modèles pour le développement d’applications qui effectuent des opérations qui requièrent des privilèges d’administrateur, mais qui s’exécutent en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-132">Models for developing applications that perform operations that require administrative privilege, but that run as a standard user.</span></span><br/> |
| [<span data-ttu-id="a7ff6-133">Référence d’autorisation</span><span class="sxs-lookup"><span data-stu-id="a7ff6-133">Authorization Reference</span></span>](authorization-reference.md)<br/>                                                                            | <span data-ttu-id="a7ff6-134">Informations détaillées sur les fonctions d’autorisation, les interfaces, les structures et d’autres éléments de programmation.</span><span class="sxs-lookup"><span data-stu-id="a7ff6-134">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                        |



 

 

 




