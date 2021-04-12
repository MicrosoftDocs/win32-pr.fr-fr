---
description: Le programme d’installation stocke toutes les informations relatives à l’interface utilisateur dans les tables de la base de données d’installation.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Aperçu de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203195"
---
# <a name="previewing-the-user-interface"></a><span data-ttu-id="fbca2-103">Aperçu de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="fbca2-103">Previewing the User Interface</span></span>

<span data-ttu-id="fbca2-104">Le programme d’installation stocke toutes les informations relatives à l' [interface utilisateur](user-interface.md) dans les tables de la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="fbca2-104">The installer stores all information about the [user interface](user-interface.md) in the tables of the installation database.</span></span> <span data-ttu-id="fbca2-105">Pour faciliter la conception de l’interface utilisateur, le programme d’installation fournit également un mode d’aperçu pour afficher ces informations.</span><span class="sxs-lookup"><span data-stu-id="fbca2-105">To facilitate the design of the UI the installer also provides a preview mode for viewing this information.</span></span> <span data-ttu-id="fbca2-106">La procédure suivante décrit comment activer le mode aperçu de l’interface utilisateur et afficher l’apparence actuelle des boîtes de dialogue et des panneaux.</span><span class="sxs-lookup"><span data-stu-id="fbca2-106">The following procedure describes how to enable the UI preview mode and display the current appearance of dialog boxes and billboards.</span></span>

<span data-ttu-id="fbca2-107">**Pour afficher l’interface utilisateur en mode aperçu**</span><span class="sxs-lookup"><span data-stu-id="fbca2-107">**To view the user interface in the preview mode**</span></span>

1.  <span data-ttu-id="fbca2-108">Activez le mode aperçu en appelant la fonction [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) .</span><span class="sxs-lookup"><span data-stu-id="fbca2-108">Enable the preview mode by calling the [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) function.</span></span>
2.  <span data-ttu-id="fbca2-109">Affichez les boîtes de dialogue particulières en appelant la fonction [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) .</span><span class="sxs-lookup"><span data-stu-id="fbca2-109">Display the particular dialog boxes by calling the [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) function.</span></span>
3.  <span data-ttu-id="fbca2-110">Affichez des panneaux d’affichage particuliers en appelant la fonction [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) .</span><span class="sxs-lookup"><span data-stu-id="fbca2-110">Display particular billboards by calling the [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) function.</span></span>

 

 



