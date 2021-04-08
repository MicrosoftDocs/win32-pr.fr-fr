---
description: TSPIMessage est un type d’énumération qui définit l’ensemble des fonctions LINEEVENT et PHONEEVENT supplémentaires qui apparaissent dans TSPI qui n’apparaissent pas dans l’interface TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753717"
---
# <a name="tspimessage"></a><span data-ttu-id="cb856-103">TSPIMessage</span><span class="sxs-lookup"><span data-stu-id="cb856-103">TSPIMessage</span></span>

<span data-ttu-id="cb856-104">**TSPIMessage** est un type d’énumération qui définit l’ensemble des fonctions [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) et [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) supplémentaires qui apparaissent dans TSPI qui n’apparaissent pas dans l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="cb856-104">**TSPIMessage** is an enumeration type that defines the set of additional [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) and [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) functions appearing in TSPI that do not appear in TAPI.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb856-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb856-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb856-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_base de messages TSPI \_</span><span class="sxs-lookup"><span data-stu-id="cb856-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI\_MESSAGE\_BASE</span></span>
</dt> <dd>

<span data-ttu-id="cb856-107">Nombre le plus bas dans la plage de valeurs de message spécifiques à TSPI.</span><span class="sxs-lookup"><span data-stu-id="cb856-107">The lowest number in the range of TSPI-specific message values.</span></span> <span data-ttu-id="cb856-108">Cette valeur n’a aucune signification, mais sert de base pour définir les autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="cb856-108">This value has no meaning by itself, but serves as a base for defining the other values.</span></span>

</dd> <dt>

<span data-ttu-id="cb856-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>NEWCALL de ligne \_</span><span class="sxs-lookup"><span data-stu-id="cb856-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINE\_NEWCALL</span></span>
</dt> <dd>

<span data-ttu-id="cb856-110">Spécifie qu’un nouvel appel entrant est arrivé et l’introduit dans l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="cb856-110">Specifies that a new, incoming call has arrived and introduces it to TAPI.</span></span> <span data-ttu-id="cb856-111">Il doit s’agir du premier message envoyé à l’interface TAPI pour un nouvel appel entrant.</span><span class="sxs-lookup"><span data-stu-id="cb856-111">This must be the first message sent to TAPI for a new incoming call.</span></span> <span data-ttu-id="cb856-112">L’interface TAPI retourne son identificateur opaque pour l’appel dans le cadre de sa gestion de ce message.</span><span class="sxs-lookup"><span data-stu-id="cb856-112">TAPI returns its opaque identifier for the call as part of its handling of this message.</span></span>

</dd> <dt>

<span data-ttu-id="cb856-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>CALLDEVSPECIFIC de ligne \_</span><span class="sxs-lookup"><span data-stu-id="cb856-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINE\_CALLDEVSPECIFIC</span></span>
</dt> <dd>

<span data-ttu-id="cb856-114">Spécifie qu’un événement spécifique à l’appareil s’est produit sur un appareil d’appel.</span><span class="sxs-lookup"><span data-stu-id="cb856-114">Specifies that a device-specific event has occurred on a call device.</span></span>

</dd> <dt>

<span data-ttu-id="cb856-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>CALLDEVSPECIFICFEATURE de ligne \_</span><span class="sxs-lookup"><span data-stu-id="cb856-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE\_CALLDEVSPECIFICFEATURE</span></span>
</dt> <dd>

<span data-ttu-id="cb856-116">Spécifie qu’un événement de fonctionnalité spécifique à l’appareil s’est produit sur un appareil d’appel.</span><span class="sxs-lookup"><span data-stu-id="cb856-116">Specifies that a device-specific feature event has occurred on a call device.</span></span>

</dd> </dl>

 

 
