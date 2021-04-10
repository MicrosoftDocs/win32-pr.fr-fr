---
description: L’API WiFi Native contient des fonctions, des structures et des énumérations qui prennent en charge la connectivité de réseau sans fil et la gestion des profils sans fil.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: À propos de l’API WiFi Native
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210446"
---
# <a name="about-the-native-wifi-api"></a><span data-ttu-id="3ea90-103">À propos de l’API WiFi Native</span><span class="sxs-lookup"><span data-stu-id="3ea90-103">About the Native Wifi API</span></span>

<span data-ttu-id="3ea90-104">L’API WiFi Native contient des fonctions, des structures et des énumérations qui prennent en charge la connectivité de réseau sans fil et la gestion des profils sans fil.</span><span class="sxs-lookup"><span data-stu-id="3ea90-104">The Native Wifi API contains functions, structures, and enumerations that support wireless network connectivity and wireless profile management.</span></span> <span data-ttu-id="3ea90-105">L’API peut être utilisée pour les réseaux d’infrastructure et ad hoc.</span><span class="sxs-lookup"><span data-stu-id="3ea90-105">The API can be used for both infrastructure and ad hoc networks.</span></span> <span data-ttu-id="3ea90-106">L’API ad hoc sans fil est une interface simplifiée orientée objet pour la création, la gestion et l’utilisation de réseaux ad hoc.</span><span class="sxs-lookup"><span data-stu-id="3ea90-106">The Wireless Ad Hoc API is a simplified object-oriented interface for creating, managing, and using ad hoc networks.</span></span>

> [!Note]  
> <span data-ttu-id="3ea90-107">Le mode ad hoc n’est peut-être pas disponible dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="3ea90-107">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="3ea90-108">À partir de Windows 8.1 et de Windows Server 2012 R2, utilisez plutôt [le Wi-Fi direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="3ea90-108">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

<span data-ttu-id="3ea90-109">L’implémentation de l’API ad hoc utilise l’API WiFi native.</span><span class="sxs-lookup"><span data-stu-id="3ea90-109">The implementation of the Ad Hoc API uses the Native Wifi API.</span></span> <span data-ttu-id="3ea90-110">Cela signifie que les appels d’API ad hoc peuvent déclencher des notifications WiFi natives, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="3ea90-110">This means that Ad Hoc API calls can trigger Native Wifi notifications, and vice versa.</span></span>

<span data-ttu-id="3ea90-111">Il n’est pas recommandé de combiner les appels d’API WiFi natives et les appels d’API ad hoc sans fil.</span><span class="sxs-lookup"><span data-stu-id="3ea90-111">Mixing Native Wifi API calls and Wireless Ad Hoc API calls is not recommended.</span></span> <span data-ttu-id="3ea90-112">Les développeurs doivent choisir une approche de programmation avant de concevoir une application.</span><span class="sxs-lookup"><span data-stu-id="3ea90-112">Developers should choose a programming approach before designing an application.</span></span> <span data-ttu-id="3ea90-113">Si votre application utilise ou gère des réseaux d’infrastructure, vous devez utiliser l’API WiFi native.</span><span class="sxs-lookup"><span data-stu-id="3ea90-113">If your application uses or manages infrastructure networks, you should use the Native Wifi API.</span></span> <span data-ttu-id="3ea90-114">Si votre application nécessite une fonctionnalité de gestion des profils, vous devez utiliser l’API WiFi native.</span><span class="sxs-lookup"><span data-stu-id="3ea90-114">If your application requires profile management functionality, you should use the Native Wifi API.</span></span> <span data-ttu-id="3ea90-115">Dans le cas contraire, vous devez utiliser l’API ad hoc sans fil.</span><span class="sxs-lookup"><span data-stu-id="3ea90-115">Otherwise, you should use the Wireless Ad Hoc API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ea90-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ea90-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ea90-117">À propos de la WiFi Native</span><span class="sxs-lookup"><span data-stu-id="3ea90-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="3ea90-118">Prise en charge de l’API WiFi native sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="3ea90-118">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[<span data-ttu-id="3ea90-119">Autorisations de l’API WiFi Native</span><span class="sxs-lookup"><span data-stu-id="3ea90-119">Native Wifi API Permissions</span></span>](native-wifi-api-permissions.md)
</dt> <dt>

[<span data-ttu-id="3ea90-120">À propos de l’API ad hoc sans fil</span><span class="sxs-lookup"><span data-stu-id="3ea90-120">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="3ea90-121">Télécharger le kit de développement logiciel (SDK) Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ea90-121">Download the Windows Vista SDK</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



