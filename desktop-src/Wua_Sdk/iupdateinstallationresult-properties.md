---
description: L’interface IUpdateInstallationResult définit les propriétés suivantes.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Propriétés IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201568"
---
# <a name="iupdateinstallationresult-properties"></a><span data-ttu-id="2f90e-103">Propriétés IUpdateInstallationResult</span><span class="sxs-lookup"><span data-stu-id="2f90e-103">IUpdateInstallationResult Properties</span></span>

<span data-ttu-id="2f90e-104">L’interface [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2f90e-104">The [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="2f90e-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="2f90e-105">Property</span></span>                                                           | <span data-ttu-id="2f90e-106">Description</span><span class="sxs-lookup"><span data-stu-id="2f90e-106">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f90e-107">**HResult**</span><span class="sxs-lookup"><span data-stu-id="2f90e-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | <span data-ttu-id="2f90e-108">Obtient la valeur de l’exception **HRESULT** levée pendant l’opération sur une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2f90e-108">Gets the **HRESULT** exception value that is raised during the operation on an update.</span></span>                                            |
| [<span data-ttu-id="2f90e-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="2f90e-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | <span data-ttu-id="2f90e-110">Obtient une valeur booléenne qui indique si un redémarrage système est requis sur un ordinateur pour terminer l’installation d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2f90e-110">Gets a Boolean value that indicates whether a system restart is required on a computer to complete the installation of an update.</span></span> |
| [<span data-ttu-id="2f90e-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="2f90e-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | <span data-ttu-id="2f90e-112">Obtient une valeur [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) qui spécifie le résultat d’une opération sur une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2f90e-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>          |



 

 

 



