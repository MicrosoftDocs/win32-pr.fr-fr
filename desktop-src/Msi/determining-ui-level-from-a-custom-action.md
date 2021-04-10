---
description: Une action personnalisée dans une table de séquence d’interface utilisateur ou un fichier exécutable externe peut nécessiter le niveau d’interface utilisateur actuel de l’installation.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Détermination du niveau d’interface utilisateur à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952308"
---
# <a name="determining-ui-level-from-a-custom-action"></a><span data-ttu-id="4832b-103">Détermination du niveau d’interface utilisateur à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="4832b-103">Determining UI Level from a Custom Action</span></span>

<span data-ttu-id="4832b-104">Une action personnalisée dans une table de séquence d’interface utilisateur ou un fichier exécutable externe peut nécessiter le niveau d’interface utilisateur actuel de l’installation.</span><span class="sxs-lookup"><span data-stu-id="4832b-104">A custom action in a UI sequence table or an external executable file may need the current user interface level of the installation.</span></span> <span data-ttu-id="4832b-105">Par exemple, une action personnalisée qui a une boîte de dialogue ne doit afficher la boîte de dialogue que lorsque le niveau de l’interface utilisateur est une interface utilisateur complète ou une interface utilisateur réduite, mais ne doit pas afficher la boîte de dialogue si le niveau d’interface utilisateur est interface utilisateur de base ou aucun.</span><span class="sxs-lookup"><span data-stu-id="4832b-105">For example, a custom action that has a dialog box should only display the dialog when the user interface level is Full UI or Reduced UI, it should not display the dialog if the user interface level is Basic UI or None.</span></span> <span data-ttu-id="4832b-106">Vous devez utiliser la propriété [**UILevel**](uilevel.md) pour déterminer le niveau actuel de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4832b-106">You should use the [**UILevel**](uilevel.md) property to determine the current user interface level.</span></span> <span data-ttu-id="4832b-107">Vous ne pouvez pas appeler [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) à partir d’une action personnalisée et il n’est pas possible de modifier la propriété de niveau interface utilisateur à partir d’une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4832b-107">You cannot call [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) from a custom action and it is not possible to change the UI level property from within a custom action.</span></span>

<span data-ttu-id="4832b-108">Il est recommandé que les actions personnalisées n’utilisent pas le niveau d’interface utilisateur comme condition pour envoyer des messages d’erreur au programme d’installation, car cela peut interférer avec la journalisation et les messages externes.</span><span class="sxs-lookup"><span data-stu-id="4832b-108">It is recommended that custom actions not use the UI level as a condition for sending error messages to the installer because this can interfere with logging and external messages.</span></span>

 

 



