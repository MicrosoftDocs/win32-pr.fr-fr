---
description: L’interface IInstallationResult définit les propriétés suivantes.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Propriétés IInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034042"
---
# <a name="iinstallationresult-properties"></a><span data-ttu-id="b0303-103">Propriétés IInstallationResult</span><span class="sxs-lookup"><span data-stu-id="b0303-103">IInstallationResult Properties</span></span>

<span data-ttu-id="b0303-104">L’interface [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b0303-104">The [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="b0303-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="b0303-105">Property</span></span>                                                     | <span data-ttu-id="b0303-106">Description</span><span class="sxs-lookup"><span data-stu-id="b0303-106">Description</span></span>                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0303-107">**HResult**</span><span class="sxs-lookup"><span data-stu-id="b0303-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | <span data-ttu-id="b0303-108">Obtient le **HRESULT** de l’exception, le cas échéant, qui est déclenché pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="b0303-108">Gets the **HRESULT** of the exception, if any, that is raised during the installation.</span></span>                                                 |
| [<span data-ttu-id="b0303-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="b0303-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | <span data-ttu-id="b0303-110">Obtient une valeur booléenne qui indique si vous devez redémarrer l’ordinateur pour terminer l’installation ou la désinstallation d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b0303-110">Gets a Boolean value that indicates whether you must restart the computer to complete the installation or uninstallation of an update.</span></span> |
| [<span data-ttu-id="b0303-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="b0303-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | <span data-ttu-id="b0303-112">Obtient une valeur [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) qui spécifie le résultat d’une opération sur une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b0303-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>               |



 

 

 



