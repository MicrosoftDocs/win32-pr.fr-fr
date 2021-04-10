---
title: Utilisation du paramètre de contexte
description: Utilisation du paramètre de contexte
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Media Format SDK, paramètre de contexte
- Windows Media Format SDK, paramètre pvContext
- paramètre pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101241"
---
# <a name="using-the-context-parameter"></a><span data-ttu-id="cc601-106">Utilisation du paramètre de contexte</span><span class="sxs-lookup"><span data-stu-id="cc601-106">Using the Context Parameter</span></span>

<span data-ttu-id="cc601-107">Certains des rappels utilisés par le kit de développement logiciel (SDK) du format Windows Media prennent un paramètre appelé *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="cc601-107">Some of the callbacks used by the Windows Media Format SDK take a parameter called *pvContext*.</span></span> <span data-ttu-id="cc601-108">Les objets appelants passent le long de la valeur que vous spécifiez dans la méthode qui a démarré l’action asynchrone.</span><span class="sxs-lookup"><span data-stu-id="cc601-108">The calling objects pass along the value you specify in the method that began the asynchronous action.</span></span> <span data-ttu-id="cc601-109">Par exemple, quand vous appelez [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), vous pouvez passer une valeur pour *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="cc601-109">For example, when you call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can pass a value for *pvContext*.</span></span> <span data-ttu-id="cc601-110">Quand la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) est appelée par l’objet lecteur pour informer votre application que le fichier a été ouvert, elle transmet la valeur que vous avez utilisée dans votre appel à **Open** en tant que paramètre *pvContext* de **OnStatus**.</span><span class="sxs-lookup"><span data-stu-id="cc601-110">When the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method is called by the reader object to notify your application that the file has been opened, it will pass whatever value you used in your call to **Open** as the *pvContext* parameter of **OnStatus**.</span></span> <span data-ttu-id="cc601-111">Ce paramètre de contexte est fourni pour votre utilisation et vous pouvez l’utiliser comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="cc601-111">This context parameter is provided for your use and you can use it in any way you like.</span></span>

<span data-ttu-id="cc601-112">Le paramètre *pvContext* est le plus souvent utilisé lorsque plusieurs objets doivent partager le même rappel.</span><span class="sxs-lookup"><span data-stu-id="cc601-112">The *pvContext* parameter is most often used when multiple objects need to share the same callback.</span></span> <span data-ttu-id="cc601-113">Par exemple, plusieurs objets utilisent la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="cc601-113">For example, several objects use the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="cc601-114">Vous pouvez utiliser *pvContext* pour permettre aux différents objets de partager une implémentation de **OnStatus** en passant une valeur différente pour *pvContext* sur votre appel d’origine.</span><span class="sxs-lookup"><span data-stu-id="cc601-114">You can use *pvContext* to enable the different objects to share one implementation of **OnStatus** by passing a different value for *pvContext* on your original call.</span></span> <span data-ttu-id="cc601-115">Dans votre implémentation de **OnStatus**, vous pouvez créer une branche de la logique de gestion des messages en fonction de la valeur de *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="cc601-115">In your implementation of **OnStatus**, you can branch the message handling logic based on the value of *pvContext*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc601-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc601-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc601-117">**Utilisation des méthodes de rappel**</span><span class="sxs-lookup"><span data-stu-id="cc601-117">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




