---
title: Utilisation du rappel OnStatus
description: Utilisation du rappel OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media Format SDK, méthode de rappel OnStatus
- Windows Media Format SDK, interface IWMStatusCallback
- OnStatus, méthode de rappel, à propos de
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940662"
---
# <a name="using-the-onstatus-callback"></a><span data-ttu-id="263b7-107">Utilisation du rappel OnStatus</span><span class="sxs-lookup"><span data-stu-id="263b7-107">Using the OnStatus Callback</span></span>

<span data-ttu-id="263b7-108">La méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) est appelée par plusieurs objets dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="263b7-108">The [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method is called by several objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="263b7-109">**OnStatus** reçoit des messages qui représentent des modifications de l’état des opérations du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="263b7-109">**OnStatus** receives messages that represent changes in the status of SDK operations.</span></span>

<span data-ttu-id="263b7-110">Pour utiliser la méthode de rappel **OnStatus** , vous devez implémenter dans votre application une classe qui hérite de l’interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) .</span><span class="sxs-lookup"><span data-stu-id="263b7-110">To use the **OnStatus** callback method, you must implement a class in your application that inherits from the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface.</span></span> <span data-ttu-id="263b7-111">Incluez le code de votre version de **OnStatus** dans la classe.</span><span class="sxs-lookup"><span data-stu-id="263b7-111">Include code for your version of **OnStatus** in the class.</span></span> <span data-ttu-id="263b7-112">Vous trouverez plusieurs exemples d’implémentations de **OnStatus** dans les exemples inclus dans ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="263b7-112">Several examples of **OnStatus** implementations can be found in the samples included with this SDK.</span></span> <span data-ttu-id="263b7-113">Pour plus d’informations sur les exemples, consultez [exemples d’applications](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="263b7-113">For more information about the samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="263b7-114">Vous devez associer votre implémentation du rappel d’État à différents objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="263b7-114">You must associate your implementation of the status callback with various objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="263b7-115">Chaque objet a une façon différente de créer cette association.</span><span class="sxs-lookup"><span data-stu-id="263b7-115">Each object has a different way of making this association.</span></span> <span data-ttu-id="263b7-116">Pour obtenir la liste des méthodes qui associent des objets spécifiques, consultez la page de référence **IWMStatusCallback** .</span><span class="sxs-lookup"><span data-stu-id="263b7-116">For a list of the methods that associate specific objects, see the **IWMStatusCallback** reference page.</span></span>

<span data-ttu-id="263b7-117">Les messages d’État qui peuvent être reçus par **OnStatus** sont définis dans le type d’énumération d' [**\_ État WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="263b7-117">The status messages that can be received by **OnStatus** are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

<span data-ttu-id="263b7-118">Vous pouvez choisir les messages à intercepter et ceux à ignorer.</span><span class="sxs-lookup"><span data-stu-id="263b7-118">You can choose which messages to trap and which to ignore.</span></span> <span data-ttu-id="263b7-119">Toutefois, il est nécessaire de répondre à certains messages d’État pour certaines fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="263b7-119">However, responding to some status messages is required for certain features.</span></span> <span data-ttu-id="263b7-120">Par exemple, lors de l’utilisation du lecteur asynchrone, la méthode [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) ouvre un fichier de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="263b7-120">For example, when using the asynchronous reader, the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method opens a file asynchronously.</span></span> <span data-ttu-id="263b7-121">La seule façon de savoir à quel moment le fichier a été ouvert consiste à intercepter le \_ message MWT ouvert.</span><span class="sxs-lookup"><span data-stu-id="263b7-121">The only way to tell when the file has been opened is to trap the MWT\_OPENED message.</span></span> <span data-ttu-id="263b7-122">En règle générale, les messages auxquels vous répondez sont des notifications de l’achèvement des tâches asynchrones.</span><span class="sxs-lookup"><span data-stu-id="263b7-122">Typically, the messages you respond to are notifications of the completion of asynchronous tasks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="263b7-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="263b7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="263b7-124">**Utilisation des méthodes de rappel**</span><span class="sxs-lookup"><span data-stu-id="263b7-124">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




