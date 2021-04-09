---
description: L’objet gestionnaire de capteurs fournit l’accès aux capteurs disponibles pour votre utilisation.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: Objet du gestionnaire de capteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112623"
---
# <a name="the-sensor-manager-object"></a><span data-ttu-id="8fbab-103">Objet du gestionnaire de capteurs</span><span class="sxs-lookup"><span data-stu-id="8fbab-103">The Sensor Manager Object</span></span>

<span data-ttu-id="8fbab-104">L’objet gestionnaire de capteurs fournit l’accès aux capteurs disponibles pour votre utilisation.</span><span class="sxs-lookup"><span data-stu-id="8fbab-104">The sensor manager object provides access to the sensors that are available for your use.</span></span>

<span data-ttu-id="8fbab-105">Pour utiliser l’API de capteur, vous devez d’abord appeler la méthode COM **CoCreateInstance** pour créer une instance de l’objet de gestionnaire de capteurs et récupérer un pointeur vers son interface, nommée [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span><span class="sxs-lookup"><span data-stu-id="8fbab-105">To use the Sensor API, you must first call the COM **CoCreateInstance** method to create an instance of the sensor manager object and retrieve a pointer to its interface, named [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span></span> <span data-ttu-id="8fbab-106">Le gestionnaire de capteurs gère la liste des capteurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="8fbab-106">The sensor manager maintains the list of available sensors.</span></span> <span data-ttu-id="8fbab-107">Vous pouvez utiliser **ISensorManager** pour appeler des méthodes qui récupèrent des groupes de capteurs par catégorie ou par type, ou vous pouvez appeler une méthode pour récupérer un capteur particulier à l’aide de son ID unique.</span><span class="sxs-lookup"><span data-stu-id="8fbab-107">You can use **ISensorManager** to call methods that retrieve groups of sensors by category or by type, or you can call a method to retrieve a particular sensor by using its unique ID.</span></span> <span data-ttu-id="8fbab-108">Le gestionnaire de capteurs vous permet également de vous inscrire pour recevoir un événement qui vous avertit lorsqu’un nouveau capteur a été connecté à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="8fbab-108">The sensor manager also enables you to register to receive an event that notifies you when a new sensor has been connected to the platform.</span></span>

<span data-ttu-id="8fbab-109">Parfois, le gestionnaire de capteurs fournit un pointeur vers un capteur, mais l’utilisateur n’a pas activé le capteur.</span><span class="sxs-lookup"><span data-stu-id="8fbab-109">Sometimes, the sensor manager provides a pointer to a sensor, but the user has not enabled the sensor.</span></span> <span data-ttu-id="8fbab-110">Par exemple, vous pouvez souvent récupérer des valeurs pour les propriétés d’un capteur non privé, telles que le modèle ou le fabricant du capteur, avant que l’utilisateur active le capteur.</span><span class="sxs-lookup"><span data-stu-id="8fbab-110">For example, you can often retrieve values for non-private sensor properties, such as the sensor manufacturer or model, before the user enables the sensor.</span></span> <span data-ttu-id="8fbab-111">Ces informations peuvent vous aider à décider s’il faut demander à l’utilisateur l’autorisation d’utiliser le capteur.</span><span class="sxs-lookup"><span data-stu-id="8fbab-111">This information can help you to decide whether to ask the user for permission to use the sensor.</span></span> <span data-ttu-id="8fbab-112">Vous pouvez appeler [**ISensorManager :: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) pour inviter l’utilisateur à activer un capteur ou une collection de capteurs particuliers.</span><span class="sxs-lookup"><span data-stu-id="8fbab-112">You can call [**ISensorManager::RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) to prompt the user to enable a particular sensor or collection of sensors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fbab-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8fbab-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fbab-114">Gestion des autorisations utilisateur</span><span class="sxs-lookup"><span data-stu-id="8fbab-114">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> <dt>

[<span data-ttu-id="8fbab-115">Demande d’autorisations utilisateur</span><span class="sxs-lookup"><span data-stu-id="8fbab-115">Requesting User Permissions</span></span>](requesting-user-permissions.md)
</dt> </dl>

 

 
