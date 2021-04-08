---
description: Cette stratégie système par ordinateur est utilisée uniquement si la journalisation n’a pas été activée par l' &\# 0034 ;/l&\# 0034 ; option de ligne de commande ou par MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Journalisation (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756615"
---
# <a name="logging-windows-installer"></a><span data-ttu-id="96da9-103">Journalisation (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="96da9-103">Logging (Windows Installer)</span></span>

<span data-ttu-id="96da9-104">Cette [stratégie système](system-policy.md) par ordinateur est utilisée uniquement si la journalisation n’a pas été activée par l’option de ligne de commande « /l » ou par [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span><span class="sxs-lookup"><span data-stu-id="96da9-104">This per-machine [system policy](system-policy.md) is used only if logging has not been enabled by the "/L" command line option or by [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span></span> <span data-ttu-id="96da9-105">Si la stratégie est définie dans ce cas, le programme d’installation crée un fichier journal dans% Temp% avec le nom aléatoire : MSI \* . Sign.</span><span class="sxs-lookup"><span data-stu-id="96da9-105">If the policy is set in this case, the installer creates a log file in %temp% with the random name: MSI\*.LOG.</span></span> <span data-ttu-id="96da9-106">Spécifiez le mode de journalisation en affectant une chaîne de caractères à la valeur de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="96da9-106">Specify the logging mode by setting the policy value to a string of characters.</span></span> <span data-ttu-id="96da9-107">Utilisez les mêmes caractères pour spécifier la stratégie de mode de journalisation telle qu’elle est utilisée par l' [option de ligne de commande](command-line-options.md)« /l ».</span><span class="sxs-lookup"><span data-stu-id="96da9-107">Use the same characters to specify logging mode policy as used by the "/L" [command line option](command-line-options.md).</span></span> <span data-ttu-id="96da9-108">Notez que vous ne pouvez pas utiliser « + » et « \* » pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="96da9-108">Note that you cannot use "+" and "\*" for the policy.</span></span>

<span data-ttu-id="96da9-109">Le mode de journalisation peut être défini à l’aide d’une stratégie, d’une option de ligne de commande ou par programme.</span><span class="sxs-lookup"><span data-stu-id="96da9-109">The logging mode can be set using policy, a command line option, or programmatically.</span></span> <span data-ttu-id="96da9-110">Pour plus d’informations sur toutes les méthodes qui sont disponibles pour définir le mode de journalisation, consultez [journalisation normale](normal-logging.md) dans la section [journalisation Windows Installer](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="96da9-110">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="96da9-111">Vous pouvez empêcher que des informations confidentielles, par exemple des mots de passe, soient entrées dans le fichier journal et rendues visibles.</span><span class="sxs-lookup"><span data-stu-id="96da9-111">You can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span> <span data-ttu-id="96da9-112">Pour plus d’informations, consultez [empêcher l’écriture d’informations confidentielles dans le fichier journal](preventing-confidential-information-from-being-written-into-the-log-file.md) .</span><span class="sxs-lookup"><span data-stu-id="96da9-112">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="registry-key"></a><span data-ttu-id="96da9-113">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="96da9-113">Registry Key</span></span>

<span data-ttu-id="96da9-114">Définissez la valeur nommée Logging sous la clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="96da9-114">Set the value named Logging under the following registry key.</span></span>

<span data-ttu-id="96da9-115">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="96da9-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="96da9-116">Type de données</span><span class="sxs-lookup"><span data-stu-id="96da9-116">Data Type</span></span>

<span data-ttu-id="96da9-117">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="96da9-117">**REG\_SZ**</span></span>

 

 



