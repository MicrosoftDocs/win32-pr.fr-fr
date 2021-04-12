---
description: Étant donné que l’API d’installation ne fournit pas de routine de rappel d’armoire par défaut, vous devez fournir une routine. La routine de rappel requise par la fonction SetupIterateCabinet doit avoir la même forme que celle vers laquelle pointe FileCallback.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Création d’une routine de rappel d’armoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203174"
---
# <a name="creating-a-cabinet-callback-routine"></a><span data-ttu-id="cc0cf-104">Création d’une routine de rappel d’armoire</span><span class="sxs-lookup"><span data-stu-id="cc0cf-104">Creating a Cabinet Callback Routine</span></span>

<span data-ttu-id="cc0cf-105">Étant donné que l’API d’installation ne fournit pas de routine de rappel d’armoire par défaut, vous devez fournir une routine.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-105">Because the Setup API does not supply a default cabinet callback routine, you need to supply a routine.</span></span> <span data-ttu-id="cc0cf-106">La routine de rappel requise par la fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) doit avoir la même forme que celle vers laquelle pointe [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="cc0cf-106">The callback routine that the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function requires must have the same form as those pointed to by [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span>

<span data-ttu-id="cc0cf-107">Voici la syntaxe utilisée par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) pour envoyer une notification à la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-107">Following is the syntax that [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

<span data-ttu-id="cc0cf-108">Le paramètre de *contexte* est un pointeur void vers une structure ou une variable de contexte qui peut être utilisée par la routine de rappel pour stocker des informations qui doivent être conservées entre les appels suivants de la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-108">The *Context* parameter is a void pointer to a context variable or structure that can be used by the callback routine to store information that needs to persist between subsequent calls to the callback routine.</span></span>

<span data-ttu-id="cc0cf-109">L’implémentation de ce contexte est spécifiée par la routine de rappel et n’est jamais référencée ou modifiée par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="cc0cf-109">This context's implementation is specified by the callback routine, and it is never referenced or altered by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

<span data-ttu-id="cc0cf-110">Le paramètre de *notification* est un entier non signé et sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-110">The *Notification* parameter is an unsigned integer and will be one of the following values.</span></span>



| <span data-ttu-id="cc0cf-111">Notification</span><span class="sxs-lookup"><span data-stu-id="cc0cf-111">Notification</span></span>                                                        | <span data-ttu-id="cc0cf-112">Description</span><span class="sxs-lookup"><span data-stu-id="cc0cf-112">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="cc0cf-113">**SPFILENOTIFY \_ FILEEXTRACTED**</span><span class="sxs-lookup"><span data-stu-id="cc0cf-113">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="cc0cf-114">Le fichier a été extrait de l’armoire.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-114">The file has been extracted from the cabinet.</span></span>      |
| [<span data-ttu-id="cc0cf-115">**SPFILENOTIFY \_ FILEINCABINET**</span><span class="sxs-lookup"><span data-stu-id="cc0cf-115">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="cc0cf-116">Un fichier est trouvé dans le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-116">A file is encountered in the cabinet.</span></span>              |
| [<span data-ttu-id="cc0cf-117">**SPFILENOTIFY \_ NEEDNEWCABINET**</span><span class="sxs-lookup"><span data-stu-id="cc0cf-117">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="cc0cf-118">Le fichier actuel se poursuit dans le fichier CAB suivant.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-118">The current file is continued in the next cabinet.</span></span> |



 

<span data-ttu-id="cc0cf-119">Les deux derniers paramètres, *param1* et *param2*, sont également des entiers non signés et contiennent des informations supplémentaires relatives à la notification.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-119">The final two parameters, *Param1* and *Param2*, are also unsigned integers and contain additional information relevant to the notification.</span></span> <span data-ttu-id="cc0cf-120">Pour plus d’informations sur les notifications envoyées par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), consultez [notifications de fichier CAB](cabinet-file-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="cc0cf-120">For more information about the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), see [Cabinet File Notifications](cabinet-file-notifications.md).</span></span>

<span data-ttu-id="cc0cf-121">Une \_ routine de rappel de notification de fichier SP \_ \_ retourne un entier non signé.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-121">A SP\_FILE\_NOTIFY\_CALLBACK routine returns an unsigned integer.</span></span> <span data-ttu-id="cc0cf-122">La routine de rappel du fichier cab doit retourner l’une des valeurs suivantes en fonction de la notification.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-122">The cabinet callback routine should return one of the following values depending on the notification.</span></span>

<span data-ttu-id="cc0cf-123">Pour la \_ notification SPFILENOTIFY FILEINCABINET, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) s’attend à ce que l’une des valeurs suivantes soit retournée par la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-123">For the SPFILENOTIFY\_FILEINCABINET notification, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="cc0cf-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc0cf-124">Value</span></span>         | <span data-ttu-id="cc0cf-125">Signification</span><span class="sxs-lookup"><span data-stu-id="cc0cf-125">Meaning</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="cc0cf-126">\_abandon FILEOP</span><span class="sxs-lookup"><span data-stu-id="cc0cf-126">FILEOP\_ABORT</span></span> | <span data-ttu-id="cc0cf-127">Abandon du traitement du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-127">Abort cabinet processing.</span></span> |
| <span data-ttu-id="cc0cf-128">FILEOP \_ doit</span><span class="sxs-lookup"><span data-stu-id="cc0cf-128">FILEOP\_DOIT</span></span>  | <span data-ttu-id="cc0cf-129">Extrayez le fichier actif.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-129">Extract the current file.</span></span> |
| <span data-ttu-id="cc0cf-130">FILEOP \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="cc0cf-130">FILEOP\_SKIP</span></span>  | <span data-ttu-id="cc0cf-131">Ignore le fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-131">Skip the current file.</span></span>    |



 

<span data-ttu-id="cc0cf-132">Pour les \_ notifications SPFILENOTIFY NEEDNEWCABINET et SPFILENOTIFY \_ FILEEXTRACTED, **SetupIterateCabinet** s’attend à ce que l’une des valeurs suivantes soit retournée par la routine de rappel.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-132">For SPFILENOTIFY\_NEEDNEWCABINET and SPFILENOTIFY\_FILEEXTRACTED notifications, **SetupIterateCabinet** expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="cc0cf-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc0cf-133">Value</span></span>      | <span data-ttu-id="cc0cf-134">Signification</span><span class="sxs-lookup"><span data-stu-id="cc0cf-134">Meaning</span></span>                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc0cf-135">AUCUNE \_ erreur</span><span class="sxs-lookup"><span data-stu-id="cc0cf-135">NO\_ERROR</span></span>  | <span data-ttu-id="cc0cf-136">Aucune erreur ne s’est produite. poursuivez le traitement du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-136">No error was encountered, continue processing the cabinet.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="cc0cf-137">ERREUR \_ xxx</span><span class="sxs-lookup"><span data-stu-id="cc0cf-137">ERROR\_XXX</span></span> | <span data-ttu-id="cc0cf-138">Une erreur du type spécifié s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-138">An error of the specified type occurred.</span></span> <span data-ttu-id="cc0cf-139">La fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retourne la **valeur false** et le code d’erreur spécifié est retourné par un appel à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="cc0cf-139">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> |



 

<span data-ttu-id="cc0cf-140">Si la routine de rappel retourne FILEOP \_ doit, la routine doit également fournir un chemin d’accès cible complet.</span><span class="sxs-lookup"><span data-stu-id="cc0cf-140">If the callback routine returns FILEOP\_DOIT, the routine must also provide a full target path.</span></span> <span data-ttu-id="cc0cf-141">Pour plus d’informations, consultez [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md).</span><span class="sxs-lookup"><span data-stu-id="cc0cf-141">For more information see [**SPFILENOTIFY\_FILEINCABINET**](spfilenotify-fileincabinet.md).</span></span>

 

 
