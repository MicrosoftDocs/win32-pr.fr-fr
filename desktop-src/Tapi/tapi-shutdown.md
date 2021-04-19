---
description: L’arrêt correct des sessions de communication et d’une application complète est nécessaire pour empêcher les ressources de rester liées dans les appels ou les applications qui n’en ont plus besoin.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Arrêt de l’interface TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538938"
---
# <a name="tapi-shutdown"></a><span data-ttu-id="06adf-103">Arrêt de l’interface TAPI</span><span class="sxs-lookup"><span data-stu-id="06adf-103">TAPI Shutdown</span></span>

<span data-ttu-id="06adf-104">L’arrêt correct des sessions de communication et d’une application complète est nécessaire pour empêcher les ressources de rester liées dans les appels ou les applications qui n’en ont plus besoin.</span><span class="sxs-lookup"><span data-stu-id="06adf-104">Proper shutdown of communications sessions and of an entire application is required to prevent resources from remaining tied up in calls or applications that no longer need them.</span></span>

<span data-ttu-id="06adf-105">L’interface TAPI fournit une série de fonctions et de méthodes pour vous aider dans le processus.</span><span class="sxs-lookup"><span data-stu-id="06adf-105">TAPI provides a series of functions and methods to assist in the process.</span></span> <span data-ttu-id="06adf-106">Évidemment, l’application doit également prendre la responsabilité de libérer correctement la mémoire allouée, que ce soit sous la forme de structures de données ou de références COM.</span><span class="sxs-lookup"><span data-stu-id="06adf-106">Obviously, the application must also take responsibility for properly releasing allocated memory, whether in the form of data structures or COM references.</span></span>



| <span data-ttu-id="06adf-107">Fonctions TAPI 2. x</span><span class="sxs-lookup"><span data-stu-id="06adf-107">TAPI 2.x functions</span></span>                                                            | <span data-ttu-id="06adf-108">Description</span><span class="sxs-lookup"><span data-stu-id="06adf-108">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="06adf-109">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="06adf-109">**lineRegisterRequestRecipient**</span></span>](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="06adf-110">Annule l’inscription de l’application en tant que gestionnaire pour les appels de téléphonie assistés.</span><span class="sxs-lookup"><span data-stu-id="06adf-110">Unregisters the application as a handler for assisted telephony calls.</span></span> |
| [<span data-ttu-id="06adf-111">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="06adf-111">**lineClose**</span></span>](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | <span data-ttu-id="06adf-112">Déconnecte l’application en tant que responsable des appels sur la ligne donnée.</span><span class="sxs-lookup"><span data-stu-id="06adf-112">Disconnects the application as a manager for calls on the given line.</span></span>  |
| [<span data-ttu-id="06adf-113">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="06adf-113">**lineShutdown**</span></span>](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | <span data-ttu-id="06adf-114">Arrête l’utilisation de l’application de l’abstraction de ligne.</span><span class="sxs-lookup"><span data-stu-id="06adf-114">Shuts down the application's usage of the line abstraction.</span></span>            |



 



| <span data-ttu-id="06adf-115">Interfaces ou méthodes TAPI 3. x</span><span class="sxs-lookup"><span data-stu-id="06adf-115">TAPI 3.x interfaces or methods</span></span>                                            | <span data-ttu-id="06adf-116">Description</span><span class="sxs-lookup"><span data-stu-id="06adf-116">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="06adf-117">**ITTAPI::UnregisterNotifications**</span><span class="sxs-lookup"><span data-stu-id="06adf-117">**ITTAPI::UnregisterNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | <span data-ttu-id="06adf-118">Supprime toutes les inscriptions de notifications d’événements effectuées par l’application.</span><span class="sxs-lookup"><span data-stu-id="06adf-118">Removes any event notification registrations performed by the application.</span></span> |
| [<span data-ttu-id="06adf-119">**ITTAPI :: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="06adf-119">**ITTAPI::Shutdown**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | <span data-ttu-id="06adf-120">Déconnecte l’application en tant que gestionnaire d’appels.</span><span class="sxs-lookup"><span data-stu-id="06adf-120">Disconnects the application as a call manager.</span></span>                             |



 

 

 
