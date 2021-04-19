---
description: Améliorations futures de l’exemple de code d’application Winsock.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Améliorations futures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516464"
---
# <a name="future-improvements"></a><span data-ttu-id="c86a4-103">Améliorations futures</span><span class="sxs-lookup"><span data-stu-id="c86a4-103">Future Improvements</span></span>

<span data-ttu-id="c86a4-104">Plusieurs améliorations peuvent être apportées à cette application, par exemple :</span><span class="sxs-lookup"><span data-stu-id="c86a4-104">There are several improvements that can be made to this application, such as:</span></span>

-   <span data-ttu-id="c86a4-105">Une seule connexion permanente peut être créée par l’application.</span><span class="sxs-lookup"><span data-stu-id="c86a4-105">A single, persistent connection could be created by the application.</span></span> <span data-ttu-id="c86a4-106">La gestion des erreurs appropriée devrait être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="c86a4-106">Appropriate error handling would have to be added.</span></span> <span data-ttu-id="c86a4-107">Cela réduirait la surcharge associée au démarrage et à la destruction de la connexion.</span><span class="sxs-lookup"><span data-stu-id="c86a4-107">This would reduce the overhead associated with connection startup and teardown.</span></span>
-   <span data-ttu-id="c86a4-108">Le code de réponse sur le serveur peut être optimisé pour consolider les réponses, ce qui réduit le nombre de paquets envoyés à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="c86a4-108">The reply code on the server could be optimized to consolidate replies, reducing the number of packets sent from the server.</span></span>
-   <span data-ttu-id="c86a4-109">Des améliorations ont été apportées au protocole.</span><span class="sxs-lookup"><span data-stu-id="c86a4-109">Improvements in the protocol could be made.</span></span> <span data-ttu-id="c86a4-110">Par exemple, un masque de mise à jour peut être utilisé pour indiquer les cellules à mettre à jour et uniquement les données de cette cellule envoyées.</span><span class="sxs-lookup"><span data-stu-id="c86a4-110">For example, an update bitmask could be used to signify which cells are to be updated, and only that cell data sent.</span></span>
-   <span data-ttu-id="c86a4-111">Les mises à jour peuvent être superposées à l’aide de différents threads, afin que le réseau ne soit pas inactif pendant l’exécution de la fonction **ComputeNext** .</span><span class="sxs-lookup"><span data-stu-id="c86a4-111">Updates could be overlapped using different threads, so that the network is not idle while the **ComputeNext** function is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c86a4-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c86a4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c86a4-113">Amélioration d’une application lente</span><span class="sxs-lookup"><span data-stu-id="c86a4-113">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="c86a4-114">Version de référence : une application très médiocre</span><span class="sxs-lookup"><span data-stu-id="c86a4-114">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="c86a4-115">Révision 1 : nettoyage évident</span><span class="sxs-lookup"><span data-stu-id="c86a4-115">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="c86a4-116">Révision 2 : reconception pour des connexions moins nombreuses</span><span class="sxs-lookup"><span data-stu-id="c86a4-116">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="c86a4-117">Révision 3 : envoi de bloc compressé</span><span class="sxs-lookup"><span data-stu-id="c86a4-117">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



