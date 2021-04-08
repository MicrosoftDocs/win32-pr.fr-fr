---
description: L’action de publication est une action de niveau supérieur appelée pour installer ou supprimer des composants publiés.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Action de publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756244"
---
# <a name="advertise-action"></a><span data-ttu-id="a1a28-103">Action de publication</span><span class="sxs-lookup"><span data-stu-id="a1a28-103">ADVERTISE Action</span></span>

<span data-ttu-id="a1a28-104">L’action de publication est une action de niveau supérieur appelée pour installer ou supprimer des composants publiés.</span><span class="sxs-lookup"><span data-stu-id="a1a28-104">The ADVERTISE action is a top-level action called to install or remove advertised components.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a1a28-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="a1a28-105">Sequence Restrictions</span></span>

<span data-ttu-id="a1a28-106">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="a1a28-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a1a28-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="a1a28-107">ActionData Messages</span></span>

<span data-ttu-id="a1a28-108">Il n’y a aucun message ActionData.</span><span class="sxs-lookup"><span data-stu-id="a1a28-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1a28-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a1a28-109">Remarks</span></span>

<span data-ttu-id="a1a28-110">La [*publication*](a-gly.md) fait référence à la capacité du programme d’installation à fournir les interfaces de chargement et de lancement d’une application sans installer physiquement l’application.</span><span class="sxs-lookup"><span data-stu-id="a1a28-110">[*Advertising*](a-gly.md) refers to the installer's ability to provide the loading and launching interfaces of an application without physically installing the application.</span></span> <span data-ttu-id="a1a28-111">Le programme d’installation n’installe pas les composants nécessaires tant qu’un utilisateur ou une application n’a pas activé une interface publiée.</span><span class="sxs-lookup"><span data-stu-id="a1a28-111">The installer does not install the necessary components until a user or application activates an advertised interface.</span></span> <span data-ttu-id="a1a28-112">Ce concept est appelé [*Install-on-demand*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a1a28-112">This concept is called [*install-on-demand*](i-gly.md).</span></span>

<span data-ttu-id="a1a28-113">L’action de publication n’est pas appelée à partir de la séquence de la table d’action, le Windows Installer exécute cette action lorsque l’exécutable de ligne de commande Msiexec.exe est appelé avec le commutateur de ligne de commande'/j’ou lorsque [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) est appelé avec le paramètre *SZCOMMANDLINE* défini sur action = advertise.</span><span class="sxs-lookup"><span data-stu-id="a1a28-113">The ADVERTISE action is not called from within the action table sequence, the Windows Installer executes this action when the command line executable Msiexec.exe is called with the '/j' command line switch or when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to ACTION=ADVERTISE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1a28-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1a28-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1a28-115">Table AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="a1a28-115">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)
</dt> </dl>

 

 



