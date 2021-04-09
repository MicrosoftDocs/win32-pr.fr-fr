---
description: Les tables de messages sont des ressources de chaîne spéciales utilisées lors de l’affichage des messages d’erreur. Ils sont déclarés dans un fichier de ressources à l’aide de l’instruction de définition de ressource MESSAGETABLE. Pour accéder aux chaînes de message, utilisez la fonction FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tables de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950439"
---
# <a name="message-tables"></a><span data-ttu-id="167a4-105">Tables de messages</span><span class="sxs-lookup"><span data-stu-id="167a4-105">Message Tables</span></span>

<span data-ttu-id="167a4-106">Les tables de messages sont des ressources de chaîne spéciales utilisées lors de l’affichage des messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="167a4-106">Message tables are special string resources used when displaying error messages.</span></span> <span data-ttu-id="167a4-107">Ils sont déclarés dans un fichier de ressources à l’aide de l’instruction de définition de ressource [MESSAGETABLE](../menurc/messagetable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="167a4-107">They are declared in a resource file using the [MESSAGETABLE](../menurc/messagetable-resource.md) resource-definition statement.</span></span> <span data-ttu-id="167a4-108">Pour accéder aux chaînes de message, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="167a4-108">To access the message strings, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function.</span></span>

<span data-ttu-id="167a4-109">Le système fournit une table de messages pour les [codes d’erreur système](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="167a4-109">The system provides a message table for the [system error codes](system-error-codes.md).</span></span> <span data-ttu-id="167a4-110">Pour récupérer la chaîne qui correspond au code d’erreur, appelez [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système.</span><span class="sxs-lookup"><span data-stu-id="167a4-110">To retrieve the string that corresponds to the error code, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag.</span></span>

<span data-ttu-id="167a4-111">Pour fournir une table de messages pour votre application, suivez les instructions figurant dans [fichiers texte du message](../eventlog/message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="167a4-111">To provide a message table for your application, follow the instructions in [Message Text Files](../eventlog/message-text-files.md).</span></span> <span data-ttu-id="167a4-112">Pour récupérer des chaînes à partir de votre table de messages, appelez [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec l’indicateur formater le \_ message \_ de \_ HMODULE.</span><span class="sxs-lookup"><span data-stu-id="167a4-112">To retrieve strings from your message table, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_HMODULE flag.</span></span>

 

 
