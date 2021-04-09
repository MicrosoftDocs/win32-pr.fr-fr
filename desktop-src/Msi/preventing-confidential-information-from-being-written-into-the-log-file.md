---
description: Les développeurs peuvent empêcher la saisie d’informations confidentielles, telles que les mots de passe, dans le fichier journal au cours d’une installation Windows Installer.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Empêcher l’écriture d’informations confidentielles dans le fichier journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034392"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a><span data-ttu-id="8fb66-103">Empêcher l’écriture d’informations confidentielles dans le fichier journal</span><span class="sxs-lookup"><span data-stu-id="8fb66-103">Preventing Confidential Information from Being Written into the Log File</span></span>

<span data-ttu-id="8fb66-104">Lorsque vous utilisez l’Windows Installer, vous pouvez empêcher que des informations confidentielles, par exemple des mots de passe, soient entrées dans le fichier journal et soient rendues visibles.</span><span class="sxs-lookup"><span data-stu-id="8fb66-104">When using the Windows Installer, you can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span>

-   <span data-ttu-id="8fb66-105">Le programme d’installation n’écrit jamais les informations de la colonne Password de la [table ServiceInstall](serviceinstall-table.md) dans le journal.</span><span class="sxs-lookup"><span data-stu-id="8fb66-105">The Installer never writes the information in the Password column of the [ServiceInstall table](serviceinstall-table.md) into the log.</span></span>
-   <span data-ttu-id="8fb66-106">Vous pouvez empêcher le programme d’installation d’écrire la propriété associée à un [contrôle d’édition](edit-control.md) dans le journal en définissant l' [attribut de contrôle de mot de passe](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="8fb66-106">You can prevent the Installer from writing the property that is associated with an [Edit Control](edit-control.md) into the log by setting the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="8fb66-107">La propriété associée à un contrôle d’édition avec l’attribut de contrôle de mot de passe est masquée même si la stratégie de [débogage](debug.md) est définie sur la valeur 7.</span><span class="sxs-lookup"><span data-stu-id="8fb66-107">The property associated with an Edit Control that has the Password Control Attribute is hidden even if the [Debug](debug.md) policy is set to a value of 7.</span></span>
-   <span data-ttu-id="8fb66-108">Vous pouvez empêcher le programme d’installation d’écrire une propriété privée dans le journal en incluant la propriété dans la propriété [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="8fb66-108">You can prevent the Installer from writing a private property into the log by including the property in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>
    > [!Note]  
    > <span data-ttu-id="8fb66-109">Cette méthode peut rendre les informations confidentielles entrées sur une ligne de commande visibles dans le journal.</span><span class="sxs-lookup"><span data-stu-id="8fb66-109">This method can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="8fb66-110">Lorsque la stratégie de [débogage](debug.md) est définie sur 7, le programme d’installation écrit les informations entrées sur une ligne de commande dans le journal.</span><span class="sxs-lookup"><span data-stu-id="8fb66-110">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="8fb66-111">Cela rend la propriété entrée sur une ligne de commande visible, même si la propriété est incluse dans la propriété [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="8fb66-111">This makes the property entered on a command line visible even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>

     

-   <span data-ttu-id="8fb66-112">Vous pouvez empêcher l’écriture dans le journal des informations contenues dans la colonne cible de la table [CustomAction](customaction-table.md) en incluant l’indicateur de bit HideTarget dans le champ type de la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="8fb66-112">You can prevent the information in the Target column of the [CustomAction](customaction-table.md) Table from being written into the log by including the HideTarget bit flag in the Type field of the CustomAction table.</span></span> <span data-ttu-id="8fb66-113">La valeur de cet indicateur est 8192 (0x2000).</span><span class="sxs-lookup"><span data-stu-id="8fb66-113">The value of this flag is 8192 (0x2000).</span></span> <span data-ttu-id="8fb66-114">Pour plus d’informations, consultez [option cible masquée des actions personnalisées](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="8fb66-114">For more information, see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

 

 



