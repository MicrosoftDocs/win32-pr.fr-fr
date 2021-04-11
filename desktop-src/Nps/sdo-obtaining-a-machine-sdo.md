---
title: Obtention d’un ordinateur SDO
description: La première étape de l’utilisation de l’API SDO consiste à créer un objet ordinateur SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031491"
---
# <a name="obtaining-a-machine-sdo"></a><span data-ttu-id="a4d2e-103">Obtention d’un ordinateur SDO</span><span class="sxs-lookup"><span data-stu-id="a4d2e-103">Obtaining a Machine SDO</span></span>

<span data-ttu-id="a4d2e-104">La première étape de l’utilisation de l’API SDO consiste à créer un objet ordinateur SDO.</span><span class="sxs-lookup"><span data-stu-id="a4d2e-104">The first step in using the SDO API is to create an SDO machine object.</span></span>

<span data-ttu-id="a4d2e-105">Utilisez la fonction [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) pour obtenir l’identificateur de classe (CLSID) de l’objet ordinateur SDO.</span><span class="sxs-lookup"><span data-stu-id="a4d2e-105">Use the [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) function to obtain the class identifier (CLSID) for the SDO machine object.</span></span> <span data-ttu-id="a4d2e-106">L’identificateur programmatique (ProgID) à utiliser pour l’objet est «IAS. SdoMachine".</span><span class="sxs-lookup"><span data-stu-id="a4d2e-106">The programmatic identifier (ProgID) to use for the object is "IAS.SdoMachine".</span></span>

<span data-ttu-id="a4d2e-107">Une fois que vous avez le CLSID, appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec ce CLSID.</span><span class="sxs-lookup"><span data-stu-id="a4d2e-107">Once you have the CLSID, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with this CLSID.</span></span> <span data-ttu-id="a4d2e-108">Spécifiez [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) en tant qu’interface pour laquelle un pointeur doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="a4d2e-108">Specify [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) as the interface for which to return a pointer.</span></span>

<span data-ttu-id="a4d2e-109">Consultez [attachement à un ordinateur SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) pour obtenir un exemple de code qui montre comment obtenir un ordinateur SDO.</span><span class="sxs-lookup"><span data-stu-id="a4d2e-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to obtain a machine SDO.</span></span>

 

 