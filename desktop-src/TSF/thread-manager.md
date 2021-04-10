---
title: Gestionnaire de threads
description: Le gestionnaire de threads est le composant de base du gestionnaire TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Text Services Framework (TSF), gestionnaire de threads
- TSF (Text Services Framework), gestionnaire de threads
- services de texte, gestionnaire de threads
- Applications compatibles TSF, gestionnaire de threads
- Gestionnaire de threads
- Gestionnaire TSF
- notifications d'événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031487"
---
# <a name="thread-manager"></a><span data-ttu-id="8562e-110">Gestionnaire de threads</span><span class="sxs-lookup"><span data-stu-id="8562e-110">Thread Manager</span></span>

<span data-ttu-id="8562e-111">Le gestionnaire de threads est le composant de base du gestionnaire TSF.</span><span class="sxs-lookup"><span data-stu-id="8562e-111">The thread manager is the base component of the TSF manager.</span></span> <span data-ttu-id="8562e-112">Le gestionnaire de threads effectue des tâches courantes liées aux applications et aux services de texte (clients).</span><span class="sxs-lookup"><span data-stu-id="8562e-112">The thread manager performs common tasks related to both applications and text services (clients).</span></span> <span data-ttu-id="8562e-113">Ces tâches incluent, sans s’y limiter, l’activation et la désactivation des services de texte TSF, la création de gestionnaires de documents et la maintenance de la relation appropriée entre les documents et le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8562e-113">These tasks include, but are not limited to, the activation and deactivation of TSF text services, the creation of document managers, and maintenance of the proper relationship between documents and the input focus.</span></span> <span data-ttu-id="8562e-114">Le gestionnaire de thread est défini par l’interface [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) .</span><span class="sxs-lookup"><span data-stu-id="8562e-114">The thread manager is defined by the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface.</span></span>

<span data-ttu-id="8562e-115">La majorité des interfaces et des objets fournis par le gestionnaire TSF peuvent être obtenus à l’aide des méthodes fournies par l’interface du gestionnaire de threads.</span><span class="sxs-lookup"><span data-stu-id="8562e-115">The majority of the interfaces and objects provided by the TSF manager can be obtained using the methods that the thread manager interface provides.</span></span>

## <a name="applications"></a><span data-ttu-id="8562e-116">Applications</span><span class="sxs-lookup"><span data-stu-id="8562e-116">Applications</span></span>

<span data-ttu-id="8562e-117">Une application crée un objet de gestionnaire de threads en appelant [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec CLSID \_ TFThreadMgr.</span><span class="sxs-lookup"><span data-stu-id="8562e-117">An application creates a thread manager object by calling [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_TFThreadMgr.</span></span>

## <a name="text-services"></a><span data-ttu-id="8562e-118">Services de texte</span><span class="sxs-lookup"><span data-stu-id="8562e-118">Text Services</span></span>

<span data-ttu-id="8562e-119">Un service de texte obtient un objet de gestionnaire de threads dans la méthode text service [ITfTextInputProcessor :: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .</span><span class="sxs-lookup"><span data-stu-id="8562e-119">A text service obtains a thread manager object in the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span>

## <a name="event-notifications"></a><span data-ttu-id="8562e-120">Notifications d'événements</span><span class="sxs-lookup"><span data-stu-id="8562e-120">Event Notifications</span></span>

<span data-ttu-id="8562e-121">Le gestionnaire de threads fournit également des notifications d’événements aux clients.</span><span class="sxs-lookup"><span data-stu-id="8562e-121">The thread manager also provides event notification to clients.</span></span> <span data-ttu-id="8562e-122">Dans TSF, les notifications d’événements sont fournies au moyen d’un récepteur d’événements, qui est un objet COM.</span><span class="sxs-lookup"><span data-stu-id="8562e-122">In TSF, event notifications are provided by means of an event sink, which is a COM object.</span></span> <span data-ttu-id="8562e-123">Pour recevoir des notifications du gestionnaire de threads, un client implémente un objet [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) et installe le récepteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="8562e-123">To receive notifications from the thread manager, a client implements an [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) object and installs the event sink.</span></span> <span data-ttu-id="8562e-124">Le récepteur d’événements est installé en interrogeant le gestionnaire de threads pour IID \_ ITfSource et en appelant [ITfSource :: ADVISESINK](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) avec IID \_ ITfThreadMgrEventSink.</span><span class="sxs-lookup"><span data-stu-id="8562e-124">The event sink is installed by querying the thread manager for IID\_ITfSource and calling [ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfThreadMgrEventSink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8562e-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8562e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8562e-126">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="8562e-126">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="8562e-127">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="8562e-127">CoCreateInstance</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="8562e-128">ITfTextInputProcessor :: Activate</span><span class="sxs-lookup"><span data-stu-id="8562e-128">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="8562e-129">ITfThreadMgrEventSink</span><span class="sxs-lookup"><span data-stu-id="8562e-129">ITfThreadMgrEventSink</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[<span data-ttu-id="8562e-130">ITfSource :: AdviseSink</span><span class="sxs-lookup"><span data-stu-id="8562e-130">ITfSource::AdviseSink</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 