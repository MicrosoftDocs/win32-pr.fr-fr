---
title: Modèle de Data-Pull et modèle de Data-Push
description: Modèle de Data-Pull et modèle de Data-Push
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383015"
---
# <a name="data-pull-model-and-data-push-model"></a><span data-ttu-id="0c680-103">Modèle de Data-Pull et modèle de Data-Push</span><span class="sxs-lookup"><span data-stu-id="0c680-103">Data-Pull Model and Data-Push Model</span></span>

<span data-ttu-id="0c680-104">Un client d’un moniker asynchrone peut choisir entre un modèle d’extraction de données et d’envoi de données pour conduire une opération asynchrone [**IMoniker :: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) et recevoir des notifications asynchrones.</span><span class="sxs-lookup"><span data-stu-id="0c680-104">A client of an asynchronous moniker can choose between a data-pull and data-push model for driving an asynchronous [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) operation and receiving asynchronous notifications.</span></span> <span data-ttu-id="0c680-105">Dans le modèle d’extraction de données, le client pilote l’opération de liaison et le moniker fournit des données au client uniquement lorsqu’il est lu.</span><span class="sxs-lookup"><span data-stu-id="0c680-105">In the data-pull model, the client drives the bind operation and the moniker provides data to the client only as it is read.</span></span> <span data-ttu-id="0c680-106">En d’autres termes, après le premier appel à [**IBindStatusCallback :: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), le moniker ne fournit aucune donnée au client, sauf si le client a consommé toutes les données qui sont déjà disponibles.</span><span class="sxs-lookup"><span data-stu-id="0c680-106">In other words, after the first call to [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), the moniker does not provide any data to the client unless the client has consumed all of the data that is already available.</span></span>

<span data-ttu-id="0c680-107">Étant donné que les données sont téléchargées uniquement lorsqu’elles sont demandées, les clients qui choisissent le modèle d’extraction de données doivent veiller à lire ces données en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="0c680-107">Because data is downloaded only as it is requested, clients that choose the data-pull model must make sure to read this data in a timely manner.</span></span> <span data-ttu-id="0c680-108">Dans le cas des téléchargements Internet avec [monikers d’URL](url-monikers.md), l’opération de liaison peut échouer si un client attend trop de temps avant de demander des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0c680-108">In the case of Internet downloads with [URL monikers](url-monikers.md), the bind operation may fail if a client waits too long before requesting more data.</span></span>

<span data-ttu-id="0c680-109">Dans le modèle de transmission de données, le moniker pilote l’opération de liaison asynchrone et notifie en continu au client chaque fois que de nouvelles données sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="0c680-109">In the data-push model, the moniker drives the asynchronous bind operation and continuously notifies the client whenever new data is available.</span></span> <span data-ttu-id="0c680-110">Le client peut choisir de lire ou non les données à tout moment pendant l’opération de liaison, mais le moniker va entraîner l’achèvement de l’opération de liaison, quelle que soit la valeur de l’opération de liaison.</span><span class="sxs-lookup"><span data-stu-id="0c680-110">The client may choose whether to read the data at any point during the bind operation, but the moniker will drive the bind operation to completion regardless.</span></span>

<span data-ttu-id="0c680-111">En outre, vous devez penser à suivre les règles COM pour l’allocation de mémoire lors de l’utilisation de monikers asynchrones, en particulier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0c680-111">Also, you need to remember to follow the COM rules for memory allocation when using asynchronous monikers, specifically the following:</span></span>

-   <span data-ttu-id="0c680-112">Chaque fois qu’un appel de fonction ou d’interface COM retourne une mémoire tampon (String ou other) à son client, le client est responsable de la libération de la mémoire en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="0c680-112">Whenever a COM interface or function call returns a buffer (string or other) to its client, the client is responsible for freeing the memory by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>
-   <span data-ttu-id="0c680-113">Chaque fois qu’une fonction ou une interface COM requiert une mémoire tampon de son client, le client doit allouer ce tampon à l’aide de [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) et l’appelé doit le libérer.</span><span class="sxs-lookup"><span data-stu-id="0c680-113">Whenever a COM interface or function requires a buffer from its client, the client must allocate that buffer using [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) and the callee must free it.</span></span>

<span data-ttu-id="0c680-114">Veillez à respecter ces règles lors de l’allocation de chaînes ou de mémoires tampons transmises à des monikers asynchrones, et n’oubliez pas de libérer de la mémoire retournée par les monikers asynchrones.</span><span class="sxs-lookup"><span data-stu-id="0c680-114">Be sure to follow these rules when allocating strings or buffers that are passed to asynchronous monikers, and remember to free memory returned by asynchronous monikers.</span></span> <span data-ttu-id="0c680-115">Pour plus d’informations, consultez Gestion de l' [allocation de mémoire](the-com-library.md) et des rubriques connexes.</span><span class="sxs-lookup"><span data-stu-id="0c680-115">See [Managing Memory Allocation](the-com-library.md) and related topics for complete details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c680-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c680-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c680-117">Monikers asynchrones</span><span class="sxs-lookup"><span data-stu-id="0c680-117">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 