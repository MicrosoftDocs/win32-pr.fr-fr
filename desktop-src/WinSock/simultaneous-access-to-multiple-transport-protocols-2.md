---
description: Un protocole de transport doit être correctement installé sur le système et enregistré auprès de Windows Sockets pour être accessible à une application.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Accès simultané à plusieurs protocoles de transport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519025"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a><span data-ttu-id="99ca2-103">Accès simultané à plusieurs protocoles de transport</span><span class="sxs-lookup"><span data-stu-id="99ca2-103">Simultaneous Access to Multiple Transport Protocols</span></span>

<span data-ttu-id="99ca2-104">Un protocole de transport doit être correctement installé sur le système et enregistré auprès de Windows Sockets pour être accessible à une application.</span><span class="sxs-lookup"><span data-stu-id="99ca2-104">A transport protocol must be properly installed on the system and registered with Windows Sockets to be accessible to an application.</span></span> <span data-ttu-id="99ca2-105">La \_ bibliothèque Ws232.dll exporte un ensemble de fonctions pour faciliter le processus d’inscription.</span><span class="sxs-lookup"><span data-stu-id="99ca2-105">The Ws2\_32.dll library exports a set of functions to facilitate the registration process.</span></span> <span data-ttu-id="99ca2-106">Cela comprend la création d’une nouvelle inscription et la suppression d’une inscription existante.</span><span class="sxs-lookup"><span data-stu-id="99ca2-106">This includes creating a new registration and removing an existing one.</span></span>

<span data-ttu-id="99ca2-107">Lorsque de nouvelles inscriptions sont créées, l’appelant (autrement dit, le script d’installation du fournisseur de la pile) fournit une ou plusieurs structures d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) renseignées contenant un ensemble complet d’informations sur le protocole.</span><span class="sxs-lookup"><span data-stu-id="99ca2-107">When new registrations are created, the caller (that is, the stack vendor's installation script) supplies one or more filled in [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures containing a complete set of information about the protocol.</span></span> <span data-ttu-id="99ca2-108">Pour plus d’informations, consultez [SPI Windows Sockets 2](about-the-winsock-spi.md).</span><span class="sxs-lookup"><span data-stu-id="99ca2-108">For more information, see [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span></span> <span data-ttu-id="99ca2-109">Toute pile de transport installée de cette manière est appelée fournisseur de services Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="99ca2-109">Any transport stack installed in this manner is referred to as a Windows Sockets service provider.</span></span>

<span data-ttu-id="99ca2-110">Sur Windows XP avec Service Pack 2 (SP2), Windows Server 2003 avec Service Pack 1 (SP1) et Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="99ca2-110">On Windows XP with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), and Windows Vista and later.</span></span> <span data-ttu-id="99ca2-111">le catalogue Winsock qui contient une liste de fournisseurs de transport et d’espaces de noms installés peut être affiché dans une invite de commandes avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="99ca2-111">the Winsock catalog that contains a list of installed transport and namespace providers can be displayed in a command prompt with the following command:</span></span>

<span data-ttu-id="99ca2-112">**netsh Winsock-afficher le catalogue**</span><span class="sxs-lookup"><span data-stu-id="99ca2-112">**netsh winsock show catalog**</span></span>

<span data-ttu-id="99ca2-113">Le kit de développement logiciel (SDK) Microsoft Windows comprend *Sporder.exe*, qui permet à l’utilisateur d’afficher et de modifier l’ordre dans lequel les fournisseurs de services sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="99ca2-113">The Microsoft Windows Software Development Kit (SDK) includes *Sporder.exe*, which enables the user to view and modify the order in which service providers are enumerated.</span></span> <span data-ttu-id="99ca2-114">À l’aide de *Sporder.exe*, un utilisateur peut établir manuellement une pile de protocole TCP/IP particulière comme fournisseur TCP/IP par défaut si plusieurs piles de ce type sont présentes.</span><span class="sxs-lookup"><span data-stu-id="99ca2-114">Using *Sporder.exe*, a user can manually establish a particular TCP/IP protocol stack as the default TCP/IP provider if more than one such stack is present.</span></span>

<span data-ttu-id="99ca2-115">L’application *Sporder.exe* utilise des fonctions exportées de *Sporder.dll* pour réorganiser les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="99ca2-115">The *Sporder.exe* application uses exported functions from *Sporder.dll* to reorder the service providers.</span></span> <span data-ttu-id="99ca2-116">Par conséquent, les applications d’installation peuvent utiliser l’interface fournie par *Sporder.dll* pour réorganiser par programmation des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="99ca2-116">As a result, installation applications can use the interface provided by *Sporder.dll* to programmatically reorder service providers.</span></span>

-   [<span data-ttu-id="99ca2-117">Protocoles et chaînes de protocole en couches</span><span class="sxs-lookup"><span data-stu-id="99ca2-117">Layered Protocols and Protocol Chains</span></span>](layered-protocols-and-protocol-chains-2.md)
-   [<span data-ttu-id="99ca2-118">Utilisation de plusieurs protocoles</span><span class="sxs-lookup"><span data-stu-id="99ca2-118">Using Multiple Protocols</span></span>](using-multiple-protocols-2.md)
-   [<span data-ttu-id="99ca2-119">Plusieurs restrictions de fournisseur sur SELECT</span><span class="sxs-lookup"><span data-stu-id="99ca2-119">Multiple Provider Restrictions on Select</span></span>](multiple-provider-restrictions-on-select-2.md)

 

 
