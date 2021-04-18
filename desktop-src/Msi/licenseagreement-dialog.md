---
description: Cette boîte de dialogue modale affiche le contrat de licence pour l’utilisateur.
ms.assetid: 367fe264-6e08-4b40-b61b-617bb92986b7
title: Boîte de dialogue LicenseAgreement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8876f315787671ee36de42e5b86167659611a77a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512980"
---
# <a name="licenseagreement-dialog"></a><span data-ttu-id="9fbfd-103">Boîte de dialogue LicenseAgreement</span><span class="sxs-lookup"><span data-stu-id="9fbfd-103">LicenseAgreement Dialog</span></span>

<span data-ttu-id="9fbfd-104">Cette boîte de dialogue modale affiche le contrat de licence pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9fbfd-104">This modal dialog box displays the license agreement to the user.</span></span> <span data-ttu-id="9fbfd-105">En général, la boîte de dialogue affiche le texte de l’accord à l’aide d’un [contrôle ScrollableText](scrollabletext-control.md) et d’une paire de cases d’option qui permettent à l’utilisateur d’accepter ou de refuser le contrat.</span><span class="sxs-lookup"><span data-stu-id="9fbfd-105">Typically the dialog box displays the text of the agreement using a [ScrollableText control](scrollabletext-control.md) and a pair of option buttons that let the user accept or reject the agreement.</span></span> <span data-ttu-id="9fbfd-106">Pour des raisons juridiques, il est recommandé qu’aucun bouton ne soit présenté à l’utilisateur, comme déjà sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="9fbfd-106">For legal reasons it is advisable that neither button be presented to the user as already selected by default.</span></span> <span data-ttu-id="9fbfd-107">Cela oblige l’utilisateur à faire un choix actif.</span><span class="sxs-lookup"><span data-stu-id="9fbfd-107">This forces the user to make an active choice.</span></span> <span data-ttu-id="9fbfd-108">Les auteurs utilisent généralement un [contrôle RadioButtonGroup](radiobuttongroup-control.md) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="9fbfd-108">Authors commonly use a [RadioButtonGroup control](radiobuttongroup-control.md) for this purpose.</span></span> <span data-ttu-id="9fbfd-109">Notez cependant que le focus sur une boîte de dialogue n’est pas déplacé vers un contrôle RadioButtonGroup tant que l’un des boutons du groupe n’a pas été sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9fbfd-109">Note however that the focus on a dialog box does not move to a RadioButtonGroup control until one of the buttons in the group has been selected.</span></span>

 

 



