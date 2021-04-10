---
description: Définit un profil de réseau local sans fil utilisé par le service de configuration automatique WiFi natif.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: Schéma WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112723"
---
# <a name="wlan_profile-schema"></a><span data-ttu-id="59d12-103">\_Schéma de profil WLAN</span><span class="sxs-lookup"><span data-stu-id="59d12-103">WLAN\_profile Schema</span></span>

<span data-ttu-id="59d12-104">Le \_ schéma de profil WLAN définit un profil de réseau local sans fil utilisé par le service de configuration automatique WiFi natif.</span><span class="sxs-lookup"><span data-stu-id="59d12-104">The WLAN\_profile Schema defines a WLAN profile used by the Native Wifi AutoConfig service.</span></span>

<span data-ttu-id="59d12-105">Le service de configuration automatique accepte les profils sans fil de l’agent stratégie de groupe, de l’interface de script (**netsh**), de l’interface utilisateur ou de l’interface de configuration flash USB.</span><span class="sxs-lookup"><span data-stu-id="59d12-105">The AutoConfig service accepts wireless profiles from the Group Policy Agent, the scripting interface (**netsh**), the user interface, or from the USB flash configuration interface.</span></span>

<span data-ttu-id="59d12-106">Un profil reçu à partir de l’un de ces systèmes est mappé au \_ schéma de profil WLAN et stocké dans le magasin de profils.</span><span class="sxs-lookup"><span data-stu-id="59d12-106">A profile received from one of these systems is mapped to the WLAN\_profile schema and stored in the profile store.</span></span> <span data-ttu-id="59d12-107">Les profils peuvent être exportés à partir du magasin de profils à l’aide des commandes netsh ou à l’aide d’éléments d’API tels que [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span><span class="sxs-lookup"><span data-stu-id="59d12-107">Profiles can be exported from the profile store using netsh commands or using API elements such as [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span></span>

<span data-ttu-id="59d12-108">L’élément racine d’un profil WLAN est l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="59d12-108">The root element of a WLAN profile is the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span> <span data-ttu-id="59d12-109">Chaque profil aura un seul élément racine.</span><span class="sxs-lookup"><span data-stu-id="59d12-109">Each profile will have exactly one root element.</span></span> <span data-ttu-id="59d12-110">L’élément **WLANProfile** est dans l’espace de noms `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="59d12-110">The **WLANProfile** element is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

<span data-ttu-id="59d12-111">Pour afficher des exemples de profils WLAN, consultez la page exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="59d12-111">To view sample WLAN profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

-   [<span data-ttu-id="59d12-112">\_Éléments de schéma de profil WLAN</span><span class="sxs-lookup"><span data-stu-id="59d12-112">WLAN\_profile Schema Elements</span></span>](wlan-profileschema-elements.md)
-   [<span data-ttu-id="59d12-113">\_Types simples de schéma de profil WLAN</span><span class="sxs-lookup"><span data-stu-id="59d12-113">WLAN\_profile Schema Simple Types</span></span>](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a><span data-ttu-id="59d12-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59d12-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="59d12-115">[Commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="59d12-115">[Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span></span>
</dt> </dl>

 

 
