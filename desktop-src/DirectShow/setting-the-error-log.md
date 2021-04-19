---
description: Définition du journal des erreurs
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Définition du journal des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513875"
---
# <a name="setting-the-error-log"></a><span data-ttu-id="87b06-103">Définition du journal des erreurs</span><span class="sxs-lookup"><span data-stu-id="87b06-103">Setting the Error Log</span></span>

<span data-ttu-id="87b06-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="87b06-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="87b06-105">Après avoir implémenté la classe de journalisation des erreurs, créez une nouvelle instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="87b06-105">After you implement the error logging class, create a new instance of the class.</span></span> <span data-ttu-id="87b06-106">Ensuite, donnez aux [services de modification DirectShow](directshow-editing-services.md) un pointeur en appelant la méthode [**IAMSetErrorLog ::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) sur la chronologie.</span><span class="sxs-lookup"><span data-stu-id="87b06-106">Then, give [DirectShow Editing Services](directshow-editing-services.md) a pointer to it by calling the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span> <span data-ttu-id="87b06-107">Interrogez la chronologie de l’interface **IAMSetErrorLog** .</span><span class="sxs-lookup"><span data-stu-id="87b06-107">Query the timeline for the **IAMSetErrorLog** interface.</span></span> <span data-ttu-id="87b06-108">Pour vous assurer que toutes les erreurs sont journalisées, vous devez appeler cette méthode avant de charger, d’enregistrer ou de rendre la chronologie.</span><span class="sxs-lookup"><span data-stu-id="87b06-108">To ensure that all errors are logged, you should call this method before you load, save, or render the timeline.</span></span>


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



<span data-ttu-id="87b06-109">La journalisation des erreurs n’a aucun effet sur les valeurs de retour que vous recevez lorsque vous appelez des méthodes dans votre application.</span><span class="sxs-lookup"><span data-stu-id="87b06-109">Error logging has no effect on the return values that you receive when you call methods in your application.</span></span> <span data-ttu-id="87b06-110">La journalisation des erreurs complète, mais ne remplace pas les techniques de gestion des erreurs habituelles.</span><span class="sxs-lookup"><span data-stu-id="87b06-110">Error logging complements but does not replace the usual error handling techniques.</span></span> <span data-ttu-id="87b06-111">Pour créer une application robuste, vérifiez toujours les valeurs HRESULT.</span><span class="sxs-lookup"><span data-stu-id="87b06-111">To create a robust application, always check HRESULT values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87b06-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87b06-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87b06-113">Journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="87b06-113">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



