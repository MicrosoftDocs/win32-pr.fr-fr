---
description: Résolution des problèmes
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Résolution des problèmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514937"
---
# <a name="troubleshooting"></a><span data-ttu-id="52354-103">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="52354-103">Troubleshooting</span></span>

<span data-ttu-id="52354-104">Si vous rencontrez des problèmes pour diagnostiquer les erreurs de votre application, reportez-vous aux conseils de dépannage suivants :</span><span class="sxs-lookup"><span data-stu-id="52354-104">If you are having trouble diagnosing your application errors, refer to the following of troubleshooting tips:</span></span>

-   <span data-ttu-id="52354-105">Assurez-vous que le Distributed Transaction Coordinator (DTC) est en cours d’exécution sur tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="52354-105">Make sure that the Distributed Transaction Coordinator (DTC) is running on all servers.</span></span>
-   <span data-ttu-id="52354-106">Vérifiez la communication réseau en commençant par le test sur un ordinateur local pour vérifier que l’application fonctionne.</span><span class="sxs-lookup"><span data-stu-id="52354-106">Check network communication by first testing on a local computer to verify that the application works.</span></span> <span data-ttu-id="52354-107">Si vous exécutez TCP/IP sur votre réseau, vous pouvez utiliser l’utilitaire ping.exe pour vérifier que les ordinateurs se trouvent sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="52354-107">If you are running TCP/IP on your network, you can use the ping.exe utility to verify that the machines are on the network.</span></span>
-   <span data-ttu-id="52354-108">Assurez-vous que SQL et DTC se trouvent sur le même ordinateur ou que le programme de configuration du client DTC spécifie que le DTC se trouve sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="52354-108">Make sure that SQL and DTC are located on the same computer or that the DTC Client Configuration program specifies that the DTC is on another computer.</span></span> <span data-ttu-id="52354-109">Si ce n’est pas le cas, SQLConnect renvoie une erreur en interne quand elle est appelée à partir d’un composant transactionnel.</span><span class="sxs-lookup"><span data-stu-id="52354-109">If not, SQLConnect will return an error internally when called from a transactional component.</span></span>
-   <span data-ttu-id="52354-110">Définissez le délai d’expiration de la transaction sur une valeur supérieure à la valeur par défaut de 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="52354-110">Set the transaction time-out to a higher number than the default 60 seconds.</span></span> <span data-ttu-id="52354-111">Une fois que le délai d’expiration de la transaction s’est écoulé, COM+ abandonne la transaction.</span><span class="sxs-lookup"><span data-stu-id="52354-111">After the transaction time-out has elapsed, COM+ aborts the transaction.</span></span> <span data-ttu-id="52354-112">Tous les appels suivants au composant sont immédiatement retournés avec le contexte \_ E \_ abandonné.</span><span class="sxs-lookup"><span data-stu-id="52354-112">All subsequent calls to the component return immediately with CONTEXT\_E\_ABORTED.</span></span>
-   <span data-ttu-id="52354-113">Assurez-vous que vos pilotes ODBC sont thread-safe et n’ont pas d’affinité de thread.</span><span class="sxs-lookup"><span data-stu-id="52354-113">Make sure that your ODBC drivers are thread-safe and do not have thread affinity.</span></span>
-   <span data-ttu-id="52354-114">Si vous avez des difficultés à faire fonctionner une application sur plusieurs serveurs, redémarrez le client, puis vérifiez que votre contrôleur de domaine est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="52354-114">If you have difficulty getting an application to work over several servers, reboot the client and then verify that your domain controller is configured properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52354-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52354-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52354-116">Isolation des erreurs et stratégie FailFast</span><span class="sxs-lookup"><span data-stu-id="52354-116">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="52354-117">Recherche de la source d’une erreur</span><span class="sxs-lookup"><span data-stu-id="52354-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="52354-118">Modification des valeurs de retour par COM+</span><span class="sxs-lookup"><span data-stu-id="52354-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="52354-119">Interprétation des codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="52354-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="52354-120">Stratégies de gestion des erreurs dans COM+</span><span class="sxs-lookup"><span data-stu-id="52354-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



