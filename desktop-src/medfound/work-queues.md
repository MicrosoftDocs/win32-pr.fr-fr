---
description: Dans Microsoft Media Foundation, une file d’attente de travail est un moyen efficace d’effectuer des opérations asynchrones sur un autre thread.
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: Files d’attente de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203102"
---
# <a name="work-queues"></a><span data-ttu-id="cd988-103">Files d’attente de travail</span><span class="sxs-lookup"><span data-stu-id="cd988-103">Work Queues</span></span>

<span data-ttu-id="cd988-104">Dans Microsoft Media Foundation, une file d’attente de travail est un moyen efficace d’effectuer des opérations asynchrones sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="cd988-104">In Microsoft Media Foundation, a work queue is an efficient way to perform asynchronous operations on another thread.</span></span>

<span data-ttu-id="cd988-105">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd988-105">This section contains the following topics.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd988-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="cd988-106">Topic</span></span></th>
<th><span data-ttu-id="cd988-107">Description</span><span class="sxs-lookup"><span data-stu-id="cd988-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd988-108"><a href="using-work-queues.md">Utilisation des files d’attente de travail</a></span><span class="sxs-lookup"><span data-stu-id="cd988-108"><a href="using-work-queues.md">Using Work Queues</a></span></span></td>
<td><span data-ttu-id="cd988-109">Décrit comment une application ou un composant peut utiliser des files d’attente de travail pour effectuer des opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="cd988-109">Describes how an application or component can use work queues to perform asynchronous operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd988-110"><a href="writing-an-asynchronous-method.md">Écriture d’une méthode asynchrone</a></span><span class="sxs-lookup"><span data-stu-id="cd988-110"><a href="writing-an-asynchronous-method.md">Writing an Asynchronous Method</a></span></span></td>
<td><span data-ttu-id="cd988-111">Décrit comment écrire une méthode asynchrone qui suit le modèle Begin/End décrit dans <a href="asynchronous-callback-methods.md">méthodes de rappel asynchrones</a>.</span><span class="sxs-lookup"><span data-stu-id="cd988-111">Describes how to write an asynchronous method that follows the Begin/End pattern described in <a href="asynchronous-callback-methods.md">Asynchronous Callback Methods</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd988-112"><a href="custom-asynchronous-result-objects.md">Objets de résultats asynchrones personnalisés</a></span><span class="sxs-lookup"><span data-stu-id="cd988-112"><a href="custom-asynchronous-result-objects.md">Custom Asynchronous Result Objects</a></span></span></td>
<td><span data-ttu-id="cd988-113">Décrit comment créer une implémentation personnalisée de l’interface <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cd988-113">Describes how to create a custom implementation of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cd988-114">La plupart des applications doivent utiliser l’implémentation de stock fournie par <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cd988-114">Most applications should use the stock implementation provided by <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span></span> <span data-ttu-id="cd988-115">Cette rubrique est destinée aux applications avec des exigences avancées.</span><span class="sxs-lookup"><span data-stu-id="cd988-115">This topic is for applications with advanced requirements.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd988-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Améliorations de la file d’attente de travail et du thread</a></span><span class="sxs-lookup"><span data-stu-id="cd988-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Work Queue and Threading Improvements</a></span></span></td>
<td><span data-ttu-id="cd988-117">Décrit les améliorations apportées à Windows 8 pour les files d’attente de travail et les threads dans la plateforme Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cd988-117">Describes improvements in Windows 8 for work queues and threading in the Media Foundation platform.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="cd988-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd988-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd988-119">API de plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cd988-119">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 




