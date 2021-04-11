---
title: Activation des informations d’erreur étendues
description: Activation des informations d’erreur étendues pour l’appel de procédure distante (RPC).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197032"
---
# <a name="enabling-extended-error-information"></a><span data-ttu-id="67c75-103">Activation des informations d’erreur étendues</span><span class="sxs-lookup"><span data-stu-id="67c75-103">Enabling Extended Error Information</span></span>

<span data-ttu-id="67c75-104">Pour activer les informations d’erreur étendues, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="67c75-104">To enable extended error information, take the following steps:</span></span>

<span data-ttu-id="67c75-105">Ouvrez la stratégie de l’ordinateur local à l’aide de l’interface gpedit. msc.</span><span class="sxs-lookup"><span data-stu-id="67c75-105">Open the local machine policy using the gpedit.msc interface.</span></span>

<span data-ttu-id="67c75-106">Accédez à la stratégie située à la page Configuration ordinateur/Modèles d’administration/système/appel de procédure distante/prise en charge des dépannages RPC/propagation des informations d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="67c75-106">Navigate to the policy located at Computer Configuration/Administrative Templates/System/Remote Procedure Call/Rpc Troubleshooting Support/Propagation of extended error information</span></span>

<span data-ttu-id="67c75-107">Activez la stratégie et définissez la **propagation des informations d’erreurs étendues** sur « on ».</span><span class="sxs-lookup"><span data-stu-id="67c75-107">Enable the policy, and set the field **Propagation of extended error information** to "On".</span></span>

<span data-ttu-id="67c75-108">Ce processus active la propagation des informations d’erreur étendues pour tous les processus sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="67c75-108">This process turns the propagation of extended error information on for all processes on the machine.</span></span>

<span data-ttu-id="67c75-109">Pour activer les informations d’erreur étendues uniquement pour certains processus sur un ordinateur, ou pour les désactiver uniquement pour certains processus sur l’ordinateur, utilisez l’option **désactivé avec les exceptions** ou **avec les exceptions** .</span><span class="sxs-lookup"><span data-stu-id="67c75-109">To enable extended error information for only certain processes on a computer, or to disable it for only certain processes on the computer, use the **Off with exceptions** or **On with exceptions** options.</span></span> <span data-ttu-id="67c75-110">Les deux options utilisent le champ **exceptions d’informations d’erreur étendues** pour spécifier les processus qui ont le paramètre par défaut et les processus qui ont le contraire du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="67c75-110">Both options use the field **Extended Error Information Exceptions** to specify which processes have the default setting, and which processes have the opposite of the default setting.</span></span> <span data-ttu-id="67c75-111">Les **exceptions d’informations d’erreur étendues** contiennent une liste de noms de processus.</span><span class="sxs-lookup"><span data-stu-id="67c75-111">**Extended Error Information Exceptions** contains a list of process names.</span></span>

<span data-ttu-id="67c75-112">Si la ligne de commande d’un processus commence par une chaîne qui se trouve dans les **exceptions d’informations d’erreur étendues**, le processus reçoit l’inverse du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="67c75-112">If the command line of a process starts with a string that is in the **Extended Error Information Exceptions**, the process will receive the opposite of the default setting.</span></span> <span data-ttu-id="67c75-113">Par exemple, si vous souhaitez que tous les processus sur votre ordinateur propagent les informations d’erreur étendues, à l’exception de LSASS et du processus appelé **serveur sécurisé**, définissez la **propagation des informations d’erreur étendues** **sur activé avec des exceptions** et spécifiez dans le champ **exceptions d’informations d’erreur étendues** la chaîne suivante : LSASS « serveur sécurisé ».</span><span class="sxs-lookup"><span data-stu-id="67c75-113">For example, if you want all the process on your computer to propagate extended error information, except for lsass and the process called **Secure Server**, set the **Propagation of extended error information** to **On with exceptions**, and specify in the **Extended Error Information Exceptions** field the following string: lsass "Secure Server".</span></span>

<span data-ttu-id="67c75-114">Les chaînes peuvent être placées entre guillemets doubles, mais cela est facultatif s’il n’y a pas d’espaces dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="67c75-114">Strings can be enclosed with double quotes, but doing so is optional if there are no spaces in the string.</span></span> <span data-ttu-id="67c75-115">En outre, le début de la ligne de commande du processus peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="67c75-115">Also, the beginning of the process command line can be specified.</span></span> <span data-ttu-id="67c75-116">Par exemple, si la valeur **off avec exceptions** est spécifiée dans le champ **propagation des informations d’erreur étendues** , et dans le champ **exceptions d’informations d’erreur étendues** , les éléments suivants sont spécifiés : Win.</span><span class="sxs-lookup"><span data-stu-id="67c75-116">For example, if **Off with exceptions** is specified in the **Propagation of extended error information** field, and in the **Extended Error Information Exceptions** field the following is specified: win.</span></span>

<span data-ttu-id="67c75-117">Chaque processus qui commence par « Win » propage les informations d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="67c75-117">Each process that begins with "win" propagates extended error information.</span></span> <span data-ttu-id="67c75-118">Sur de nombreux ordinateurs, par exemple, ces processus sont winlogon.exe et WINWORD.EXE.</span><span class="sxs-lookup"><span data-stu-id="67c75-118">On many computers, for example, those processes would be winlogon.exe and WINWORD.EXE.</span></span>

 

 




