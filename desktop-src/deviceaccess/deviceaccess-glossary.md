---
title: Glossaire de l’accès aux appareils
description: Voici les termes utilisés dans la documentation de l’API d’accès aux appareils.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381455"
---
# <a name="device-access-glossary"></a><span data-ttu-id="a8263-103">Glossaire de l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="a8263-103">Device Access Glossary</span></span>

<span data-ttu-id="a8263-104">Voici les termes utilisés dans la documentation de l’API d’accès aux appareils.</span><span class="sxs-lookup"><span data-stu-id="a8263-104">The following are terms used throughout the documentation for the Device Access API.</span></span>

<dl> <dt>

<span data-ttu-id="a8263-105">**Conteneur**</span><span class="sxs-lookup"><span data-stu-id="a8263-105">**AppContainer**</span></span>
</dt> <dd>

<span data-ttu-id="a8263-106">Environnement d’exécution hautement restreint dans lequel un processus s’exécute avec un sous-ensemble réduit des privilèges de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a8263-106">A highly restricted execution environment in which a process runs with a reduced subset of the user's privileges.</span></span> <span data-ttu-id="a8263-107">Un processus qui s’exécute dans un AppContainer est appelé « processus AppContainer ».</span><span class="sxs-lookup"><span data-stu-id="a8263-107">A process that's running within an AppContainer is called an AppContainer process.</span></span> <span data-ttu-id="a8263-108">Un processus AppContainer est isolé des autres processus AppContainer et du profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a8263-108">An AppContainer process is isolated from other AppContainer processes and from the user's profile.</span></span> <span data-ttu-id="a8263-109">Il dispose d’un accès limité à un très petit sous-ensemble de ressources système telles que les fichiers, les périphériques, les clés de Registre, les points de terminaison d’appel de procédure à distance (RPC) de communication entre processus (IPC) et les ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="a8263-109">It has limited access to a very small subset of system resources like files, devices, registry keys, interprocess communication (IPC)/remote procedure call (RPC) endpoints, and network resources.</span></span>

</dd> <dt>

<span data-ttu-id="a8263-110">**Binding**</span><span class="sxs-lookup"><span data-stu-id="a8263-110">**Binding**</span></span>
</dt> <dd>

<span data-ttu-id="a8263-111">Association d’un objet d’accès d’appareil à une interface d’appareil particulière.</span><span class="sxs-lookup"><span data-stu-id="a8263-111">Associating a device access object with a particular device interface.</span></span> <span data-ttu-id="a8263-112">Si la liaison est réussie, les applications du Windows Store peuvent utiliser l’objet d’accès de l’appareil en tant que répartiteur pour communiquer avec le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="a8263-112">If binding is successful, Windows Store apps can use the device access object as a broker to communicate with the device driver.</span></span>

</dd> <dt>

<span data-ttu-id="a8263-113">**Service Broker**</span><span class="sxs-lookup"><span data-stu-id="a8263-113">**Broker**</span></span>
</dt> <dd>

<span data-ttu-id="a8263-114">Composant qui fournit l’accès à une ressource qui n’est pas accordée par défaut.</span><span class="sxs-lookup"><span data-stu-id="a8263-114">A component that provides access to a resource that isn't granted by default.</span></span>

</dd> <dt>

<span data-ttu-id="a8263-115">**Application privilégiée**</span><span class="sxs-lookup"><span data-stu-id="a8263-115">**Privileged App**</span></span>
</dt> <dd>

<span data-ttu-id="a8263-116">Application identifiée dans les métadonnées d’un appareil particulier, comme associé à ce périphérique, afin qu’il puisse communiquer avec l’interface restreinte du pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="a8263-116">An app that's identified in a particular device's metadata as associated with that device, so that it can communicate with the device driver's restricted interface.</span></span> <span data-ttu-id="a8263-117">Un exemple d’une telle application peut être une application de lecture musicale propriétaire qui dispose d’une autorisation exclusive pour se synchroniser avec un lecteur de musique portable, lorsque les applications de concurrents ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="a8263-117">An example of such an app might be a proprietary music playback app that has exclusive permission to sync with a portable music player, when apps from competitors can't.</span></span> <span data-ttu-id="a8263-118">Pour plus d’informations sur la façon de définir les métadonnées d’un appareil ou sur la façon de restreindre un pilote aux applications privilégiées, consultez [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span><span class="sxs-lookup"><span data-stu-id="a8263-118">For more information about how to set a device's metadata or how to restrict a driver to privileged apps, see [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span></span>

</dd> </dl>
