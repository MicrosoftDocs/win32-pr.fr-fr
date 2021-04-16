---
description: Explique comment les services de certificats traitent les demandes de certificat.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Traitement des demandes de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570960"
---
# <a name="processing-certificate-requests"></a><span data-ttu-id="24d55-103">Traitement des demandes de certificat</span><span class="sxs-lookup"><span data-stu-id="24d55-103">Processing Certificate Requests</span></span>

<span data-ttu-id="24d55-104">Les services de certificats effectuent les étapes suivantes lors du traitement d’une [*demande de certificat*](../secgloss/c-gly.md):</span><span class="sxs-lookup"><span data-stu-id="24d55-104">Certificate Services performs the following steps when processing a [*certificate request*](../secgloss/c-gly.md):</span></span>

1.  <span data-ttu-id="24d55-105">Réception de la demande.</span><span class="sxs-lookup"><span data-stu-id="24d55-105">Request reception.</span></span>

    <span data-ttu-id="24d55-106">La [*demande de certificat*](../secgloss/c-gly.md) est envoyée par le client à une application intermédiaire, qui la formate dans une \# demande de format PKCS 10 et l’envoie au moteur serveur.</span><span class="sxs-lookup"><span data-stu-id="24d55-106">The [*certificate request*](../secgloss/c-gly.md) is sent by the client to an intermediary application, which formats it into a PKCS \#10 format request and submits it to the server engine.</span></span>

2.  <span data-ttu-id="24d55-107">Approbation de la demande.</span><span class="sxs-lookup"><span data-stu-id="24d55-107">Request approval.</span></span>

    <span data-ttu-id="24d55-108">Le moteur de serveur appelle le [module de stratégie](policy-modules.md), qui interroge les propriétés de demande, détermine si la demande est autorisée ou non, et définit les propriétés de certificat facultatives.</span><span class="sxs-lookup"><span data-stu-id="24d55-108">The server engine calls the [Policy Module](policy-modules.md), which queries request properties, decides whether the request is authorized or not, and sets optional certificate properties.</span></span>

3.  <span data-ttu-id="24d55-109">La formation des certificats.</span><span class="sxs-lookup"><span data-stu-id="24d55-109">Certificate formation.</span></span>

    <span data-ttu-id="24d55-110">Si la demande est approuvée, le moteur de serveur prend la demande, ainsi que toutes les propriétés demandées par le module de stratégie, et crée un certificat complet.</span><span class="sxs-lookup"><span data-stu-id="24d55-110">If the request is approved, the server engine takes the request, and any properties requested by the Policy Module, and builds a complete certificate.</span></span>

4.  <span data-ttu-id="24d55-111">Publication du certificat.</span><span class="sxs-lookup"><span data-stu-id="24d55-111">Certificate publication.</span></span>

    <span data-ttu-id="24d55-112">Le moteur du serveur stocke le certificat terminé dans la base de données des services de certificats et notifie l’application intermédiaire de l’état de la demande.</span><span class="sxs-lookup"><span data-stu-id="24d55-112">The server engine stores the completed certificate in the Certificate Services database and notifies the intermediary application of the request status.</span></span> <span data-ttu-id="24d55-113">Si le [module de sortie](exit-modules.md) l’a demandé, le moteur du serveur l’avertit d’un événement d’émission de certificat.</span><span class="sxs-lookup"><span data-stu-id="24d55-113">If the [exit module](exit-modules.md) has so requested, the server engine will notify it of a certificate issuance event.</span></span> <span data-ttu-id="24d55-114">Cela permet au module de sortie d’effectuer d’autres opérations, telles que la publication du certificat sur un référentiel de certificats externe (par exemple, un service d’annuaire).</span><span class="sxs-lookup"><span data-stu-id="24d55-114">This allows the exit module to perform further operations such as publishing the certificate to an external certificate repository (for example, a directory service).</span></span> <span data-ttu-id="24d55-115">Pendant ce temps, l’intermédiaire récupère le certificat publié auprès des services de certificats et le transmet au client.</span><span class="sxs-lookup"><span data-stu-id="24d55-115">Meanwhile, the intermediary gets the published certificate from Certificate Services and passes it back to the client.</span></span>

<span data-ttu-id="24d55-116">L’illustration suivante montre comment une [*demande de certificat*](../secgloss/c-gly.md) est traitée par les services de certificats.</span><span class="sxs-lookup"><span data-stu-id="24d55-116">The following illustration shows how a [*certificate request*](../secgloss/c-gly.md) is processed by Certificate Services.</span></span>

![traitement d’une demande de certificat](images/certflow.png)

 

 
