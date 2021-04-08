---
title: Activation de session à session avec un moniker de session
description: L’activation de session à session (également appelée activation inter-sessions) permet à un processus client de démarrer (activer) un processus serveur local sur une session spécifiée.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729620"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a><span data-ttu-id="f2d77-103">Activation de session à session avec un moniker de session</span><span class="sxs-lookup"><span data-stu-id="f2d77-103">Session-to-Session Activation with a Session Moniker</span></span>

<span data-ttu-id="f2d77-104">L’activation de session à session (également appelée activation inter-sessions) permet à un processus client de démarrer (activer) un processus serveur local sur une session spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f2d77-104">Session-to-session activation (also called cross-session activation) allows a client process to start (activate) a local server process on a specified session.</span></span> <span data-ttu-id="f2d77-105">Cette fonctionnalité est disponible pour les applications qui sont configurées pour s’exécuter dans le contexte de sécurité de l’utilisateur interactif, également appelé mode d’activation d’objet « RunAs interactive User ».</span><span class="sxs-lookup"><span data-stu-id="f2d77-105">This feature is available for applications that are configured to run in the security context of the interactive user, also known as the "RunAs Interactive User" object activation mode.</span></span> <span data-ttu-id="f2d77-106">Pour plus d’informations sur les contextes de sécurité, consultez [le contexte de sécurité du client](/windows/desktop/SecAuthZ/the-client-security-context).</span><span class="sxs-lookup"><span data-stu-id="f2d77-106">For more information about security contexts, see [The Client's Security Context](/windows/desktop/SecAuthZ/the-client-security-context).</span></span>

<span data-ttu-id="f2d77-107">DCOM (Distributed COM) permet l’activation d’objets pour chaque session à l’aide d’un [moniker de session](session-monikers.md)fourni par le système.</span><span class="sxs-lookup"><span data-stu-id="f2d77-107">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied [Session Moniker](session-monikers.md).</span></span> <span data-ttu-id="f2d77-108">D’autres monikers fournis par le système incluent les [monikers de fichiers](../com/file-monikers.md), les [monikers d’élément](../com/item-monikers.md), les [monikers composites](../com/composite-monikers.md)génériques, les [anti-monikers](../com/anti-monikers.md), les [monikers de pointeur](../com/pointer-monikers.md)et les [monikers d’URL](../com/url-monikers.md).</span><span class="sxs-lookup"><span data-stu-id="f2d77-108">Other system-supplied monikers include [file monikers](../com/file-monikers.md), [item monikers](../com/item-monikers.md), generic [composite monikers](../com/composite-monikers.md), [anti-monikers](../com/anti-monikers.md), [pointer monikers](../com/pointer-monikers.md), and [URL monikers](../com/url-monikers.md).</span></span>

<span data-ttu-id="f2d77-109">Pour pouvoir utiliser le moniker de session, l’application DCOM doit être configurée pour s’exécuter en tant qu’utilisateur interactif.</span><span class="sxs-lookup"><span data-stu-id="f2d77-109">To be able to use the session moniker, the DCOM application must be set to run as the interactive user.</span></span> <span data-ttu-id="f2d77-110">Cela peut être défini à l’aide de l’outil d’administration Services de composants, en affichant les propriétés de l’application DCOM et en sélectionnant **l’utilisateur interactif** sous l’onglet **identité** . Pour plus d’informations sur les risques de sécurité possibles associés à la configuration d’une application DCOM pour qu’elle s’exécute en tant qu’utilisateur interactif dans un environnement de Services Bureau à distance, consultez la section « identité de l’application (COM) » de la documentation COM dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="f2d77-110">This can be set by using the Component Services Administrative tool, viewing the Properties of the DCOM application, and selecting **The interactive user** on the **Identity** tab. For more information about the possible security risks associated with setting a DCOM application to run as the interactive user in a Remote Desktop Services environment, see the "Application Identity (COM)" section of the COM documentation in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="f2d77-111">Si un autre type d’utilisateur est sélectionné pour exécuter l’application, le moniker de session sera ignoré par l’application.</span><span class="sxs-lookup"><span data-stu-id="f2d77-111">If any other type of user is selected to run the application, the session moniker will be ignored by the application.</span></span> <span data-ttu-id="f2d77-112">Le moniker de session est également ignoré par les applications serveur COM+.</span><span class="sxs-lookup"><span data-stu-id="f2d77-112">The session moniker is also ignored by COM+ server applications.</span></span> <span data-ttu-id="f2d77-113">Pour plus d’informations sur les autres méthodes permettant de sélectionner le type d’utilisateur pour l’exécution de l’application, consultez la documentation COM dans le kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="f2d77-113">For more information about other methods for selecting the type of user to run the application, see the COM documentation in the Platform SDK.</span></span>

<span data-ttu-id="f2d77-114">Pour créer un moniker de session, vous devez composer l’ID de session de la session Services Bureau à distance avec un moniker de classe qui spécifie l’ID de classe du serveur de traitement.</span><span class="sxs-lookup"><span data-stu-id="f2d77-114">To create a session moniker, you must compose the session ID of the Remote Desktop Services session with a class moniker that specifies the process server's class ID.</span></span>

<span data-ttu-id="f2d77-115">**Pour créer un moniker de session**</span><span class="sxs-lookup"><span data-stu-id="f2d77-115">**To create a session moniker**</span></span>

1.  <span data-ttu-id="f2d77-116">Préfixez le nom d’affichage du moniker de la classe avec le nom complet du moniker de session à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="f2d77-116">Prefix the display name of the class moniker with the display name of the session moniker by using the following syntax:</span></span>

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    <span data-ttu-id="f2d77-117">où *digits* représente l’ID de session de la session sur laquelle le processus serveur sera démarré, et où *Class ID* représente l’ID de classe du serveur.</span><span class="sxs-lookup"><span data-stu-id="f2d77-117">where *digits* represents the session ID of the session on which the server process will be started, and where *class id* represents the class ID of the server.</span></span> <span data-ttu-id="f2d77-118">Notez que l’ID de session est un nombre en base 10.</span><span class="sxs-lookup"><span data-stu-id="f2d77-118">Note that the session ID is a base-10 number.</span></span>

    <span data-ttu-id="f2d77-119">Pour les ordinateurs qui exécutent Windows XP ou une version ultérieure, l’utilisation de la syntaxe suivante entraîne l’envoi par COM de l’activation à la session de console physique active, quel que soit son ID de session :</span><span class="sxs-lookup"><span data-stu-id="f2d77-119">For computers that are running Windows XP or later, using the following syntax will result in COM sending the activation to the currently active physical console session, whatever its session ID is:</span></span>

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  <span data-ttu-id="f2d77-120">Une fois que vous avez créé le moniker de session, vous pouvez passer le résultat à la fonction [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) ou à la fonction [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f2d77-120">After you have created the session moniker, you can pass the result to either the [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) function or the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function.</span></span>

<span data-ttu-id="f2d77-121">Vous pouvez utiliser un moniker de session de la même façon que vous le feriez pour tout autre moniker.</span><span class="sxs-lookup"><span data-stu-id="f2d77-121">You can use a session moniker in the same way as you would use any other moniker.</span></span>

<span data-ttu-id="f2d77-122">Pour obtenir un exemple de code qui montre comment activer un processus serveur local sur une session spécifiée, consultez [utilisation d’un moniker de session](using-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="f2d77-122">For a code sample that demonstrates how to activate a local server process on a specified session, see [Using a Session Moniker](using-a-session-moniker.md).</span></span>

<span data-ttu-id="f2d77-123">Pour plus d’informations sur l’activation d’objets, les monikers fournis par le système et les monikers de classe, consultez la documentation COM dans le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="f2d77-123">For more information about object activation, system-supplied monikers and class monikers, see the COM documentation in the Platform SDK.</span></span>

> [!Note]  
> <span data-ttu-id="f2d77-124">Les processus créés entre les sessions ont une limite supérieure de la taille du bloc d’environnement.</span><span class="sxs-lookup"><span data-stu-id="f2d77-124">Processes that are created across sessions have an upper limit on the size of the environment block.</span></span> <span data-ttu-id="f2d77-125">Cette limite est d’environ 4 Ko, mais elle peut être plus grande ou plus petite selon les autres informations nécessaires pour créer le processus (par exemple, les noms de fichiers, les répertoires et les paramètres pour le nouveau processus).</span><span class="sxs-lookup"><span data-stu-id="f2d77-125">This limit is around 4 KB, but it can be larger or smaller depending on what other information is needed to create the process (for example file names, directories, and parameters for the new process).</span></span>

 

 

 