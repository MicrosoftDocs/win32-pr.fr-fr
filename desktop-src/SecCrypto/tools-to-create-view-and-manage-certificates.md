---
description: Les outils CryptoAPI sont des outils permettant d’effectuer des tâches courantes de gestion des certificats.
ms.assetid: 29146de8-adae-444b-bc75-fa43a19ab8f9
title: Outils pour créer, afficher et gérer des certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fb4595b7c7711b10271bd97a447a77f3a01c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759622"
---
# <a name="tools-to-create-view-and-manage-certificates"></a><span data-ttu-id="e7331-103">Outils pour créer, afficher et gérer des certificats</span><span class="sxs-lookup"><span data-stu-id="e7331-103">Tools to Create, View, and Manage Certificates</span></span>

<span data-ttu-id="e7331-104">Les outils CryptoAPI sont des outils permettant d’effectuer des tâches courantes de gestion des certificats.</span><span class="sxs-lookup"><span data-stu-id="e7331-104">CryptoAPI Tools are tools to perform common certificate management tasks.</span></span>



| <span data-ttu-id="e7331-105">Outil</span><span class="sxs-lookup"><span data-stu-id="e7331-105">Tool</span></span>                                | <span data-ttu-id="e7331-106">Notes</span><span class="sxs-lookup"><span data-stu-id="e7331-106">Remarks</span></span>                                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7331-107">MakeCert</span><span class="sxs-lookup"><span data-stu-id="e7331-107">MakeCert</span></span>](makecert.md)<br/> | <span data-ttu-id="e7331-108">Crée un certificat [*X. 509*](../secgloss/x-gly.md) de test.</span><span class="sxs-lookup"><span data-stu-id="e7331-108">Creates a test [*X.509*](../secgloss/x-gly.md) certificate.</span></span><br/>                                                                                |
| [<span data-ttu-id="e7331-109">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="e7331-109">Cert2SPC</span></span>](cert2spc.md)<br/> | <span data-ttu-id="e7331-110">Crée un certificat SPC (test [*Software Publisher Certificate*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="e7331-110">Creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC).</span></span><br/>           |
| [<span data-ttu-id="e7331-111">CertMgr</span><span class="sxs-lookup"><span data-stu-id="e7331-111">CertMgr</span></span>](certmgr.md)<br/>   | <span data-ttu-id="e7331-112">Gère les certificats, les listes CTL et les [*listes de révocation de certificats*](../secgloss/c-gly.md) (CRL).</span><span class="sxs-lookup"><span data-stu-id="e7331-112">Manages certificates, CTLs, and [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs).</span></span><br/> |



 

<span data-ttu-id="e7331-113">Toutes les entrées d’utilisateur de ces outils ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="e7331-113">All user input to these tools is case insensitive.</span></span> <span data-ttu-id="e7331-114">Des options distinctes existent maintenant pour le nom de la [*paire de clés*](../secgloss/k-gly.md) et le fichier de [*clé privée*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e7331-114">Separate options now exist for the [*key pair*](../secgloss/k-gly.md) name and the [*private key*](../secgloss/p-gly.md) file.</span></span>

## <a name="additional-tools"></a><span data-ttu-id="e7331-115">Outils supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e7331-115">Additional Tools</span></span>

<span data-ttu-id="e7331-116">Certutil.exe est un outil en ligne de commande installé dans le cadre des services de certificats.</span><span class="sxs-lookup"><span data-stu-id="e7331-116">Certutil.exe is a command-line tool that is installed as part of Certificate Services.</span></span> <span data-ttu-id="e7331-117">Vous pouvez utiliser Certutil.exe pour vider et afficher les informations de configuration de l' [*autorité de certification*](../secgloss/c-gly.md) , configurer les services de certificats, sauvegarder et restaurer les composants de l’autorité de certification et vérifier les [*certificats*](../secgloss/c-gly.md), les [*paires de clés*](../secgloss/k-gly.md)et les chaînes de certificats.</span><span class="sxs-lookup"><span data-stu-id="e7331-117">You can use Certutil.exe to dump and display [*certification authority*](../secgloss/c-gly.md) (CA) configuration information, configure Certificate Services, back up and restore CA components, and verify [*certificates*](../secgloss/c-gly.md), [*key pairs*](../secgloss/k-gly.md), and certificate chains.</span></span> <span data-ttu-id="e7331-118">Pour plus d’informations sur certutil, consultez la rubrique [certutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732443(v=ws.11)) sur Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="e7331-118">For more information about Certutil, see the [Certutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732443(v=ws.11)) topic on Microsoft TechNet.</span></span>

 

 
