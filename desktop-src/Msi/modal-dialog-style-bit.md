---
description: Si ce bit est défini, la boîte de dialogue est modale, d’autres boîtes de dialogue de la même application ne peuvent pas être placées dessus et la boîte de dialogue garde le contrôle pendant son exécution.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit de style de boîte de dialogue modal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529751"
---
# <a name="modal-dialog-style-bit"></a><span data-ttu-id="274dd-103">Bit de style de boîte de dialogue modal</span><span class="sxs-lookup"><span data-stu-id="274dd-103">Modal Dialog Style Bit</span></span>

<span data-ttu-id="274dd-104">Si ce bit est défini, la boîte de dialogue est modale, d’autres boîtes de dialogue de la même application ne peuvent pas être placées dessus et la boîte de dialogue garde le contrôle pendant son exécution.</span><span class="sxs-lookup"><span data-stu-id="274dd-104">If this bit is set, the dialog box is modal, other dialogs of the same application cannot be put on top of it, and the dialog keeps the control while it is running.</span></span> <span data-ttu-id="274dd-105">Si ce bit n’est pas défini, la boîte de dialogue est non modale, d’autres boîtes de dialogue de la même application peuvent être déplacées dessus.</span><span class="sxs-lookup"><span data-stu-id="274dd-105">If this bit is not set, the dialog is modeless, other dialogs of the same application may be moved on top of it.</span></span> <span data-ttu-id="274dd-106">Après la création et l’affichage d’une boîte de dialogue non modale, l’interface utilisateur retourne le contrôle au programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="274dd-106">After a modeless dialog is created and displayed, the user interface returns control to the installer.</span></span> <span data-ttu-id="274dd-107">Le programme d’installation appelle ensuite l’interface utilisateur régulièrement pour mettre à jour la boîte de dialogue et lui permettre de traiter les messages.</span><span class="sxs-lookup"><span data-stu-id="274dd-107">The installer then calls the user interface periodically to update the dialog and to give it a chance to process the messages.</span></span> <span data-ttu-id="274dd-108">Dès que cette opération est effectuée, le contrôle est retourné au programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="274dd-108">As soon as this is done, the control is returned to the installer.</span></span>

> [!Note]  
> <span data-ttu-id="274dd-109">Il ne doit y avoir aucune boîte de dialogue non modale dans une séquence d’Assistant, étant donné que cela retournerait le contrôle au programme d’installation, mettant fin à la séquence de l’Assistant prématurément.</span><span class="sxs-lookup"><span data-stu-id="274dd-109">There should be no modeless dialogs in a wizard sequence, since this would return control to the installer, ending the wizard sequence prematurely.</span></span>

 

## <a name="value"></a><span data-ttu-id="274dd-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="274dd-110">Value</span></span>



| <span data-ttu-id="274dd-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="274dd-111">Decimal</span></span> | <span data-ttu-id="274dd-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="274dd-112">Hexadecimal</span></span> | <span data-ttu-id="274dd-113">Constante</span><span class="sxs-lookup"><span data-stu-id="274dd-113">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="274dd-114">2</span><span class="sxs-lookup"><span data-stu-id="274dd-114">2</span></span>       | <span data-ttu-id="274dd-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="274dd-115">0x00000002</span></span>  | <span data-ttu-id="274dd-116">**msidbDialogAttributesSysModal**</span><span class="sxs-lookup"><span data-stu-id="274dd-116">**msidbDialogAttributesSysModal**</span></span> |



 

 

 



