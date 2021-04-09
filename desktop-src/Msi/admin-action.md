---
description: L’action d’administration est une action de niveau supérieur qui permet d’effectuer des installations administratives.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Action d’administration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864509"
---
# <a name="admin-action"></a><span data-ttu-id="eeb72-103">Action d’administration</span><span class="sxs-lookup"><span data-stu-id="eeb72-103">ADMIN Action</span></span>

<span data-ttu-id="eeb72-104">L’action d’administration est une action de niveau supérieur qui permet d’effectuer des [installations administratives](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="eeb72-104">The ADMIN action is a top-level action used to perform [administrative installations](administrative-installation.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="eeb72-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="eeb72-105">Sequence Restrictions</span></span>

<span data-ttu-id="eeb72-106">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="eeb72-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="eeb72-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="eeb72-107">ActionData Messages</span></span>

<span data-ttu-id="eeb72-108">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="eeb72-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeb72-109">Notes</span><span class="sxs-lookup"><span data-stu-id="eeb72-109">Remarks</span></span>

<span data-ttu-id="eeb72-110">L’action d’administration n’est pas appelée à partir de la séquence de la table d’action, Windows Installer exécute cette action lorsque [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) est appelé avec le paramètre *szCommandLine* défini sur « action = admin » ou l’exécutable de ligne de commande Msiexec.exe est appelé avec le commutateur de ligne de commande « /a ».</span><span class="sxs-lookup"><span data-stu-id="eeb72-110">The ADMIN action is not called from within the action table sequence, Windows Installer executes this action when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to "ACTION=ADMIN" or the command line executable Msiexec.exe is called with the '/a' command line switch.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeb72-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eeb72-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb72-112">Table AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="eeb72-112">AdminUISequence Table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="eeb72-113">Table AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="eeb72-113">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)
</dt> </dl>

 

 



