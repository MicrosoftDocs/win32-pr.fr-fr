---
description: Le processus de création d’une demande de certificat implique la collecte de certaines informations auprès du demandeur.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Création de la demande de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536966"
---
# <a name="creating-the-certificate-request"></a><span data-ttu-id="06bd0-103">Création de la demande de certificat</span><span class="sxs-lookup"><span data-stu-id="06bd0-103">Creating the Certificate Request</span></span>

<span data-ttu-id="06bd0-104">Le processus de création d’une demande de certificat implique la collecte de certaines informations auprès du demandeur.</span><span class="sxs-lookup"><span data-stu-id="06bd0-104">The process of creating a certificate request involves collecting certain information from the requester.</span></span> <span data-ttu-id="06bd0-105">En général, cette opération s’effectue par le biais d’une interface utilisateur, bien que les informations puissent être extraites directement d’une base de données sans avoir besoin d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="06bd0-105">Usually, this is done through some sort of user interface (UI), although the information could be taken directly from a database without the need for a UI.</span></span> <span data-ttu-id="06bd0-106">Le niveau d’information requis est défini par la stratégie de l' [*autorité de certification*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="06bd0-106">The level of information required is set by the policy of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="06bd0-107">Voici un exemple des informations requises :</span><span class="sxs-lookup"><span data-stu-id="06bd0-107">An example of the required information might be as follows:</span></span>

-   <span data-ttu-id="06bd0-108">Nom commun</span><span class="sxs-lookup"><span data-stu-id="06bd0-108">Common Name</span></span>
-   <span data-ttu-id="06bd0-109">Nom de l’unité</span><span class="sxs-lookup"><span data-stu-id="06bd0-109">Unit Name</span></span>
-   <span data-ttu-id="06bd0-110">Nom de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="06bd0-110">Company Name</span></span>
-   <span data-ttu-id="06bd0-111">City</span><span class="sxs-lookup"><span data-stu-id="06bd0-111">City</span></span>
-   <span data-ttu-id="06bd0-112">State</span><span class="sxs-lookup"><span data-stu-id="06bd0-112">State</span></span>
-   <span data-ttu-id="06bd0-113">Pays/région</span><span class="sxs-lookup"><span data-stu-id="06bd0-113">Country/Region</span></span>

> [!Note]  
> <span data-ttu-id="06bd0-114">L’interface est conçue pour effectuer une seule requête pour chaque instance de xenroll.</span><span class="sxs-lookup"><span data-stu-id="06bd0-114">The interface is designed to make a single request for each xenroll instance.</span></span> <span data-ttu-id="06bd0-115">Une instance xenroll distincte doit être créée pour créer chaque [*demande de certificat*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="06bd0-115">A separate xenroll instance must be created to create each [*certificate request*](../secgloss/c-gly.md).</span></span>

 

<span data-ttu-id="06bd0-116">Pour plus d’informations sur l’utilisation du contrôle d’inscription de certificats pour demander un certificat dans des langages de programmation spécifiques, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="06bd0-116">For information about how to use the Certificate Enrollment Control to request a certificate in specific programming languages, see the following topics:</span></span>

-   [<span data-ttu-id="06bd0-117">Exemple de demande en C++</span><span class="sxs-lookup"><span data-stu-id="06bd0-117">Request Sample in C++</span></span>](request-sample-in-c-.md)
-   [<span data-ttu-id="06bd0-118">Exemple de demande dans VBScript</span><span class="sxs-lookup"><span data-stu-id="06bd0-118">Request Sample in VBScript</span></span>](request-sample-in-vbscript.md)

 

 
