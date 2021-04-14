---
title: Interface IWMDRMDeviceApp2
description: L’interface IWMDRMDeviceApp2 étend IWMDRMDeviceApp en fournissant une nouvelle version de la méthode QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interface IWMDRMDeviceApp2 Windows Media Gestionnaire de périphériques
- Interface IWMDRMDeviceApp2 Windows Media Gestionnaire de périphériques, Description
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313135"
---
# <a name="iwmdrmdeviceapp2-interface"></a><span data-ttu-id="dfc8f-105">Interface IWMDRMDeviceApp2</span><span class="sxs-lookup"><span data-stu-id="dfc8f-105">IWMDRMDeviceApp2 interface</span></span>

<span data-ttu-id="dfc8f-106">L’interface **IWMDRMDeviceApp2** étend [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) en fournissant une nouvelle version de la méthode [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="dfc8f-106">The **IWMDRMDeviceApp2** interface extends [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) by providing a new version of the [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) method.</span></span> <span data-ttu-id="dfc8f-107">**QueryDeviceStatus2** permet à l’appelant de demander une exigence DRM spécifique.</span><span class="sxs-lookup"><span data-stu-id="dfc8f-107">**QueryDeviceStatus2** enables the caller to query for a specific DRM requirement.</span></span>

<span data-ttu-id="dfc8f-108">Pour accéder à cette interface, appelez **CoCreateInstance** et transmettez le CLSID \_ WMDRMDeviceApp.</span><span class="sxs-lookup"><span data-stu-id="dfc8f-108">To get this interface, call **CoCreateInstance** and pass in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="dfc8f-109">Cette interface est définie dans le fichier d’en-tête généré à partir de WMDRMDeviceApp. idl.</span><span class="sxs-lookup"><span data-stu-id="dfc8f-109">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="dfc8f-110">Cet en-tête **\# comprend** « WMDM. h ».</span><span class="sxs-lookup"><span data-stu-id="dfc8f-110">This header **\#includes** "wmdm.h".</span></span> <span data-ttu-id="dfc8f-111">Vous devrez peut-être modifier ce nom de fichier pour qu’il corresponde à l’en-tête généré à partir de WMDM. idl.</span><span class="sxs-lookup"><span data-stu-id="dfc8f-111">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="dfc8f-112">Membres</span><span class="sxs-lookup"><span data-stu-id="dfc8f-112">Members</span></span>

<span data-ttu-id="dfc8f-113">L’interface **IWMDRMDeviceApp2** hérite de [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span><span class="sxs-lookup"><span data-stu-id="dfc8f-113">The **IWMDRMDeviceApp2** interface inherits from [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span></span> <span data-ttu-id="dfc8f-114">**IWMDRMDeviceApp2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dfc8f-114">**IWMDRMDeviceApp2** also has these types of members:</span></span>

-   [<span data-ttu-id="dfc8f-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dfc8f-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dfc8f-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dfc8f-116">Methods</span></span>

<span data-ttu-id="dfc8f-117">L’interface **IWMDRMDeviceApp2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dfc8f-117">The **IWMDRMDeviceApp2** interface has these methods.</span></span>



| <span data-ttu-id="dfc8f-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="dfc8f-118">Method</span></span>                                                            | <span data-ttu-id="dfc8f-119">Description</span><span class="sxs-lookup"><span data-stu-id="dfc8f-119">Description</span></span>                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="dfc8f-120">**QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="dfc8f-120">**QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md) | <span data-ttu-id="dfc8f-121">Interroge un appareil pour obtenir un État ou une fonctionnalité DRM spécifique.</span><span class="sxs-lookup"><span data-stu-id="dfc8f-121">Queries a device for a specific DRM status or capability.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="dfc8f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfc8f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc8f-123">**IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="dfc8f-123">**IWMDRMDeviceApp**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="dfc8f-124">**Gestion du contenu protégé dans l’application**</span><span class="sxs-lookup"><span data-stu-id="dfc8f-124">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="dfc8f-125">**Interfaces pour les applications**</span><span class="sxs-lookup"><span data-stu-id="dfc8f-125">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="dfc8f-126">**Contrôle de l’utilisation du contenu**</span><span class="sxs-lookup"><span data-stu-id="dfc8f-126">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

 





