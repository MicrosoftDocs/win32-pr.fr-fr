---
description: Ce document est destiné aux développeurs qui écrivent leurs propres programmes d’installation qui souhaitent en savoir plus sur les tables de base de données Windows Installer. Pour obtenir des informations générales, consultez à propos de Windows Installer.
ms.assetid: c4bedc0e-cd1a-4cdc-8dd1-4a774aaf533e
title: Flux d’informations de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd9d6792249433c4200a8e68515fbfeb409b390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529693"
---
# <a name="summary-information-stream"></a><span data-ttu-id="b2e9a-104">Flux d’informations de synthèse</span><span class="sxs-lookup"><span data-stu-id="b2e9a-104">Summary Information Stream</span></span>

<span data-ttu-id="b2e9a-105">Ce document est destiné aux développeurs qui écrivent leurs propres programmes d’installation qui souhaitent en savoir plus sur les tables de base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b2e9a-105">The material in this section is intended for developers who are writing their own setup programs who want to learn more about Windows Installer database tables.</span></span> <span data-ttu-id="b2e9a-106">Pour obtenir des informations générales, consultez [à propos de Windows Installer](about-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="b2e9a-106">For general information, see [About Windows Installer](about-windows-installer.md).</span></span>

<span data-ttu-id="b2e9a-107">Le flux d’informations de résumé est utilisé par le programme d’installation pour deux raisons.</span><span class="sxs-lookup"><span data-stu-id="b2e9a-107">The summary information stream is used by the installer for two purposes.</span></span> <span data-ttu-id="b2e9a-108">Tout d’abord, il contient des informations sur le package qui peuvent être consultées par le biais de l’Explorateur Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b2e9a-108">First, it contains information about the package that can be viewed through Microsoft Windows Explorer.</span></span> <span data-ttu-id="b2e9a-109">Ces informations sont accessibles via l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="b2e9a-109">This information is accessible through the **IStream** interface.</span></span> <span data-ttu-id="b2e9a-110">Deuxièmement, il contient les propriétés utilisées par le programme d’installation pour installer le package.</span><span class="sxs-lookup"><span data-stu-id="b2e9a-110">Second, it contains properties that are used by the installer to install the package.</span></span> <span data-ttu-id="b2e9a-111">Les rubriques suivantes fournissent des informations sur l’utilisation du flux d’informations résumées avec le programme d’installation :</span><span class="sxs-lookup"><span data-stu-id="b2e9a-111">The following topics provide information about how to use the summary information stream with the installer:</span></span>

-   [<span data-ttu-id="b2e9a-112">À propos du flux d’informations de synthèse</span><span class="sxs-lookup"><span data-stu-id="b2e9a-112">About the Summary Information Stream</span></span>](about-the-summary-information-stream.md)
-   [<span data-ttu-id="b2e9a-113">Utilisation du flux d’informations de synthèse</span><span class="sxs-lookup"><span data-stu-id="b2e9a-113">Using the Summary Information Stream</span></span>](using-the-summary-information-stream.md)
-   [<span data-ttu-id="b2e9a-114">Référence du flux d’informations de synthèse</span><span class="sxs-lookup"><span data-stu-id="b2e9a-114">Summary Information Stream Reference</span></span>](summary-information-stream-reference.md)

 

 



