---
description: Gestion des erreurs dans le CRM COM+
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Gestion des erreurs dans le CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483449"
---
# <a name="error-handling-in-the-com-crm"></a><span data-ttu-id="d17c2-103">Gestion des erreurs dans le CRM COM+</span><span class="sxs-lookup"><span data-stu-id="d17c2-103">Error Handling in the COM+ CRM</span></span>

<span data-ttu-id="d17c2-104">Les applications serveur COM+ implémentent une stratégie FailFast.</span><span class="sxs-lookup"><span data-stu-id="d17c2-104">COM+ server applications implement a failfast policy.</span></span> <span data-ttu-id="d17c2-105">Si une erreur interne grave est détectée, le processus de l’application serveur se termine et écrit un message d’erreur dans le journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="d17c2-105">If a serious internal error is detected, the server application process exits and writes an error message to the Windows event log.</span></span> <span data-ttu-id="d17c2-106">Cela permet de détecter rapidement les problèmes et est possible en raison de la protection des données d’application par le traitement des transactions.</span><span class="sxs-lookup"><span data-stu-id="d17c2-106">This allows quick detection of problems and is possible due to the protection of application data by transaction processing.</span></span> <span data-ttu-id="d17c2-107">Recherchez toujours dans le journal des événements Windows les erreurs de CRM, soit pendant le développement, soit pendant le déploiement final.</span><span class="sxs-lookup"><span data-stu-id="d17c2-107">Always check the Windows event log for any errors from the CRM, either during development or during final deployment.</span></span>

<span data-ttu-id="d17c2-108">Les erreurs de base dans l’utilisation des interfaces CRM, telles que les arguments non valides ou les erreurs de séquence (par exemple, la tentative d’écriture d’un enregistrement de journal avant l’inscription du compensateur CRM), renvoient des codes d’erreur et ne doivent pas déclencher FailFast.</span><span class="sxs-lookup"><span data-stu-id="d17c2-108">Basic errors in using the CRM interfaces, such as invalid arguments or sequence errors (for example, trying to write a log record before registering the CRM Compensator), return error codes and should not trigger failfast.</span></span> <span data-ttu-id="d17c2-109">Pour le développement CRM, vous pouvez choisir de définir la clé de Registre VTRACE1 (voir [paramètres du Registre CRM CRM](com--crm-registry-settings.md)), ce qui entraîne l’affichage d’un message dans la fenêtre sortie du débogueur pour chaque erreur.</span><span class="sxs-lookup"><span data-stu-id="d17c2-109">For CRM development, you may choose to set the VTRACE1 registry key (see [COM+ CRM Registry Settings](com--crm-registry-settings.md)), which causes a message to appear in the debugger output window for each error.</span></span>

<span data-ttu-id="d17c2-110">Des erreurs temporaires peuvent également se produire.</span><span class="sxs-lookup"><span data-stu-id="d17c2-110">Transient errors can also occur.</span></span> <span data-ttu-id="d17c2-111">Ces erreurs sont généralement dues à des conditions de synchronisation et entraînent le renvoi d’un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d17c2-111">These errors are typically caused by timing conditions and result in an error code being returned.</span></span> <span data-ttu-id="d17c2-112">Le développeur CRM doit s’assurer que ces conditions d’erreur sont gérées.</span><span class="sxs-lookup"><span data-stu-id="d17c2-112">The CRM developer should ensure that these error conditions are handled.</span></span> <span data-ttu-id="d17c2-113">Par exemple, lors de l’écriture d’un enregistrement de journal, la transaction peut être abandonnée en raison d’un délai d’attente. La méthode retourne ensuite une erreur, que l’appelant doit vérifier et gérer de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="d17c2-113">For example, while writing a log record, the transaction could abort due to a time-out. The method then returns an error, which the caller should check for and handle appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d17c2-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d17c2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d17c2-115">Concepts de Gestionnaire des ressources de compensation COM+</span><span class="sxs-lookup"><span data-stu-id="d17c2-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



