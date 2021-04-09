---
description: Représente la configuration de l’historique des fichiers de l’utilisateur sous lequel l’objet FhConfigMgr est créé. Toutes les opérations de configuration sont effectuées en appelant les méthodes de l’interface IFhConfigMgr.
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: FhConfigMgr, classe (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 083ce344e44035b5872d91ad14465659defc8229
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861077"
---
# <a name="fhconfigmgr-class"></a><span data-ttu-id="6ae0f-104">FhConfigMgr, classe</span><span class="sxs-lookup"><span data-stu-id="6ae0f-104">FhConfigMgr class</span></span>

<span data-ttu-id="6ae0f-105">Représente la configuration de l’historique des fichiers de l’utilisateur sous lequel l’objet **FhConfigMgr** est créé.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-105">Represents the File History configuration of the user under which the **FhConfigMgr** object is created.</span></span> <span data-ttu-id="6ae0f-106">Toutes les opérations de configuration sont effectuées en appelant les méthodes de l’interface [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) .</span><span class="sxs-lookup"><span data-stu-id="6ae0f-106">All configuration operations are performed by calling the methods of the [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="6ae0f-107">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="6ae0f-107">When to implement</span></span>

<span data-ttu-id="6ae0f-108">L’API d’historique des fichiers implémente cette classe.</span><span class="sxs-lookup"><span data-stu-id="6ae0f-108">The File History API implements this class.</span></span> <span data-ttu-id="6ae0f-109">Pour créer une instance de cette classe, utilisez la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="6ae0f-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae0f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ae0f-110">Requirements</span></span>



| <span data-ttu-id="6ae0f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ae0f-111">Requirement</span></span> | <span data-ttu-id="6ae0f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ae0f-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae0f-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ae0f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae0f-114">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ae0f-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6ae0f-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ae0f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae0f-116">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ae0f-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6ae0f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ae0f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ae0f-118"><dt>Fhcfg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae0f-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ae0f-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="6ae0f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ae0f-120"><dt>Fhcfg. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ae0f-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
