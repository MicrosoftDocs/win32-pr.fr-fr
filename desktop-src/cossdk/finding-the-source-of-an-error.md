---
description: Recherche de la source d’une erreur
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Recherche de la source d’une erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033755"
---
# <a name="finding-the-source-of-an-error"></a><span data-ttu-id="0749a-103">Recherche de la source d’une erreur</span><span class="sxs-lookup"><span data-stu-id="0749a-103">Finding the Source of an Error</span></span>

<span data-ttu-id="0749a-104">Vous pouvez diagnostiquer la source et obtenir une description des erreurs d’application à l’aide de COM+ et d’autres outils.</span><span class="sxs-lookup"><span data-stu-id="0749a-104">You can diagnose the source and obtain a description of application errors by using COM+ and other tools.</span></span> <span data-ttu-id="0749a-105">Si vous découvrez que l’erreur d’application est provoquée par COM+, vous pouvez interpréter le message d’erreur qui affiche le fichier winerror. h ou à l’aide de l’utilitaire Microsoft Visual C++ Error.</span><span class="sxs-lookup"><span data-stu-id="0749a-105">If you discover that the application error is caused by COM+, you can interpret the error message viewing the Winerror.h file or by using the Microsoft Visual C++ error utility.</span></span>

<span data-ttu-id="0749a-106">Si votre application serveur échoue ou provoque un comportement inattendu, vous devez d’abord déterminer l’emplacement où l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0749a-106">If your server application is failing or causing unexpected behavior, you must first determine where the error occurred.</span></span> <span data-ttu-id="0749a-107">Le système observateur d’événements effectue le suivi des événements de l’application, de la sécurité et du système.</span><span class="sxs-lookup"><span data-stu-id="0749a-107">The system Event Viewer tracks application, security, and system events.</span></span> <span data-ttu-id="0749a-108">De nombreuses erreurs « silencieuses » sont enregistrées ici.</span><span class="sxs-lookup"><span data-stu-id="0749a-108">Many "silent" errors are recorded here.</span></span> <span data-ttu-id="0749a-109">Toutefois, toutes les erreurs ne sont pas affichées dans la observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="0749a-109">However, not all errors are shown in the Event Viewer.</span></span>

<span data-ttu-id="0749a-110">Vous devez d’abord faire référence au journal des applications dans le observateur d’événements pour vérifier l’application associée au message d’événement.</span><span class="sxs-lookup"><span data-stu-id="0749a-110">You should first refer to the application log in the Event Viewer to check the application associated with the event message.</span></span> <span data-ttu-id="0749a-111">(Étant donné que vous pouvez également archiver les journaux des événements, vous pouvez suivre l’historique des événements de l’erreur.) Double-cliquez sur une entrée dans votre journal pour activer une page de **propriétés d’événement** qui fournit des informations supplémentaires sur l’événement système.</span><span class="sxs-lookup"><span data-stu-id="0749a-111">(Because you can also archive event logs, you can track an event history of the error.) Double-clicking an entry in your log activates an **Event Properties** page, which provides further information about the system event.</span></span>

<span data-ttu-id="0749a-112">Pour plus d’informations sur le débogage d’une application COM+, consultez [débogage d’applications com+](debugging-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="0749a-112">For more information on debugging a COM+ application, see [Debugging COM+ Applications](debugging-com--applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0749a-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0749a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0749a-114">Isolation des erreurs et stratégie FailFast</span><span class="sxs-lookup"><span data-stu-id="0749a-114">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="0749a-115">Modification des valeurs de retour par COM+</span><span class="sxs-lookup"><span data-stu-id="0749a-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="0749a-116">Interprétation des codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0749a-116">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="0749a-117">Stratégies de gestion des erreurs dans COM+</span><span class="sxs-lookup"><span data-stu-id="0749a-117">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="0749a-118">Dépannage</span><span class="sxs-lookup"><span data-stu-id="0749a-118">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



