---
description: Vous pouvez installer des produits entiers avec des fonctions de Windows Installer. Les étapes suivantes décrivent l’installation d’un produit.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Installation d’une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519508"
---
# <a name="installing-an-application"></a><span data-ttu-id="8715f-104">Installation d’une application</span><span class="sxs-lookup"><span data-stu-id="8715f-104">Installing an Application</span></span>

<span data-ttu-id="8715f-105">Vous pouvez installer des produits entiers avec des fonctions de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8715f-105">You can install entire products with Windows Installer functions.</span></span> <span data-ttu-id="8715f-106">Les étapes suivantes décrivent l’installation d’un produit.</span><span class="sxs-lookup"><span data-stu-id="8715f-106">The following steps describe how to install a product.</span></span>

<span data-ttu-id="8715f-107">**Pour installer un produit**</span><span class="sxs-lookup"><span data-stu-id="8715f-107">**To install a product**</span></span>

1.  <span data-ttu-id="8715f-108">Exécutez un produit par le biais de sa séquence d’installation ou de désinstallation en appelant la fonction [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) .</span><span class="sxs-lookup"><span data-stu-id="8715f-108">Run a product through its installation or uninstallation sequence by calling the [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) function.</span></span>
2.  <span data-ttu-id="8715f-109">Spécifiez le niveau d’installation en appelant la fonction [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .</span><span class="sxs-lookup"><span data-stu-id="8715f-109">Specify the installation level by calling the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function.</span></span>

    <span data-ttu-id="8715f-110">Vous pouvez utiliser les paramètres de la fonction [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) pour définir l’état d’installation.</span><span class="sxs-lookup"><span data-stu-id="8715f-110">You can use the parameters of the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function to set the installation state.</span></span> <span data-ttu-id="8715f-111">Par exemple, vous pouvez définir l’État sur installer localement ou pour installer à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="8715f-111">For example, you can set the state to install locally or to install from the source.</span></span> <span data-ttu-id="8715f-112">Vous pouvez définir la plage de fonctionnalités du produit à inclure en définissant le niveau.</span><span class="sxs-lookup"><span data-stu-id="8715f-112">You can set the range of product features to be included by setting the level.</span></span>

<span data-ttu-id="8715f-113">Pour plus d’informations sur l’installation d’une application, consultez [résilience](resiliency.md) et [mécanisme d’installation](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="8715f-113">For more information about installing an application, see [Resiliency](resiliency.md) and [Installation Mechanism](installation-mechanism.md).</span></span>

 

 



