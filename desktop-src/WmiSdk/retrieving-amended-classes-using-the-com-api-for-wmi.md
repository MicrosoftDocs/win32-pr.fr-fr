---
description: 'Si vous utilisez l’API COM pour WMI pour récupérer ou stocker des informations de classe localisées, spécifiez les paramètres régionaux dans le paramètre strLocale de l’interface IWbemLocator :: ConnectServer.'
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Récupération des classes modifiées à l’aide de l’API COM pour WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759760"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a><span data-ttu-id="4dcca-103">Récupération des classes modifiées à l’aide de l’API COM pour WMI</span><span class="sxs-lookup"><span data-stu-id="4dcca-103">Retrieving Amended Classes Using the COM API for WMI</span></span>

<span data-ttu-id="4dcca-104">Si vous utilisez l’API COM pour WMI pour récupérer ou stocker des informations de classe localisées, spécifiez les paramètres régionaux dans le paramètre *strLocale* de l’interface [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="4dcca-104">If you are using the COM API for WMI to retrieve or store localized class information, specify the locale in the *strLocale* parameter to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) interface.</span></span> <span data-ttu-id="4dcca-105">Lors de la lecture ou de l’écriture de classes modifiées, indiquez que vous souhaitez utiliser les définitions de classe localisées en spécifiant \_ l’indicateur WBEM \_ utiliser \_ \_ des qualificateurs modifiés comme indicateur pour le paramètre *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="4dcca-105">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS as a flag for the *iFlags* parameter.</span></span>

<span data-ttu-id="4dcca-106">Le tableau suivant répertorie les versions synchrones et asynchrones des méthodes qui utilisent l’indicateur WBEM \_ \_ utiliser des \_ \_ qualificateurs modifiés.</span><span class="sxs-lookup"><span data-stu-id="4dcca-106">The following table lists the synchronous and asynchronous versions of the methods that use the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span>



| <span data-ttu-id="4dcca-107">Méthode synchrone</span><span class="sxs-lookup"><span data-stu-id="4dcca-107">Synchronous Method</span></span>                                                            | <span data-ttu-id="4dcca-108">Méthode asynchrone</span><span class="sxs-lookup"><span data-stu-id="4dcca-108">Asynchronous Method</span></span>                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="4dcca-109">**IWbemServices :: CreateClassEnum**</span><span class="sxs-lookup"><span data-stu-id="4dcca-109">**IWbemServices::CreateClassEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [<span data-ttu-id="4dcca-110">**IWbemServices :: CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="4dcca-110">**IWbemServices::CreateClassEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [<span data-ttu-id="4dcca-111">**IWbemServices :: CreateInstanceEnum**</span><span class="sxs-lookup"><span data-stu-id="4dcca-111">**IWbemServices::CreateInstanceEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [<span data-ttu-id="4dcca-112">**IWbemServices :: CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="4dcca-112">**IWbemServices::CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [<span data-ttu-id="4dcca-113">**IWbemServices :: ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="4dcca-113">**IWbemServices::ExecQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [<span data-ttu-id="4dcca-114">**IWbemServices :: ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="4dcca-114">**IWbemServices::ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [<span data-ttu-id="4dcca-115">**IWbemServices :: GetObject**</span><span class="sxs-lookup"><span data-stu-id="4dcca-115">**IWbemServices::GetObject**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [<span data-ttu-id="4dcca-116">**IWbemServices :: GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="4dcca-116">**IWbemServices::GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [<span data-ttu-id="4dcca-117">**IWbemServices ::P utClass**</span><span class="sxs-lookup"><span data-stu-id="4dcca-117">**IWbemServices::PutClass**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [<span data-ttu-id="4dcca-118">**IWbemServices ::P utClassAsync**</span><span class="sxs-lookup"><span data-stu-id="4dcca-118">**IWbemServices::PutClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [<span data-ttu-id="4dcca-119">**IWbemServices ::P utInstance**</span><span class="sxs-lookup"><span data-stu-id="4dcca-119">**IWbemServices::PutInstance**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [<span data-ttu-id="4dcca-120">**IWbemServices ::P utInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="4dcca-120">**IWbemServices::PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



