---
description: Si cette stratégie système par ordinateur est définie sur &\# 0034 ; 1&\# 0034 ;, le programme d’installation écrit des messages de débogage communs dans le débogueur à l’aide de la fonction OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866362"
---
# <a name="debug"></a><span data-ttu-id="8ba52-103">Débogage</span><span class="sxs-lookup"><span data-stu-id="8ba52-103">Debug</span></span>

<span data-ttu-id="8ba52-104">Si cette [stratégie système](system-policy.md) par ordinateur est définie sur « 1 », le programme d’installation écrit des messages de débogage communs dans le débogueur à l’aide de la fonction [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="8ba52-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer writes common debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="8ba52-105">Si cette valeur est définie sur « 2 », le programme d’installation écrit tous les messages de débogage valides dans le débogueur à l’aide de la fonction [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="8ba52-105">If this value is set to "2", the installer writes all valid debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="8ba52-106">Cette stratégie est à des fins de débogage uniquement et peut ne pas être prise en charge dans les futures versions de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8ba52-106">This policy is for debugging purposes only and may not be supported in future versions of Windows Installer.</span></span>

<span data-ttu-id="8ba52-107">Windows Installer écrit uniquement des lignes de commande dans le fichier journal si le troisième bit (0x04) est défini dans la valeur de la stratégie de débogage.</span><span class="sxs-lookup"><span data-stu-id="8ba52-107">Windows Installer only writes command lines into the log file if the third (0x04) bit is set in the value of the Debug policy.</span></span> <span data-ttu-id="8ba52-108">Par conséquent, pour afficher les lignes de commande dans le journal, définissez la valeur de la stratégie de débogage sur 7.</span><span class="sxs-lookup"><span data-stu-id="8ba52-108">Therefore, to display command lines in the log, set the Debug policy value to 7.</span></span> <span data-ttu-id="8ba52-109">Cela n’affiche pas les propriétés associées à un [contrôle d’édition](edit-control.md) avec l' [attribut de contrôle de mot de passe](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="8ba52-109">This does not display properties associated with an [Edit Control](edit-control.md) having the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="8ba52-110">Cela rendra les propriétés définies sur la ligne de commande visibles dans le journal même si la propriété est incluse dans la propriété [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="8ba52-110">This will make properties set on the command line visible in the log even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span> <span data-ttu-id="8ba52-111">Pour plus d’informations, consultez [la page empêcher l’écriture d’informations confidentielles dans le fichier journal](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="8ba52-111">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="8ba52-112">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="8ba52-112">Registry Key</span></span>

<span data-ttu-id="8ba52-113">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="8ba52-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="8ba52-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="8ba52-114">Data Type</span></span>

<span data-ttu-id="8ba52-115">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="8ba52-115">**REG\_DWORD**</span></span>

 

 
