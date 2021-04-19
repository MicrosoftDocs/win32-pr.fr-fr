---
description: La classe CMsgThread fournit la prise en charge d’un thread de travail auquel les demandes peuvent être publiées de manière asynchrone au lieu d’être envoyées directement.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: CMsg, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514089"
---
# <a name="cmsg-class"></a><span data-ttu-id="0e759-103">CMsg, classe</span><span class="sxs-lookup"><span data-stu-id="0e759-103">CMsg class</span></span>

<span data-ttu-id="0e759-104">La classe [**CMsgThread**](cmsgthread.md) fournit la prise en charge d’un thread de travail auquel les demandes peuvent être publiées de manière asynchrone au lieu d’être envoyées directement.</span><span class="sxs-lookup"><span data-stu-id="0e759-104">The [**CMsgThread**](cmsgthread.md) class provides support for a worker thread to which requests can be posted asynchronously instead of sent directly.</span></span> <span data-ttu-id="0e759-105">La classe [**CAMThread**](camthread.md) fournit un thread de travail auquel les demandes uniques peuvent être envoyées.</span><span class="sxs-lookup"><span data-stu-id="0e759-105">The [**CAMThread**](camthread.md) class provides a worker thread to which single requests can be sent.</span></span> <span data-ttu-id="0e759-106">Un seul client peut effectuer une demande à la fois et le client se bloque jusqu’à ce que le thread de travail ait terminé la demande.</span><span class="sxs-lookup"><span data-stu-id="0e759-106">Only one client can make a request at a time, and the client blocks until the worker thread has completed the request.</span></span> <span data-ttu-id="0e759-107">En revanche, la classe **CMsgThread** fournit un thread de travail sur lequel n’importe quel nombre de demandes peut être publié.</span><span class="sxs-lookup"><span data-stu-id="0e759-107">By contrast, the **CMsgThread** class provides a worker thread to which any number of requests can be posted.</span></span> <span data-ttu-id="0e759-108">Les requêtes (sous la forme d’un `CMsg` objet) sont mises en file d’attente et exécutées dans l’ordre, de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0e759-108">The requests (in the form of a `CMsg` object) are queued and executed in order, asynchronously.</span></span> <span data-ttu-id="0e759-109">Aucune réponse ou valeur de retour n’est reçue.</span><span class="sxs-lookup"><span data-stu-id="0e759-109">No reply or return value is received.</span></span>



| <span data-ttu-id="0e759-110">Données membres</span><span class="sxs-lookup"><span data-stu-id="0e759-110">Data Members</span></span>              | <span data-ttu-id="0e759-111">Description</span><span class="sxs-lookup"><span data-stu-id="0e759-111">Description</span></span>                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e759-112">dwFlags</span><span class="sxs-lookup"><span data-stu-id="0e759-112">dwFlags</span></span>                   | <span data-ttu-id="0e759-113">Paramètre d’indicateur pour le code de la requête.</span><span class="sxs-lookup"><span data-stu-id="0e759-113">Flag parameter to the request code.</span></span>                                                                                                                                               |
| <span data-ttu-id="0e759-114">lpParam</span><span class="sxs-lookup"><span data-stu-id="0e759-114">lpParam</span></span>                   | <span data-ttu-id="0e759-115">Données requises par le thread de travail comme valeurs de paramètre ou de retour.</span><span class="sxs-lookup"><span data-stu-id="0e759-115">Data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="0e759-116">Ces données ne doivent pas être basées sur la pile, car elles seront référencées un peu plus tard après la fin de l’opération de mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="0e759-116">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span> |
| <span data-ttu-id="0e759-117">pEvent</span><span class="sxs-lookup"><span data-stu-id="0e759-117">pEvent</span></span>                    | <span data-ttu-id="0e759-118">Objet d’événement qu’un thread de travail peut signaler pour indiquer l’achèvement de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0e759-118">Event object that a worker thread can signal to indicate the completion of the operation.</span></span>                                                                                         |
| <span data-ttu-id="0e759-119">uMsg</span><span class="sxs-lookup"><span data-stu-id="0e759-119">uMsg</span></span>                      | <span data-ttu-id="0e759-120">Code de requête défini par le client de la classe thread et compris par la fonction de thread de travail remplacée.</span><span class="sxs-lookup"><span data-stu-id="0e759-120">Request code that is defined by the client of the thread class and understood by the overridden worker thread function.</span></span>                                                           |
| <span data-ttu-id="0e759-121">Fonctions de membre</span><span class="sxs-lookup"><span data-stu-id="0e759-121">Member Functions</span></span>          | <span data-ttu-id="0e759-122">Description</span><span class="sxs-lookup"><span data-stu-id="0e759-122">Description</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="0e759-123">**CMsg**</span><span class="sxs-lookup"><span data-stu-id="0e759-123">**CMsg**</span></span>](cmsg-cmsg.md) | <span data-ttu-id="0e759-124">Construit un objet [**CMsg**](cmsg-cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="0e759-124">Constructs a [**CMsg**](cmsg-cmsg.md) object.</span></span>                                                                                                                                    |



 

 

 



