---
title: Objets de données de serveur
description: L’API SDO (Server Data Objects) permet de configurer et d’administrer par programme un système exécutant NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509451"
---
# <a name="server-data-objects"></a><span data-ttu-id="b05c5-103">Objets de données de serveur</span><span class="sxs-lookup"><span data-stu-id="b05c5-103">Server Data Objects</span></span>

> [!Note]  
> <span data-ttu-id="b05c5-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b05c5-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="b05c5-105">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="b05c5-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="b05c5-106">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="b05c5-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="b05c5-107">L’API SDO (Server Data Objects) permet de configurer et d’administrer par programme un système exécutant NPS.</span><span class="sxs-lookup"><span data-stu-id="b05c5-107">The Server Data Objects (SDO) API makes it possible to programmatically configure and administer a system running NPS.</span></span> <span data-ttu-id="b05c5-108">À l’aide de SDO, un développeur peut également écrire des applications qui administrent les stratégies d’accès à distance et les profils.</span><span class="sxs-lookup"><span data-stu-id="b05c5-108">Using SDO, a developer can also write applications that administer remote access policies and profiles.</span></span> <span data-ttu-id="b05c5-109">Les stratégies et les profils d’accès à distance sont utilisés par le service de routage et d’accès à distance (RRAS), ainsi que par le serveur NPS pour déterminer si un client distant est autorisé à se connecter à un serveur d’accès réseau (NAS).</span><span class="sxs-lookup"><span data-stu-id="b05c5-109">The remote access policies and profiles are used by the Routing and Remote Access Service (RRAS) as well as NPS to determine whether a remote client is allowed to connect to a network access server (NAS).</span></span>

<span data-ttu-id="b05c5-110">L’API SDO est applicable dans n’importe quel environnement qui utilise des stratégies d’accès à distance ou NPS.</span><span class="sxs-lookup"><span data-stu-id="b05c5-110">The SDO API is applicable in any environment that uses NPS or Remote Access Policies.</span></span>

<span data-ttu-id="b05c5-111">Avec l’API SDO, un développeur peut manipuler tout élément de la configuration NPS qui est accessible via l’interface utilisateur du serveur NPS.</span><span class="sxs-lookup"><span data-stu-id="b05c5-111">With the SDO API, a developer can manipulate any element of the NPS configuration that is accessible through the NPS user interface.</span></span>

<span data-ttu-id="b05c5-112">L’API SDO permet également de définir ou de récupérer les valeurs accessibles via la page de propriétés paramètres de numérotation utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b05c5-112">The SDO API also makes it possible to set or retrieve any of the values accessible through the user dial-in settings property page.</span></span>

<span data-ttu-id="b05c5-113">L’API SDO est composée d’interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="b05c5-113">The SDO API is composed of COM interfaces.</span></span> <span data-ttu-id="b05c5-114">Chacune des interfaces de l’API SDO hérite de l’interface COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b05c5-114">Each of the interfaces in the SDO API inherits from the COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b05c5-115">L’interface **IDispatch** permet aux développeurs d’appeler les méthodes d’interface SDO à partir de Visual Basic ou de n’importe quel client Automation, ainsi qu’à partir de C/C++.</span><span class="sxs-lookup"><span data-stu-id="b05c5-115">The **IDispatch** interface enables developers to call the SDO interface methods from Visual Basic or any Automation client, as well as from C/C++.</span></span>

<span data-ttu-id="b05c5-116">Les développeurs peuvent également appeler l’API SDO à partir de langages de script tels que VBScript.</span><span class="sxs-lookup"><span data-stu-id="b05c5-116">Developers can also call the SDO API from scripting languages such as VBScript.</span></span> <span data-ttu-id="b05c5-117">Toutefois, étant donné que VBScript est limité à l’utilisation des paramètres de type VARIANT uniquement, les fonctionnalités de SDO ne sont pas toutes disponibles.</span><span class="sxs-lookup"><span data-stu-id="b05c5-117">However, because VBScript is limited to using VARIANT-type parameters only, not all the functionality of SDO is available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b05c5-118">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b05c5-118">In This Section</span></span>

[<span data-ttu-id="b05c5-119">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b05c5-119">Overview</span></span>](/windows/desktop/Nps/sdo-about-server-data-objects)

<span data-ttu-id="b05c5-120">Informations générales sur l’API des objets de données du serveur.</span><span class="sxs-lookup"><span data-stu-id="b05c5-120">General information about the Server Data Objects API.</span></span>

[<span data-ttu-id="b05c5-121">À</span><span class="sxs-lookup"><span data-stu-id="b05c5-121">Using</span></span>](/windows/desktop/Nps/sdo-using-server-data-objects)

<span data-ttu-id="b05c5-122">Exemple de code qui montre comment utiliser l’API des objets de données du serveur.</span><span class="sxs-lookup"><span data-stu-id="b05c5-122">Sample code that demonstrates how to use the Server Data Objects API.</span></span>

[<span data-ttu-id="b05c5-123">Référence</span><span class="sxs-lookup"><span data-stu-id="b05c5-123">Reference</span></span>](/windows/desktop/Nps/sdo-server-data-objects-reference)

<span data-ttu-id="b05c5-124">Documentation des types énumérés et des interfaces qui composent l’API des objets de données du serveur.</span><span class="sxs-lookup"><span data-stu-id="b05c5-124">Documentation of the enumerated types and interfaces that compose the Server Data Objects API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b05c5-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b05c5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b05c5-126">Serveur de stratégie réseau (service d’authentification Internet)</span><span class="sxs-lookup"><span data-stu-id="b05c5-126">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="b05c5-127">Service d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="b05c5-127">Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 