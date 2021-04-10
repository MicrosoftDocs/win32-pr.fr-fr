---
title: Messages du pilote
description: Messages du pilote
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- pilotes installables, messages
- pilotes installables, messages personnalisés
- messages du pilote
- messages de pilote personnalisés
- pilotes installables, fonction DriverProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031104"
---
# <a name="driver-messages"></a><span data-ttu-id="8f6ef-108">Messages du pilote</span><span class="sxs-lookup"><span data-stu-id="8f6ef-108">Driver Messages</span></span>

<span data-ttu-id="8f6ef-109">Chaque message de pilote se compose d’un identificateur de message et de paramètres 2 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-109">Each driver message consists of a message identifier and two 32-bit parameters.</span></span> <span data-ttu-id="8f6ef-110">L’identificateur de message est une valeur unique que la fonction [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) vérifie pour déterminer l’action à effectuer. La signification des paramètres du message dépend du message.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-110">The message identifier is a unique value that the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function checks to determine which action to carry out. The meaning of the message parameters depends on the message.</span></span> <span data-ttu-id="8f6ef-111">Les paramètres peuvent représenter des valeurs ou des adresses.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-111">The parameters may represent values or addresses.</span></span> <span data-ttu-id="8f6ef-112">Dans de nombreux cas, les paramètres ne sont pas utilisés et sont définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-112">In many cases, the parameters are not used and are set to zero.</span></span>

<span data-ttu-id="8f6ef-113">Les messages de pilote peuvent être standard ou personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-113">Driver messages can be standard or custom.</span></span> <span data-ttu-id="8f6ef-114">Windows envoie des messages de pilote standard, tels que [**DRV \_ Open**](drv-open.md), [**DRV \_ Close**](drv-close.md)et [**DRV \_ configure**](drv-configure.md), à un pilote installable en réponse à une demande d’ouverture, de fermeture ou de configuration du pilote.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-114">Windows sends standard driver messages, such as [**DRV\_OPEN**](drv-open.md), [**DRV\_CLOSE**](drv-close.md), and [**DRV\_CONFIGURE**](drv-configure.md), to an installable driver in response to a request to open, close, or configure the driver.</span></span> <span data-ttu-id="8f6ef-115">Les messages standard indiquent au pilote installable de charger ou de décharger ses ressources, d’activer ou de désactiver son fonctionnement, d’ouvrir ou de fermer une instance de pilote et d’afficher une boîte de dialogue de configuration.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-115">The standard messages direct the installable driver to load or unload its resources, enable or disable its operation, open or close a driver instance, and display a configuration dialog box.</span></span> <span data-ttu-id="8f6ef-116">Certains messages standard, tels que [**DRV \_ Power**](drv-power.md) et [**DRV \_ EXITSESSION**](drv-exitsession.md), notifient au pilote des événements à l’ensemble du système qui affectent le fonctionnement du pilote ou de tout matériel associé.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-116">Some standard messages, such as [**DRV\_POWER**](drv-power.md) and [**DRV\_EXITSESSION**](drv-exitsession.md), notify the driver of system-wide events that affect the operation of the driver or any related hardware.</span></span>

<span data-ttu-id="8f6ef-117">Les applications et les dll envoient des messages de pilote personnalisés pour indiquer à un pilote installable d’effectuer des actions spécifiques au pilote.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-117">Applications and DLLs send custom driver messages to direct an installable driver to carry out driver-specific actions.</span></span> <span data-ttu-id="8f6ef-118">Les pilotes installables qui prennent en charge les messages personnalisés doivent inclure un traitement approprié dans la fonction **DriverProc** .</span><span class="sxs-lookup"><span data-stu-id="8f6ef-118">Installable drivers that support custom messages must include appropriate processing in the **DriverProc** function.</span></span> <span data-ttu-id="8f6ef-119">Pour éviter les conflits entre les messages de pilote standard et personnalisés, les identificateurs de message personnalisés doivent avoir des valeurs allant de DRV \_ réservé à DRV \_ User.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-119">To prevent conflict between custom and standard driver messages, custom message identifiers must have values ranging from DRV\_RESERVED to DRV\_USER.</span></span> <span data-ttu-id="8f6ef-120">Les messages personnalisés passés à la fonction [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="8f6ef-120">Custom messages passed to the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function are ignored.</span></span>

 

 