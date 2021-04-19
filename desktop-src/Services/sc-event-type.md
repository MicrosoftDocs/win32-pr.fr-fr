---
description: Indique un type de changement d’état de service pour l’analyse et la création de rapports.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Énumération SC_EVENT_TYPE (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545105"
---
# <a name="sc_event_type-enumeration"></a><span data-ttu-id="ce7c2-103">\_Énumération des types d’événements SC \_</span><span class="sxs-lookup"><span data-stu-id="ce7c2-103">SC\_EVENT\_TYPE enumeration</span></span>

<span data-ttu-id="ce7c2-104">Indique un type de changement d’état de service pour l’analyse et la création de rapports.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-104">Indicates a type of service status change for monitoring and reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce7c2-105">Syntax</span></span>


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ce7c2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ce7c2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ce7c2-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**\_ \_ modification de la base de données d’événements SC \_**</span><span class="sxs-lookup"><span data-stu-id="ce7c2-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC\_EVENT\_DATABASE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="ce7c2-108">Un service a été ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-108">A service has been added or deleted.</span></span> <span data-ttu-id="ce7c2-109">Le paramètre *hService* de la fonction [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) doit être un handle vers le SCM.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-109">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the SCM.</span></span>

</dd> <dt>

<span data-ttu-id="ce7c2-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**modification de la propriété de l' \_ événement SC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ce7c2-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC\_EVENT\_PROPERTY\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="ce7c2-111">Une ou plusieurs propriétés de service ont été mises à jour.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-111">One or more of service properties have been updated.</span></span> <span data-ttu-id="ce7c2-112">Le paramètre *hService* de la fonction [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) doit être un handle du service.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-112">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ce7c2-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**modification de l’état de l' \_ événement SC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ce7c2-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC\_EVENT\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="ce7c2-114">L’état d’un service a changé.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-114">The status of a service has changed.</span></span> <span data-ttu-id="ce7c2-115">Le paramètre *hService* de la fonction [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) doit être un handle du service.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-115">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce7c2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce7c2-116">Requirements</span></span>



| <span data-ttu-id="ce7c2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce7c2-117">Requirement</span></span> | <span data-ttu-id="ce7c2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce7c2-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7c2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce7c2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ce7c2-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ce7c2-120">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="ce7c2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce7c2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ce7c2-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ce7c2-122">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="ce7c2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce7c2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce7c2-124"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce7c2-124"><dt>Winsvcp.h</dt></span></span> </dl> |



 

 




